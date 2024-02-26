<template>
    <div>
        <SidebarRightCardView title="What's Happening">
            <SidebarRightCardViewItem v-for="whatsHappening in whatsHappeningItems">
                <div>
                    <h1 class="font-bold text-base text-gray-800">{{ whatsHappening.title }}</h1>

                    <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
                </div>
            </SidebarRightCardViewItem>
        </SidebarRightCardView>

        <SidebarRightCardView title="Who to Follow"> 
            <SidebarRightCardViewItem v-for="whoToFollow in whoToFollowItems">
                <div class="flex justify-between p-2 items-center">
                    <div class="flex">
                        <img class="h-10 w-10 rounded-full" :src="whoToFollow.image" alt="whoToFollow.name">

                        <div class="flex flex-col px-2">
                            <h1 class="text-gray-900 font-bold text-sm dark:text-white">{{ whoToFollow.name }}</h1>
                            <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
                        </div>
                    </div>

                    <div class="flex h-full">
                        <button class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full hover:bg-white hover:text-black">Follow</button>
                    </div>
                </div>
            </SidebarRightCardViewItem>
        </SidebarRightCardView>

    </div>
</template>

<script setup>
const whatsHappeningItems = ref([
    {
        title: 'SpaceX',
        count: '11.7m tweets'
    },
    {
        title: '#CodingIsfun',
        count: '9.3k tweets'
    },
    {
        title: '#ArtforAll',
        count: '2.5k tweets'
    }
])

const whoToFollowItems = ref([
    {
        name: 'James Mark',
        handle: '@markkyng',
        image: 'https://picsum.photos/200/200'
    },
    {
        name: 'Johhny English',
        handle: '@johnny',
        image: 'https://picsum.photos/200/200'
    },
    {
        name: 'Sophia Richie',
        handle: '@msophyrich',
        image: 'https://picsum.photos/200/200'
    }
])
</script>