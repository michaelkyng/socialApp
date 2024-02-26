<template>
    <div class="flex flex-col h-screen">


        <div class="p-1 my-2 rounded-full hover:bg-blue-50 dark:hover:bg-white/20 w-min" :class="defaultTransition">
            <NuxtLink to="/">
                <div class="w-min h-min">
                    <LogoSocial />
                </div>
            </NuxtLink>
        </div>
        
        <div class="mt-4 space-y-3">

            <SidebarLeftTab active>
                <template #icon>
                    <HomeIcon/>
                </template>


                <template #name>
                    Home
                </template>
            </SidebarLeftTab>


            <SidebarLeftTab>
                <template #icon>
                    <HashtagIcon />
                </template>


                <template #name>
                    Explore
                </template>
            </SidebarLeftTab>

            <SidebarLeftTab>
                <template #icon>
                    <BellIcon />
                </template>


                <template #name>
                    Notifications
                </template>
            </SidebarLeftTab>

            <SidebarLeftTab>
                <template #icon>
                    <InboxIcon />
                </template>


                <template #name>
                    Messages
                </template>
            </SidebarLeftTab>

            <SidebarLeftTab>
                <template #icon>
                    <BookmarkIcon/>
                </template>


                <template #name>
                    BookMarks
                </template>
            </SidebarLeftTab>

            <SidebarLeftTab>
                <template #icon>
                    <DocumentTextIcon />
                </template>


                <template #name>
                    Lists
                </template>
            </SidebarLeftTab>

            <SidebarLeftTab>
                <template #icon>
                    <UserIcon />
                </template>


                <template #name>
                    Profile
                </template>
            </SidebarLeftTab>

            <SidebarLeftTab>
                <template #icon>
                    <DotsCircleHorizontalIcon />
                </template>


                <template #name>
                    More
                </template>
            </SidebarLeftTab>
        </div>
    </div>
</template>

<script setup>
import { HomeIcon } from "@heroicons/vue/solid";
import {  HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, DotsCircleHorizontalIcon } from "@heroicons/vue/outline";
const { defaultTransition } = useTailwindConfig();

</script>