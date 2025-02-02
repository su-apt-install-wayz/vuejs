<template>
    <div class="w-full max-w-md p-6 bg-white rounded-lg shadow-md">
        <h2 class="text-2xl font-bold text-center text-blue-900">Connexion à mon compte</h2>

        <form class="mt-8 flex flex-col gap-5">
            <div class="flex flex-col gap-2">
                <label for="email" class="block text-sm font-medium text-gray-900">Adresse email</label>
                <div class="relative">
                    <div class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none">
                        <AtSymbolIcon class="w-5 h-5 text-gray-500" />
                    </div>
                    <input type="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5" placeholder="Votre email" required>
                </div>
            </div>

            <div class=" flex flex-col gap-2">
                <label for="password" class="block text-sm font-medium text-gray-900">Mot de passe</label>
                <div class="relative">
                    <div class="absolute inset-y-0 left-0 flex items-center pl-3.5 pointer-events-none">
                        <LockClosedIcon class="w-5 h-5 text-gray-500" />
                    </div>
                    <input :type="showPassword ? 'text' : 'password'" id="password" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5" placeholder="Votre mot de passe" required>
                    <div class="absolute inset-y-0 right-3 flex items-center cursor-pointer"
                        @click="showPassword = !showPassword">
                        <EyeSlashIcon v-if="showPassword" class="w-5 h-5 text-gray-500" />
                        <EyeIcon v-else class="w-5 h-5 text-gray-500" />
                    </div>
                </div>
            </div>

            <a href="#" class="text-sm text-blue-600 hover:underline">Mot de passe oublié ?</a>
            <button class="w-full px-4 py-2 mt-4 text-white bg-blue-900 rounded-lg hover:bg-blue-800 cursor-pointer">Je me connecte</button>
        </form>

        <div class="flex items-center my-6">
            <div class="flex-grow border-t border-gray-300"></div>
            <span class="mx-2 text-gray-600 bg-white">Pas encore d'accès web ?</span>
            <div class="flex-grow border-t border-gray-300"></div>
        </div>

        <button class="w-full px-4 py-2 text-white bg-gray-700 rounded-lg hover:bg-blue-800 cursor-pointer">Je crée mon compte Internet Desenfans</button>
    </div>
</template>

<script setup>
import { EyeIcon, EyeSlashIcon, AtSymbolIcon, LockClosedIcon } from '@heroicons/vue/24/outline';
import { ref } from 'vue';

const showPassword = ref(false);
</script>