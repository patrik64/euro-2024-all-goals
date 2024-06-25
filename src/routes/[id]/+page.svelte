<script>
  export let data;

  let id = '';
  for(let x in data) {
    id += data[x];
  }

  import round1 from "$lib/data/round1.json";

  let game = round1[id - 1];
</script>

{#if game}
<div class="my-10 mx-auto lg:w-1/2 bg-white shadow overflow-hidden sm:rounded-lg">
  <div class="px-4 py-5 sm:px-6">
    <div class="text-2xl leading-6 font-medium">{game.team1} - {game.team2}</div>
    <div class="py-2 text-2xl leading-6 font-medium">{game.result}</div>
</div>
  <div class="border-t border-gray-200 px-4 py-5 sm:p-0">
    {#each game.links as link}
    <dl class="sm:divide-y sm:divide-gray-200">
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">{link.currentresult}</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{link.snippet}</dd>
      </div>
    </dl>
    {/each}
  </div>
</div>
{/if}