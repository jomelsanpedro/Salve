<template>
    <div class="max-w-7xl mx-auto grid grid-cols-2 gap-4">
        <div class="main-left">
            <div class="p-12 bg-slate-700 rounded-lg">
                <form class="space-y-8">
                    <div class="relative">
                        <input 
                            id="email" 
                            name="email" 
                            type="email" 
                            placeholder="Email" 
                            class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label for="email" 
                        class="
                        absolute
                        left-3 
                        -top-6
                        text-slate-400
                        transition-all
                        peer-placeholder-shown:text-base 
                        peer-placeholder-shown:text-slate-400    
                        peer-placeholder-shown:top-6 
                        peer-focus:-top-6 
                        peer-focus:text-slate-400  
                        peer-focus:text-xl
                        select-none
                        pointer-events-none
                        ">Email</label>
                    </div>
                    <!-- absolute
                        left-3 
                        -top-3.5 
                        text-black 
                        text-sm 
                        transition-all 
                        peer-placeholder-shown:text-base 
                        peer-placeholder-shown:text-black    
                        peer-placeholder-shown:top-0 
                        peer-focus:-top-6 
                        peer-focus:text-slate-400 
                        peer-focus:text-xl -->
                    <div class="relative">
                        <input 
                            id="password" 
                            type="password" 
                            placeholder="Your password" 
                            class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label for="password" class="
                        absolute
                        left-3 
                        -top-6
                        text-slate-400
                        transition-all
                        peer-placeholder-shown:text-base 
                        peer-placeholder-shown:text-slate-400    
                        peer-placeholder-shown:top-6 
                        peer-focus:-top-6 
                        peer-focus:text-slate-400  
                        peer-focus:text-xl
                        select-none
                        pointer-events-none
                        ">Password</label>
                    </div>

                    <div>
                        <button class="py-4 px-6 bg-blue-500 text-slate-100 rounded-lg">Log in</button>
                    </div>

                    <div>
                        <p  class=" text-slate-400 text-xl">Don't have an account? 
                            <RouterLink :to="{'name': 'signup'}" class="group text-blue-500 transition-all duration-300 ease-in-out">
                                <span class="bg-left-bottom bg-gradient-to-r from-blue-500 to-blue-500 bg-[length:0%_2px] bg-no-repeat group-hover:bg-[length:100%_2px] transition-all duration-500 ease-out">
                                SIGN UP
                                </span>
                            </RouterLink>
                            
                        </p>
                    </div>
                </form>
            </div>
        </div>
        <Intro />
    </div>
    
</template>
<script>
import Intro from '../components/Intro.vue'

export default {
    name: 'FeedView',
    components: {
        Intro,
    }
}
</script>