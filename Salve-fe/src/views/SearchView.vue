<template>
    <div class="max-w-7xl text-slate-300 mx-auto grid grid-cols-1 sm:grid-cols-4 gap-4">
        <div class="main-left col-span-3 space-y-4">
            <div class="bg-slate-600 rounded-lg">
                <div class="p-4 flex space-x-4">  
                    <input type="search" class="p-4 w-full bg-blue-50 rounded-lg text-sm sm:text-base" placeholder="What are you looking for?">

                    <a href="#" class="inline-block py-4 px-6 bg-blue-500 text-white rounded-lg">Search</a>
                </div>
            </div>

            <div class="p-3 bg-slate-600 rounded-lg grid grid-cols-3 sm:grid-cols-4 gap-4">
                <div class="p-4 text-center bg-slate-800 rounded-lg">
                    <img src="https://avatars.githubusercontent.com/u/113662172?s=1000&v=4" class="mb-6 rounded-full">
                
                    <p><strong>Jomel</strong></p>

                    <div class="mt-6 flex space-x-4 sm:space-x-8 justify-around">
                        <p class="text-xs">182 friends</p>
                        <p class="text-xs">120 posts</p>
                    </div>
                </div>

                <div class="p-4 text-center bg-slate-800 rounded-lg">
                    <img src="https://avatars.githubusercontent.com/u/113662172?s=1000&v=4" class="mb-6 rounded-full">
                
                    <p><strong>Jomel</strong></p>

                    <div class="mt-6 flex space-x-4 sm:space-x-8 justify-around">
                        <p class="text-xs">182 friends</p>
                        <p class="text-xs">120 posts</p>
                    </div>
                </div>

                <div class="p-4 text-center bg-slate-800 rounded-lg">
                    <img src="https://avatars.githubusercontent.com/u/113662172?s=1000&v=4" class="mb-6 rounded-full">
                
                    <p><strong>Jomel</strong></p>

                    <div class="mt-6 flex space-x-4 sm:space-x-8 justify-around">
                        <p class="text-xs">182 friends</p>
                        <p class="text-xs">120 posts</p>
                    </div>
                </div>

                <div class="p-4 text-center bg-slate-800 rounded-lg">
                    <img src="https://avatars.githubusercontent.com/u/113662172?s=1000&v=4" class="mb-6 rounded-full">
                
                    <p><strong>Jomel</strong></p>

                    <div class="mt-6 flex space-x-4 sm:space-x-8 justify-around">
                        <p class="text-xs">182 friends</p>
                        <p class="text-xs">120 posts</p>
                    </div>
                </div>
                
                <div class="p-4 text-center bg-slate-800 rounded-lg">
                    <img src="https://avatars.githubusercontent.com/u/113662172?s=1000&v=4" class="mb-6 rounded-full">
                
                    <p><strong>Jomel</strong></p>

                    <div class="mt-6 flex space-x-4 sm:space-x-8 justify-around">
                        <p class="text-xs">182 friends</p>
                        <p class="text-xs">120 posts</p>
                    </div>
                </div>
            </div>

            <div class="p-4 bg-slate-600 rounded-lg">
                <div class="mb-6 flex items-center justify-between">
                    <div class="flex items-center space-x-6">
                        <img src="https://avatars.githubusercontent.com/u/113662172?s=1000&v=4" class="w-[40px] rounded-full">
                        
                        <p><strong>Jomel</strong></p>
                    </div>

                    <p class="">18 minutes ago</p>
                </div>

                <p class="text-xl text-white">God is good all the time!</p>

                <div class="my-6 flex justify-between">
                    <div class="flex space-x-6">
                        <div class="flex items-center space-x-2">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 7.5l3 2.25-3 2.25m4.5 0h3m-9 8.25h13.5A2.25 2.25 0 0021 18V6a2.25 2.25 0 00-2.25-2.25H5.25A2.25 2.25 0 003 6v12a2.25 2.25 0 002.25 2.25z" />
                            </svg>
  
                            
                            <span class="text-xs">82 commends</span>
                        </div>
                        
                        <div class="flex items-center space-x-2">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 20.25c4.97 0 9-3.694 9-8.25s-4.03-8.25-9-8.25S3 7.444 3 12c0 2.104.859 4.023 2.273 5.48.432.447.74 1.04.586 1.641a4.483 4.483 0 01-.923 1.785A5.969 5.969 0 006 21c1.282 0 2.47-.402 3.445-1.087.81.22 1.668.337 2.555.337z"></path>
                            </svg> 

                            <span class="text-xs">0 remarks</span>
                        </div>
                    </div>
                    
                    <div>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.75a.75.75 0 110-1.5.75.75 0 010 1.5zM12 12.75a.75.75 0 110-1.5.75.75 0 010 1.5zM12 18.75a.75.75 0 110-1.5.75.75 0 010 1.5z"></path>
                        </svg>   
                    </div>   
                </div>  
            </div>
        </div>

        <div class="main-right col-span-3 sm:col-span-1 space-y-4">
            <PeopleYouMayKnow />

            <Trends />
        </div>
    </div>
</template>

<script>
import PeopleYouMayKnow from '../components/PeopleYouMayKnow.vue'
import Trends from '../components/Trends.vue'

export default {
    name: 'SearchView',
    components: {
        PeopleYouMayKnow,
        Trends,
    }
}
</script>