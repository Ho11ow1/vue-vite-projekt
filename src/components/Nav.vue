<script setup>

</script>


<template>
<!--                                                                  PRIME BLOCKS NAV IS BAD                                                        -->
<div class="bg-indigo-900 py-3 px-6 shadow-2 flex align-items-center justify-content-between relative lg:static">
    <a v-ripple class="cursor-pointer block lg:hidden text-white mt-1 p-ripple"
        v-styleclass="{ selector: '@next', enterClass: 'hidden', leaveToClass: 'hidden', hideOnOutsideClick: true }">
        <i class="pi pi-bars text-4xl"></i>
    </a>
    <div class="align-items-center flex-grow-1 lg:justify-content-end hidden lg:flex absolute lg:static w-full bg-indigo-900 left-0 top-100 px-6 lg:px-0 z-3 shadow-2 lg:shadow-none">
        <ul class="end list-none p-0 m-0 flex lg:align-items-center text-white select-none flex-column lg:flex-row cursor-pointer items-center">
            <li class="relative">
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <span>Advantages</span>
                </a>
            </li>
            <li>
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <span>Platform</span>
                </a>
            </li>
            <li>
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <span>Ecosystem</span>
                </a>
            </li>
            <li>
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <span>Coins</span>
                </a>
            </li>
            <li>
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <span>Scan</span>
                </a>
            </li>
            <li>
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <span>Contact</span>
                </a>
            </li>
            <li>
                <a v-ripple class="flex px-0 lg:px-4 py-3 hover:text-indigo-100 font-medium transition-colors transition-duration-150 p-ripple">
                    <button label="WALLET" class="border-solid border-2 border-red-600 text-gray-100 text-base font-medium rounded-3xl px-4 py-1">
                        WALLET
                    </button>
                </a>
            </li>
        </ul>
    </div>
</div>

</template>

<style scoped>

.end{
    margin-left:auto;
}

</style>