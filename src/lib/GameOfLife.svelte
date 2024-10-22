<script lang="ts">
  import { onMount, onDestroy } from 'svelte';
  import { browser } from '$app/environment';

  let canvas: HTMLCanvasElement;
  let ctx: CanvasRenderingContext2D | null;
  let cells: number[][];
  let cellSize = 10; // Decreased cell size for more cells
  let cols: number;
  let rows: number;
  let animationId: number;
  let lastDrawTime = 0;
  const frameDelay = 100; // Delay between frames in milliseconds (adjust as needed)

  function setup(): void {
    if (!browser || !canvas) return;
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
    cols = Math.floor(canvas.width / cellSize);
    rows = Math.floor(canvas.height / cellSize);
    cells = Array(cols).fill(null).map(() => Array(rows).fill(0));
    for (let i = 0; i < cols; i++) {
      for (let j = 0; j < rows; j++) {
        cells[i][j] = Math.random() > 0.85 ? 1 : 0; // Further reduced initial population
      }
    }
  }

  function draw(): void {
    if (!browser || !ctx || !canvas) return;
    // Clear the entire canvas
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    for (let i = 0; i < cols; i++) {
      for (let j = 0; j < rows; j++) {
        let x = i * cellSize;
        let y = j * cellSize;
        if (cells[i][j] === 1) {
          ctx.fillStyle = 'rgba(0, 255, 0, 0.3)'; // Slightly increased opacity
          ctx.fillRect(x, y, cellSize - 1, cellSize - 1);
        }
      }
    }

    let next = cells.map(arr => [...arr]);

    for (let i = 0; i < cols; i++) {
      for (let j = 0; j < rows; j++) {
        let state = cells[i][j];
        let neighbors = countNeighbors(cells, i, j);

        if (state === 0 && neighbors === 3) {
          next[i][j] = 1;
        } else if (state === 1 && (neighbors < 2 || neighbors > 3)) {
          next[i][j] = 0;
        } else {
          next[i][j] = state;
        }
      }
    }

    cells = next;
  }

  function countNeighbors(cells: number[][], x: number, y: number): number {
    let sum = 0;
    for (let i = -1; i < 2; i++) {
      for (let j = -1; j < 2; j++) {
        let col = (x + i + cols) % cols;
        let row = (y + j + rows) % rows;
        sum += cells[col][row];
      }
    }
    sum -= cells[x][y];
    return sum;
  }

  function animate(currentTime: number) {
    if (currentTime - lastDrawTime > frameDelay) {
      draw();
      lastDrawTime = currentTime;
    }
    animationId = requestAnimationFrame(animate);
  }

  function handleResize() {
    if (!browser || !canvas) return;
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
    setup();
  }

  onMount(() => {
    if (!browser || !canvas) return;
    ctx = canvas.getContext('2d');
    setup();
    lastDrawTime = performance.now();
    animate(lastDrawTime);
    window.addEventListener('resize', handleResize);
  });

  onDestroy(() => {
    if (browser) {
      if (animationId) {
        cancelAnimationFrame(animationId);
      }
      window.removeEventListener('resize', handleResize);
    }
  });
</script>

{#if browser}
  <canvas bind:this={canvas} class="fixed top-0 left-0 w-full h-full opacity-50"></canvas>
{/if}

<style>
  canvas {
    pointer-events: none;
    z-index: -1;
  }
</style>
