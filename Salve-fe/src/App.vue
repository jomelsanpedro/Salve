
<template>
 <nav class="bg-slate-700">
      <div class="max-w-7xl mx-auto">
            <div class="py-3 px-2 flex items-center justify-between  sm:-mb-5">
                <div class="menu-left flex items-center flex-shrink-0 text-slate-400">
                    <a href="" class="font-semibold sm:text-xl text-2xl tracking-tight ml-3">S A L V E</a>
                </div>
                <div class="menu-right flex items-center flex-shrink-0 mr-4 w-9 h-9 sm:w-12 sm:h-12">
                    <a href="#">
                    <img src="https://avatars.githubusercontent.com/u/113662172?s=70&v=4" class="rounded-full">
                    </a>
                </div>
            </div>
                
            <div class="py-2 flex items-center justify-center relative">
              <div class="menu-center flex space-x-16 sm:absolute
                        sm:left-30 
                        sm:-top-10">
                  
                  <RouterLink :to="{'name': 'feed'}" class="text-slate-400">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-9 h-9 sm:w-12 sm:h-12">
                        <path d="M11.47 3.84a.75.75 0 011.06 0l8.69 8.69a.75.75 0 101.06-1.06l-8.689-8.69a2.25 2.25 0 00-3.182 0l-8.69 8.69a.75.75 0 001.061 1.06l8.69-8.69z" />
                        <path d="M12 5.432l8.159 8.159c.03.03.06.058.091.086v6.198c0 1.035-.84 1.875-1.875 1.875H15a.75.75 0 01-.75-.75v-4.5a.75.75 0 00-.75-.75h-3a.75.75 0 00-.75.75V21a.75.75 0 01-.75.75H5.625a1.875 1.875 0 01-1.875-1.875v-6.198a2.29 2.29 0 00.091-.086L12 5.43z" />
                    </svg>
                  </RouterLink>
                  <RouterLink :to="{'name': 'message'}" class="text-slate-400">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-9 h-9 sm:w-12 sm:h-12">
                        <path fill-rule="evenodd" d="M4.848 2.771A49.144 49.144 0 0112 2.25c2.43 0 4.817.178 7.152.52 1.978.292 3.348 2.024 3.348 3.97v6.02c0 1.946-1.37 3.678-3.348 3.97a48.901 48.901 0 01-3.476.383.39.39 0 00-.297.17l-2.755 4.133a.75.75 0 01-1.248 0l-2.755-4.133a.39.39 0 00-.297-.17 48.9 48.9 0 01-3.476-.384c-1.978-.29-3.348-2.024-3.348-3.97V6.741c0-1.946 1.37-3.68 3.348-3.97zM6.75 8.25a.75.75 0 01.75-.75h9a.75.75 0 010 1.5h-9a.75.75 0 01-.75-.75zm.75 2.25a.75.75 0 000 1.5H12a.75.75 0 000-1.5H7.5z" clip-rule="evenodd" />
                    </svg>
                  </RouterLink>

                  <a href="#" class="text-slate-400">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-9 h-9 sm:w-12 sm:h-12">
                        <path fill-rule="evenodd" d="M5.25 9a6.75 6.75 0 0113.5 0v.75c0 2.123.8 4.057 2.118 5.52a.75.75 0 01-.297 1.206c-1.544.57-3.16.99-4.831 1.243a3.75 3.75 0 11-7.48 0 24.585 24.585 0 01-4.831-1.244.75.75 0 01-.298-1.205A8.217 8.217 0 005.25 9.75V9zm4.502 8.9a2.25 2.25 0 104.496 0 25.057 25.057 0 01-4.496 0z" clip-rule="evenodd" />
                    </svg>         
                  </a>

                  <RouterLink :to="{'name': 'search'}" class="text-slate-400">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-9 h-9 sm:w-12 sm:h-12">
                        <path d="M8.25 10.875a2.625 2.625 0 115.25 0 2.625 2.625 0 01-5.25 0z" />
                        <path fill-rule="evenodd" d="M12 2.25c-5.385 0-9.75 4.365-9.75 9.75s4.365 9.75 9.75 9.75 9.75-4.365 9.75-9.75S17.385 2.25 12 2.25zm-1.125 4.5a4.125 4.125 0 102.338 7.524l2.007 2.006a.75.75 0 101.06-1.06l-2.006-2.007a4.125 4.125 0 00-3.399-6.463z" clip-rule="evenodd" />
                    </svg> 
                  </RouterLink>
              </div>
          </div>
      </div>
  </nav>

  <main class="px-8 py-6 bg-slate-900">
      <RouterView />
  </main>
  <Toast />
</template>
<script>
  import Toast from '@/components/Toast.vue'
  export default{
    components: {
      Toast
    }
  }
</script>