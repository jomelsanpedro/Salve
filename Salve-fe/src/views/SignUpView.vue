<template>
    <div class="max-w-7xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-4">
        <div class="main-left">
            <div class="p-12 bg-slate-700 rounded-lg">
                <form class="space-y-8">
                    <div class="relative">
                        <input 
                            type="text" 
                            placeholder="Your full name" 
                            class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="
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
                            ">Name</label><br>
                    </div>

                    <div class="relative">
                        <input
                            type="email" 
                            placeholder="Your e-mail address" 
                            class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="
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
                            ">E-mail</label><br>
                    </div>

                    <div class="relative">
                        <input 
                            type="password" 
                            placeholder="Your password" 
                            class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="
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
                            ">Password</label><br>
                    </div>

                    <div class="relative">
                        <input 
                            type="password" 
                            placeholder="Repeat your password" 
                            class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="
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
                            ">Repeat password</label><br>
                    </div>

                    <div>
                        <button class="py-4 px-6 bg-blue-500 text-slate-100 rounded-lg">Sign up</button>
                    </div>
                    <div>
                        <p  class=" text-slate-400 text-xl">Already have an account? 
                            <RouterLink :to="{'name': 'login'}" class="group text-blue-500 transition-all duration-300 ease-in-out">
                                <span class="bg-left-bottom bg-gradient-to-r from-blue-500 to-blue-500 bg-[length:0%_2px] bg-no-repeat group-hover:bg-[length:100%_2px] transition-all duration-500 ease-out">LOG IN</span>
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