<script>
  import { layout, url, isActive } from "@roxi/routify";
</script>

<header class="text-gray-600 body-font">
  <div class="container mx-auto sm:flex sm:flex-wrap sm:p-5 sm:flex-row items-center sm:static sm:z-0 sm:bg-transparent sm:* block fixed inset-x-0 bottom-0 z-10 bg-white shadow">
    <a class="flex title-font font-medium items-center text-gray-900 mb-4 sm:mb-0" href='/'>
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-10 h-10 text-white p-2 bg-yellow-500 rounded-full" viewBox="0 0 24 24">
        <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path>
      </svg>
      <span class="ml-3 text-xl">Portal Kajian</span>
    </a>
    <nav class="sm:ml-auto flex flex-wrap items-center text-base justify-center">
      {#each $layout.children as {path, title}}
      <a class="mr-5 hover:text-gray-900" href={$url(path)} class:active={$isActive(path)}>{title}</a>
      {/each}
    </nav>
    <button class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 sm:mt-0">Login
      <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
        <path d="M5 12h14M12 5l7 7-7 7"></path>
      </svg>
    </button>
  </div>
</header>