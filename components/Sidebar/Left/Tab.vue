<template>
    <NuxtLink to="#">
        <div class="flex items-center p-3 w-min hover:bg-gray-200 dark:hover:bg-dim-200 text-black dark:text-white gap-4 rounded-full" :class="defaultTransition">

            <div class="h-4 w-4 text-dark" >
                <slot name="icon" />
            </div>

            <div class="hidden xl:block" :class="textClasses">
                <slot name="name" />
            </div>

        </div>
    </NuxtLink>
</template>
<script setup>
const { defaultTransition } = useTailwindConfig();
const props = defineProps({
    active: {
        type: Boolean,
        default: false
    }

})

const textClasses = computed(() => props.active ? 'font-semibold' : 'font-normal' )
</script>
