<script>
  import round1 from "$lib/data/round1.json";
  import round2 from "$lib/data/round2.json";
  import round3 from "$lib/data/round3.json";
  import round16 from "$lib/data/round16.json";
  import quarter from "$lib/data/quarter-final.json"
</script>
  
<div class="max-w-7xl mx-auto py-8 sm:py-16 sm:px-6 lg:px-8">

  <!-- quarter-final -->
  <div class="sm:flex sm:items-center">
    <div class="sm:flex-auto">
      <h1 class="lg:pt-10 text-3xl text-gray-600 text-center">Quarter-final</h1>
    </div>
  </div>

  <div>
    <ul class="py-6 mx-4 lg:mx-auto grid grid-cols-2 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-3xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-4">
      {#each quarter as game}
      <li class="mx-auto">
          <div class="w-[10rem] md:w-[11rem] whitespace-nowrap bg-white mt-4 select-none cursor-pointer rounded-lg shadow-lg hover:bg-tertiary-500 hover:border-gray-700 transition duration-500 ease-in-out">
            <a href={`/${game.id}`}>
              <div class="flex flex-col py-4">
              <div class="flex">
                <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
                <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
              </div>
              <div class="space-y-2">
                <div class="whitespace-nowrap text-xs font-medium lg:text-sm text-center">
                  <h3>
                    <div class="text-black">{game.team1} - {game.team2}</div>
                    <div class="text-black">{game.result}</div>
                  </h3>
                </div>
              </div>
              </div>
            </a>
          </div>
        </li>
      {/each}
    </ul>
  </div>

   <!-- round 16 -->
   <div class="sm:flex sm:items-center">
    <div class="sm:flex-auto">
      <h1 class="lg:pt-10 text-3xl text-gray-600 text-center">Round of 16</h1>
    </div>
  </div>

  <div>
    <ul class="py-6 mx-4 lg:mx-auto grid grid-cols-2 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-3xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-4">
      {#each round16 as game}
      <li class="mx-auto">
          <div class="w-[10rem] md:w-[11rem] whitespace-nowrap bg-white mt-4 select-none cursor-pointer rounded-lg shadow-lg hover:bg-tertiary-500 hover:border-gray-700 transition duration-500 ease-in-out">
            <a href={`/${game.id}`}>
              <div class="flex flex-col py-4">
              <div class="flex">
                <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
                <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
              </div>
              <div class="space-y-2">
                <div class="whitespace-nowrap text-xs font-medium lg:text-sm text-center">
                  <h3>
                    <div class="text-black">{game.team1} - {game.team2}</div>
                    <div class="text-black">{game.result}</div>
                  </h3>
                </div>
              </div>
              </div>
            </a>
          </div>
        </li>
      {/each}
    </ul>
  </div>

  <!-- round 3 -->
  <div class="sm:flex sm:items-center">
    <div class="sm:flex-auto">
      <h1 class="lg:pt-10 text-3xl text-gray-600 text-center">Round 3</h1>
    </div>
  </div>

  <div>
    <ul class="py-6 mx-4 lg:mx-auto grid grid-cols-2 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-6xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-6">
      {#each round3 as game}
      <li class="mx-auto">
          <div class="w-[10rem] md:w-[11rem] whitespace-nowrap bg-white mt-4 select-none cursor-pointer rounded-lg shadow-lg hover:bg-tertiary-500 hover:border-gray-700 transition duration-500 ease-in-out">
            <a href={`/${game.id}`}>
              <div class="flex flex-col py-4">
              <div class="flex">
                <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
                <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
              </div>
              <div class="space-y-2">
                <div class="whitespace-nowrap text-xs font-medium lg:text-sm text-center">
                  <h3>
                    <div class="text-black">{game.team1} - {game.team2}</div>
                    <div class="text-black">{game.result}</div>
                  </h3>
                </div>
              </div>
              </div>
            </a>
          </div>
        </li>
      {/each}
    </ul>
  </div>

  <!-- round 2 -->
  <div class="sm:flex sm:items-center">
    <div class="sm:flex-auto">
      <h1 class="lg:pt-10 text-3xl text-gray-600 text-center">Round 2</h1>
    </div>
  </div>

  <div>
    <ul class="py-6 mx-4 lg:mx-auto grid grid-cols-2 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-6xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-6">
      {#each round2 as game}
      <li class="mx-auto">
        <div class="w-[10rem] md:w-[11rem] whitespace-nowrap bg-white mt-4 select-none cursor-pointer rounded-lg shadow-lg hover:bg-tertiary-500 hover:border-gray-700 transition duration-500 ease-in-out">
          <a href={`/${game.id}`}>
            <div class="flex flex-col py-4">
            <div class="flex">
              <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
              <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
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
          </div>
        </li>
      {/each}
    </ul>
  </div>

  <!-- round 1 -->
  <div class="flex justify-center items-center">
    <h1 class="lg:pt-10 text-3xl text-gray-600">Round 1</h1>
  </div>

  
    <ul class="py-6 mx-4 lg:mx-auto grid grid-cols-2 gap-y-8 sm:grid-cols-4 md:gap-x-6 lg:max-w-6xl lg:gap-x-8 lg:gap-y-8 xl:grid-cols-6">
      {#each round1 as game}
        <li class="mx-auto">
        <div class="w-[10rem] md:w-[11rem] whitespace-nowrap bg-white mt-4 select-none cursor-pointer rounded-lg shadow-lg hover:bg-tertiary-500 hover:border-gray-700 transition duration-500 ease-in-out">
          <a href={`/${game.id}`}>
            <div class="flex flex-col py-4">
            <div class="flex">
              <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag1}`} alt={game.team1} />
              <img class="mx-auto h-10 w-10 rounded-md object-cover" src={`/images/countries/${game.flag2}`} alt={game.team2} />
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
          </div>
        </li>
      {/each}
    </ul>
  

</div>
