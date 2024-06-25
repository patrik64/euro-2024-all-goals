<script>
  import Youtube from "svelte-youtube-embed";
  export let data;

  let id = '';
  for(let x in data) {
    id += data[x];
  }

  import movies from "$lib/data/movies.json";

  let movie = movies[id - 1];
</script>

{#if movie}
<div class="my-10 mx-auto lg:w-1/2 bg-white shadow overflow-hidden sm:rounded-lg">
  <div class="px-4 py-5 sm:px-6">
    <div class="text-2xl leading-6 font-medium">{movie.name}</div>
    {#if movie.image && movie.image.length > 0}
      <img class="my-4 object-contain" src={`/images/movies/${movie.image}`} alt="" />
      <div class="text-xss text-gray-500">&copy; imdb</div>
    {/if}
  </div>
  <div class="border-t border-gray-200 px-4 py-5 sm:p-0">
    <dl class="sm:divide-y sm:divide-gray-200">
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Name</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.name}</dd>
      </div>
      {#if movie.name !== movie.engname}
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">ENG Name</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.engname}</dd>
      </div>
      {/if}
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">IMDB Score</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.score}</dd>
      </div>
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Year</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.year}</dd>
      </div>
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Movie Length</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.length}</dd>
      </div>
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">IMDB</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2"><a href={movie.links[1].lvalue} class="hover:text-black">{movie.links[1].lvalue}</a></dd>
      </div>
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Viennale</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2"><a href={movie.links[0].lvalue} class="hover:text-black">{movie.links[0].lvalue}</a></dd>
      </div>
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Show 1</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.shows[0].date} - {movie.shows[0].time}h - {movie.shows[0].weekday} - {movie.shows[0].kino}</dd>
      </div>
      {#if movie.shows[1].kino.length > 0}
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Show 2</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2">{movie.shows[1].date} - {movie.shows[1].time}h - {movie.shows[1].weekday} - {movie.shows[1].kino}</dd>
      </div>
      {/if}
      {#if movie.trailer}
      <div class="py-4 sm:py-5 sm:grid sm:grid-cols-4 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-600">Trailer</dt>
        <dd class="mt-1 text-sm text-gray-600 sm:mt-0 sm:col-span-2"><Youtube id="{movie.trailer}" /></dd>
      </div>
      {/if}
    </dl>
  </div>
</div>
{/if}