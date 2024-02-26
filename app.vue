<template>
  <div :class="{'dark' : darkmode}">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-10">
      
          <!-- Left-->
            <div class="hidden md:block xs:col-span-1 xl:col-span-2 min-w">
              <div class="sticky top-0">
                <SidebarLeft />
              </div>
            </div>

          <!-- Center-->

            <main class="col-span-12 md:col-span-8 xl:col-span-6">
              <NuxtPage />
            </main>

          <!-- Right-->

            <div class="hidden md:block col-span-12 md:col-span-3 xl:col-span-4 min-w">
              <div class="sticky top-0">
                <SidebarRight />
              </div>
            </div>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const darkmode = ref();
// darkmode.value = true
</script>