<template>
    <div class="max-w-7xl mx-auto grid grid-cols-1 sm:grid-cols-2 gap-4">
        <div class="main-left">
            <div class="p-12 bg-slate-700 rounded-lg">
                <form class="space-y-8" v-on:submit.prevent="submitForm">
                    <div class="relative">
                        <input type="text" v-model="form.name" placeholder="Your full name" class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="absolute left-3 -top-6 text-slate-400 transition-all peer-placeholder-shown:text-base peer-placeholder-shown:text-slate-400 peer-placeholder-shown:top-6 peer-focus:-top-6 peer-focus:text-slate-400 peer-focus:text-xl select-none pointer-events-none">
                            Name</label>
                    </div>

                    <div class="relative">
                        <input type="email" v-model="form.email" placeholder="Your e-mail address" class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="absolute left-3 -top-6 text-slate-400 transition-all peer-placeholder-shown:text-base peer-placeholder-shown:text-slate-400 peer-placeholder-shown:top-6 peer-focus:-top-6 peer-focus:text-slate-400 peer-focus:text-xl select-none pointer-events-none">
                            E-mail</label>
                    </div>

                    <div class="relative">
                        <input type="password" v-model="form.password1" placeholder="Your password" class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="absolute left-3 -top-6 text-slate-400 transition-all peer-placeholder-shown:text-base peer-placeholder-shown:text-slate-400 peer-placeholder-shown:top-6 peer-focus:-top-6 peer-focus:text-slate-400 peer-focus:text-xl select-none pointer-events-none">
                            Password</label>
                    </div>

                    <div class="relative">
                        <input type="password" v-model="form.password2" placeholder="Repeat your password" class="peer w-full mt-2 py-4 px-3 border border-gray-200 rounded-lg placeholder-transparent">
                        <label class="absolute left-3 -top-6 text-slate-400 transition-all peer-placeholder-shown:text-base peer-placeholder-shown:text-slate-400 peer-placeholder-shown:top-6 peer-focus:-top-6 peer-focus:text-slate-400 peer-focus:text-xl select-none pointer-events-none">
                            Repeat password</label>
                    </div>
                    <template v-if="errors.length">
                        <div class="bg-red-300 text-white rounded-lg p-6">
                            <p v-for="error in errors" v-bind:key="error">{{ error }}</p>
                        </div>
                    </template>

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
import axios from 'axios'
import Intro from '../components/Intro.vue'
import { useToastStore } from '@/stores/toast'


export default {
    name: 'SignUpView',
    components: {
        Intro,
    },

    setup() {
        const toastStore = useToastStore()

        return {
            toastStore
        }
    },

    data() {
        return {
            form: {
                email: '',
                name: '',
                password1: '',
                password2: ''
            },
            errors: [],
        }
    },

    methods: {
        submitForm() {
            this.errors = []

            if (this.form.email === '') {
                this.errors.push('Your e-mail is missing')
            }

            if (this.form.name === '') {
                this.errors.push('Your name is missing')
            }

            if (this.form.password1 === '') {
                this.errors.push('Your password is missing')
            }

            if (this.form.password1 !== this.form.password2) {
                this.errors.push('The password does not match')
            }

            if (this.errors.length === 0) {
                axios
                    .post('api/signup/', this.form)
                    .then(response => {
                        if (response.data.message === 'success') {
                            this.toastStore.showToast(5000, 'The user is registered. Please log in', 'bg-emerald-500')

                            this.form.email = ''
                            this.form.name = ''
                            this.form.password1 = ''
                            this.form.password2 = ''
                        } else {
                            this.toastStore.showToast(5000, 'Something went wrong. Please try again', 'bg-red-300')
                        }
                    })
                    .catch(error => {
                        console.log('error', error)
                    })
            }
        }
    }
}
</script>