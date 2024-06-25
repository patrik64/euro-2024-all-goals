<script>
  import round1 from "$lib/data/round1.json";
  import round2 from "$lib/data/round2.json";
</script>
  
<div class="max-w-7xl mx-auto py-8 sm:py-16 sm:px-6 lg:px-8">

  <!-- round 1 -->
  <div class="flex justify-center items-center">
    <h1 class="lg:p-10 text-3xl text-gray-600">Round 1</h1>
  </div>
  
  <div class="lg:border-dashed lg:rounded-md lg:border-gray-400 lg:border-2" >
    <ul class="py-6 mx-4 grid grid-cols-2 gap-x-12 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-6xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-6">
      {#each round1 as game}
        <li>
          <a href={`/${game.id}`}>
            <div class="flex flex-col w-48 p-4 border-solid border-2 rounded-lg">
            <div class="flex">
              <img class="mx-auto h-10 w-10 rounded-full object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
              <img class="mx-auto h-10 w-10 rounded-full object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
            </div>
            <div class="space-y-2">
              <div class="text-xs font-medium lg:text-sm text-center">
                <h3>
                  <div class="text-black">{game.team1} - {game.team2}</div>
                  <div class="text-black">{game.result}</div>
                </h3>
              </div>
            </div>
            </div>
          </a>
        </li>
      {/each}
    </ul>
  </div>

  <!-- round 2 -->
  <div class="sm:flex sm:items-center">
    <div class="sm:flex-auto">
      <h1 class="lg:p-10 text-3xl text-gray-600 text-center">Round 2</h1>
    </div>
  </div>

  <div class="lg:border-dashed lg:rounded-md lg:border-gray-400 lg:border-2" >
    <ul class="py-6 mx-4 grid grid-cols-2 gap-x-12 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-6xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-6">
      {#each round2 as game}
        <li>
          <a href={`/${game.id}`}>
            <div class="flex flex-col w-48 p-4 border-solid border-2 rounded-lg">
            <div class="flex">
              <img class="mx-auto h-10 w-10 rounded-full object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
              <img class="mx-auto h-10 w-10 rounded-full object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
            </div>
            <div class="space-y-2">
              <div class="text-xs font-medium lg:text-sm text-center">
                <h3>
                  <div class="text-black">{game.team1} - {game.team2}</div>
                  <div class="text-black">{game.result}</div>
                </h3>
              </div>
            </div>
            </div>
          </a>
        </li>
      {/each}
    </ul>
  </div>

</div>
