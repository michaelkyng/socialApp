<template>
    <div class="flex flex-col">
        
        <div class="m-2 border rounded-xl bg-gray-50 dark:bg-dim-700 overflow-hidden" :class="twitterBorderColor">
            <h1 class="p-3 text-lg font-bold text-gray-900 dark:text-white border-b"
            :class="twitterBorderColor">{{ props.title }}</h1>
            <slot></slot>

            <div class="p-3 text-sm text-blue-500 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300" :class="defaultTransition">
                Show More
            </div>
        </div>

    </div>
</template>


<script setup>
const { twitterBorderColor, defaultTransition } = useTailwindConfig();
const props =   defineProps({
        title : {
            type : String,
            required : true
        }
    })
</script>