<script setup lang="ts">
import { ref } from "vue";
import { RiMenuFill } from "@remixicon/vue";

const isMenuOpen = ref(false);

const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
    <header class="header w-full" id="header">
        <nav class="nav container mt-3 mx-auto py-6 flex justify-between text-base font-semibold">
            <div class="Nav-logo">
                <a href="/" class="flex items-center justify-center">
                    <img src="../assets/vue.svg" alt="Vue Logo" />
                    <h2 class="ml-3 text-neutral-300 font-medium text-3xl">
                        IPI
                    </h2>
                </a>
            </div>
            <div class="flex items-center md:hidden">
                <RiMenuFill class="ri Hamburger text-3xl text-neutral-300" @click="toggleMenu" />
            </div>
            <!-- Force Vue-class Nav -->
            <div :class="['nav--menu', isMenuOpen ? 'block' : 'hidden', 'md:flex']">
                <ul class="nav--list flex flex-col md:flex-row gap-10 md:gap-5 items-center text-neutral-300">
                    <li class="nav--item">
                        <a href="#app">
                            Home
                        </a>
                    </li>
                    <li class="nav--item">
                        <a href="#advantages">
                            Advantages
                        </a>
                    </li>
                    <li class="nav--item">
                        <a href="#platform">
                            Platform
                        </a>
                    </li>
                    <li class="nav--item">
                        <a href="#coins">
                            Coins
                        </a>
                    </li>
                    <li class="nav--item">
                        <a href="https://scan.ipi.io">
                            Scan
                        </a>
                    </li>
                    <li class="nav--item">
                        <a href="#contact">
                            Contact
                        </a>
                    </li>
                    <li class="nav--item">
                        <a href="https://wallet.ipi.io">
                            <button class="border-solid border-2 border-red-600 px-6 py-2 rounded-3xl text-base font-semibold">
                                WALLET
                            </button>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<style scoped>
.header {
    background-color: #0f1932;
    position: sticky;
    top: 0;
    left: 0;
    z-index: 1000;
}

/* Responsive Menu for mobile */
.nav--menu.hidden {
    display: none;
}

.nav--menu.block {
    display: block;
}

@media (max-width: 767px) {
    header {
        padding-top: 0.75rem;
    }
    .nav--list {
        gap: 1rem;
        flex-direction: column;
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        width: 100vw;
        background-color: #0f1932;
        padding: 1rem;
        z-index: 1000;
    }
    .Hamburger {
        cursor: pointer;
        position:absolute;
        right:0;
        margin-right:1rem;
    }
}

@media (min-width: 768px) {
    .nav--menu {
        display: flex !important; 
    }
    .nav--list {
        flex-direction: row;
        position: static;
        background-color: transparent;
        padding: 0;
    }
}
</style>
