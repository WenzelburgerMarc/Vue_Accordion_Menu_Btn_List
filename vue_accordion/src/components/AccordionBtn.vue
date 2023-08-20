<template>
    <div class="w-full m-0 p-0 pointer-events-none overflow-hidden">
        <div class="main-container pointer-events-auto bg-gray-300 dark:bg-gray-500 p-3 rounded-xl flex justify-start items-center hover:cursor-pointer overflow-hidden"
            @click="isOpen = !isOpen">
            <i class="bx bx-money icon text-3xl"
                :class="isOpen ? 'text-black dark:text-white' : 'text-gray-400 dark:text-gray-300'"></i>
            <div class="title text-lg ml-3 truncate"
                :class="isOpen ? 'text-black dark:text-white' : 'text-gray-400 dark:text-gray-300'">Payments</div>
            <i class="bx bx-chevron-right icon chevron text-3xl ml-auto"
                :class="isOpen ? 'open text-black dark:text-white' : 'text-gray-400 dark:text-gray-300'"></i>
        </div>
        <ul class="h-auto w-auto z-0">
            <AccordionItem title="Income" :actionEvent="() => { console.log('Income') }" :isOpen="isOpen" />
            <AccordionItem title="Expenses" :actionEvent="() => { console.log('Expenses') }" :isOpen="isOpen" />
            <AccordionItem title="Savings" :actionEvent="() => { console.log('Savings') }" :isOpen="isOpen"
                :isLastElement="true" />
        </ul>
    </div>
</template>
<script lang="ts">
import AccordionItem from './AccordionItem.vue';
export default {
    name: 'AccordionBtn',
    components: {
        AccordionItem
    },
    data() {
        return {
            isOpen: false
        }
    },

}
</script>
<style scoped>
.icon,
.title {
    transition: all 0.25s ease-in-out;
}

.chevron.open {
    transform: rotate(-90deg);
}

.main-container:hover .icon,
.main-container:hover .title {
    color: black;
}

.dark .main-container:hover .icon,
.dark .main-container:hover .title {
    color: white;
}
</style>