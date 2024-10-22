<script lang="ts">
  import BlogPostLayout from '$lib/components/BlogPostLayout.svelte';

  const title = "Post Mortem: First Game Jam";
  const date = "2023-10-22";
</script>

<BlogPostLayout {title} {date}>
  <p>I took a challenge to make a game in 10 days for the Revival Game Jam 2024. Here's a post-mortem of the experience.</p>

  <h2>Why did I do it?</h2>
  <p>I am feeling very bipolar in my development skillset. Some might call it being a reneissance man, in reality I am just a jack of all trades, master of none. Before being efficient at anything, I find a new shiny object I want to learn. Usually I ignite a flame of passion, but before being able to see the fruit of my idea, I reach a point of burn out. So when I discovered there is a game jam, I liked the idea of pressuring myself to finish within such a short time frame. To jump into something I never did before, and try for the first time ever to build a game.</p>

  <h2>The Game Jam</h2>
  <p>The game jam hosted by the <a href="https://societyofplay.net/" target="_blank">Society of Play</a> was running from the 4th to the 21st of October. I discovered it on the 10th, and I spent the first 2 days switching between different game engines, before deciding on using <a href="https://phaser.io/" target="_blank">phaser</a> with <a href="https://svelte.dev/" target="_blank">svelte</a>.</p>
  <figure>
    <img src="/images/blog/post-mortem/1.png" alt="moment of commitment" />
    <figcaption>moment of commitment</figcaption>
  </figure>



  <h2>The Theme</h2>
  <p>The theme of the game jam was <strong>Revival</strong>. I decided to revive <a href="https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life" target="_blank">The Game of Life</a>, the amazing mathematical game from John Conway. Ever since learning about it, I was fascinated by the concept of emergent behavior, and the idea that a simple set of rules can create complex and unpredictable patterns. I wanted to make a game that would allow people to experience this, and hopefully get someone intruiged about it as well.</p>

  <h2>The Development Process</h2>
  <p>For the first time ever, I created a txt file to make sure I stay on track when building.</p>
  <figure>
    <img src="/images/blog/post-mortem/2.png" alt="development plan" />
    <figcaption>development plan</figcaption>
  </figure>
  <p>I am an AI lover, so of course I was using cursor all the way. Instead of reading the docs like a good boy, I went straight into building the game. I am new to svelte as well, so I took this as a great learning experience on how svelte as well as phaser works.</p>
  <p>The first thing I did was building a simulation of the game of life, and I started experimenting with different game ideas. Right from the beginning I knew that I wanted to make the game goal to survive, I just didnt know how yet.</p>


  <h2>The game of life</h2>
  <p>Quickly, I started getting familiar with the behavior of the game of life, and I started learning more about the different shapes and their behavior.</p>
  <p>The gliders, the LWSS, and the Pulsars felt the most usable for a game system.</p>
  <p>I wanted to make sure the game can be easily picked up even with people who dont know the game of life, so I created pre-generated structures for the player.</p>
  <figure>
    <img src="/images/blog/post-mortem/3.png" alt="game of life" />
    <figcaption>pre-made structures</figcaption>
  </figure>
  <p>The game was slowly taking shape, I realized by itself the rules of the game of life are fun and nicely unpredictable, so all I needed now was a trigger for the player to experience the chaos.</p>
  
  <h2>The core game loop</h2>
  <p>I decided the pulsars will represent the players base, and their lives. Upon destruction of them all, the game is over.</p>
  <p>For the enemies, I was experimenting with the enemy using the same shapes of ships, but the predictable movement made aiming for the enemy hard, and for the player easy to avoid. I decided to use small red snakes, that spawn in intervals on random positions within the game grid. They automatically move towards the nearest pulsar.</p>
  
  <h2>Time to make it fun!</h2>
  <p>The game wasnt dynamic. The player could stop the generations at any time, and this lead to constant start and stop of the game.</p>
  <p>While taking a break, a video on youtube jumped at me. It was named <a href="https://youtu.be/3EmDlsj27nA" target="_blank">"How to instantly increase your game's fun
    "</a> </p>
  <p><strong>It proposed a fun experiment:</strong> try 10xing some value inside of your game, and see how it changes the experience. I started with making enemies spawn 10x faster, it was fun, but the break through was when I aplied this to the game speed. I realized its much more visually pleasing when the generations happen fast.</p>
  <p>After doing that, making the game turn-based, automatically stopping every 50 generations, was an obvious move.</p>


  <h2>The help along the way</h2>
  <p>Often I reached out with a question in the society of play discord, and it lead me to some great improvements and feedback. The music and sounds within the game wouldnt be there without the society of play.</p>
  <p>I also got to show my game in the Show n Play event before the game jam ended, which was a nice boost of motivation.</p>


  <h2>The finishing touches</h2>
  <p>After being satisfied with the game loop, came a frustrating period of bug fixing. I saw my online deployment was running sooooo slow and laggy compared with the local version.</p>
  <p>I had to actually learn about phaser, actually learn about rendering and proper structure to fix this, but I managed.</p>
  <p>Just today I finally got the game working within itch io website, and I am very happy with the result.</p>
  <h2>Lessons Learned</h2>
  <ul>
    <li>Just do it, less thinking, more doing.</li>
    <li>Pressure is a great friend of mine.</li>
    <li>Take a break to refresh your thinking.</li>
    <li>The community is a great source of motivation and feedback.</li>

  </ul>



  <h2>Conclusion</h2>
  <p>I wouldnt do anything differently, this went great. Had this game jam been longer and giving me more time, not sure I would finish it. The pressure was great.</p>
  <p>If you want to play the game, you can find it <a href="https://brianpistar.itch.io/cellular-domination-station" target="_blank">here</a>.</p>
</BlogPostLayout>
