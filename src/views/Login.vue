<template>
    <div class="w-full max-w-md p-6 bg-white rounded-lg shadow-md">
        <h2 class="text-2xl font-bold text-center text-blue-900">Connexion à mon compte</h2>

        <form class="mt-6">
            <div class="mb-4">
                <label class="block text-gray-700 py-2">Adresse email</label>
                <input type="email" placeholder="Adresse email" class="w-full px-4 py-2 border rounded-md focus:ring-2 focus:ring-blue-400 focus:outline-none" required>
            </div>
            <div class="mb-4">
                <label class="block text-gray-700 py-2">Mot de passe</label>
                <div class="relative">
                    <input :type="showPassword ? 'text' : 'password'" placeholder="Mot de passe" class="w-full px-4 py-2 border rounded-md focus:ring-2 focus:ring-blue-400 focus:outline-none" />
                    <span class="absolute inset-y-0 right-3 flex items-center cursor-pointer"
                        @click="showPassword = !showPassword">
                        <EyeSlashIcon v-if="showPassword" class="w-6 h-6 text-gray-700" />
                        <EyeIcon v-else class="w-6 h-6 text-gray-700" />
                    </span>
                </div>
            </div>
            <a href="#" class="text-sm text-blue-600 hover:underline">Mot de passe oublié ?</a>
            <button class="w-full px-4 py-2 mt-4 text-white bg-blue-900 rounded-md hover:bg-blue-800 cursor-pointer">Je me connecte</button>
        </form>

        <div class="flex items-center my-6">
            <div class="flex-grow border-t border-gray-300"></div>
            <span class="mx-2 text-gray-600 bg-white p-2">Pas encore d'accès web ?</span>
            <div class="flex-grow border-t border-gray-300"></div>
        </div>

        <button class="w-full px-4 py-2 text-white bg-gray-700 rounded-md hover:bg-blue-800 cursor-pointer">Je crée mon compte Internet Desenfans</button>
    </div>
</template>

<script setup>
import { EyeIcon, EyeSlashIcon } from '@heroicons/vue/24/outline';
import { ref } from 'vue';

const showPassword = ref(false);
</script>