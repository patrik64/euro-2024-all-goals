<script>
  export let data;

  let id = '';
  for(let x in data) {
    id += data[x];
  }

  import round1 from "$lib/data/round1.json";
  import round2 from "$lib/data/round2.json";
  import round3 from "$lib/data/round3.json";

  let idx = parseInt(id, 10)
  
  let game = round1[idx - 1];

  if (idx > 12 && idx <= 24) {
    game = round2[idx - 13];
  }

  if (idx >= 25) {
    game = round3[idx - 25];
  }
  
</script>

{#if game}
<div class="my-10 mx-auto lg:w-1/2 bg-white shadow overflow-hidden sm:rounded-lg">
  <div class="px-4 py-5 sm:px-6">
    <div class="text-2xl leading-6 font-medium">{game.team1} {game.result1} - {game.team2} {game.result2}</div>
  </div>
  <div class="border-t border-gray-200 px-4 py-5 sm:p-0">
    {#each game.links as link}
    <dl class="sm:divide-y sm:divide-gray-200">
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">
          <a rel="external" href="{link.link}" class="text-teal-800 space-y-4">
            {game.team1} {link.currentresult1} - {game.team2} {link.currentresult2}
          </a>
        </dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">
          {#if link.video.length > 0}
          <video controls>
            <source src="{link.video}" type="video/mp4">
          </video>
          {/if}
        </dd>
      </div>
    </dl>
    {/each}
  </div>
</div>
{/if}