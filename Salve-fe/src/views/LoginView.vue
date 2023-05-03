<template>
    <div class="max-w-7xl mx-auto grid grid-cols-2 gap-4">
        <div class="main-left">
            <div class="p-12 bg-slate-700 rounded-lg">
                <form class="space-y-6">
                    <div>
                        <label class="text-slate-400 text-xl">E-mail</label><br>
                        <input type="email" placeholder="Your e-mail address" class="w-full mt-2 py-4 px-6 border border-gray-200 rounded-lg">
                    </div>

                    <div>
                        <label class="text-slate-400 text-xl">Password</label><br>
                        <input type="password" placeholder="Your password" class="w-full mt-2 py-4 px-6 border border-gray-200 rounded-lg">
                    </div>

                    <div>
                        <button class="py-4 px-6 bg-blue-500 text-slate-100 rounded-lg">Log in</button>
                    </div>

                    <div>
                        <p  class=" text-slate-400 text-xl">Don't have an account? <RouterLink :to="{'name': 'signup'}" class="underline">Click here</RouterLink> to create one!</p>
                    </div>
                </form>
            </div>
        </div>
        <div class="pt-40 main-right">
            <h1 class="py-1 px-12 font-mono font-bold text-slate-400 text-2xl tracking-tight">S A L V E</h1>
            <div class="py-1 px-12 bg-slate-900 text-slate-400 text-xl"> 
                Connect with other tech enthusiasts around the world on Salve.
            </div>
        </div>
    </div>
    
</template>