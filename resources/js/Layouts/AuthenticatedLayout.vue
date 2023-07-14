<script setup>
import { ref } from 'vue';
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import Dropdown from '@/Components/Dropdown.vue';
import DropdownLink from '@/Components/DropdownLink.vue';
import NavLink from '@/Components/NavLink.vue';
import ResponsiveNavLink from '@/Components/ResponsiveNavLink.vue';
import { Link } from '@inertiajs/vue3';
import TopNavigation from "@/Components/TopNavigation.vue";
import SideNavigation from "@/Components/SideNavigation.vue";

const showingNavigationDropdown = ref(false);
</script>

<template>
<div class="min-h-screen bg-gray-100 flex flex-col">
    <header>
        <TopNavigation />
    </header>
    <div class="flex-1 flex">
        <SideNavigation class="w-1/5 min-h-full bg-red-500"/>
        <main class="w-full flex flex-col">
            <!-- Page Heading -->
            <header class="bg-white shadow" v-if="$slots.header">
                <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                    <slot name="header" />
                </div>
            </header>

            <!-- Page Content -->
            <div class="flex-1">
                <slot />
            </div>


            <footer>
                Footer
            </footer>
        </main>
    </div>

</div>



</template>
