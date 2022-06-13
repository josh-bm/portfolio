<template>
  <div>
    <a :href="projectData.url" target="_blank" external>
      <div class="bg-white cursor-pointer rounded-lg shadow-lg hover:shadow-xl hover:scale-105">
            <img :src="projectData.img_url" class="rounded-t-lg h-72 object-cover mx-auto" />
        <div class="text-black px-2.5 py-4 h-40 space-y-2 flex flex-col">
          <h2 class="font-medium">{{ projectData.title }}</h2>
          <p class="">{{ projectData.description }}</p>

          <div class="flex space-x-1 pt-5 self-end items-end">
          <div v-for="tag in projectData.tags">
            <span class="bg-teal-700 p-2 rounded-lg text-white text-xs">{{tag.name}}</span>
          </div>
          </div>
          <slot></slot>
          <slot name="button"></slot>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: ["projectData"],
};
</script>


<!-- <div v-for="project in projects" :key="project.name">
          <div
            class="max-w-sm rounded-lg overflow-hidden shadow-lg hover:shadow-xl border bg-white"
          >
            <nuxt-link to="/project">
              <div class="relative w-full">
                <figure class="w-full mx-auto">
                  <img
                    class="w-full h-80 scale-75 hover:scale-90 object-cover"
                    :src="project.imageSrc"
                    alt=""
                  />
                </figure>
                <div class="absolute top-2 right-2 flex items-center">
                  <span
                    class="bg-green-600 rounded-full px-2 py-1 font-semibold text-white cursor-help"
                    title="Eachthing Sustainability Score"
                    >{{ project.score }}</span
                  >
                </div>
              </div>

              <div class="p-5">
                <div class="space-y-2">
                  <span class="block font-bold text-xl">
                    {{ project.brand }}
                  </span>

                  <span class="block font-semibold text-lg">
                    {{ project.name }}
                  </span>

                  <span class="block text-sm">
                    {{ project.category }}
                  </span>
                </div>

                <div class="flex justify-between">
                  <div class="font-bold">{{ project.price }} kr.</div>
                  <div></div>
                  <div
                    class="flex items-center cursor-help"
                    title="230 anmeldelser"
                  >
                    <span class="material-symbols-outlined text-yellow-400">
                      star
                    </span>
                    <span class="material-symbols-outlined text-yellow-400">
                      star
                    </span>
                    <span class="material-symbols-outlined text-yellow-400">
                      star
                    </span>
                    <span class="material-symbols-outlined text-yellow-400">
                      star
                    </span>
                    <span class="material-symbols-outlined text-yellow-400">
                      star
                    </span>
                  </div>
                </div>
                <div class="pt-4 flex flex-wrap">
                  <span
                    v-for="tag in project.tags"
                    class="inline-block bg-gray-200 rounded-full px-2.5 py-2 text-xs font-semibold text-gray-700 mr-2 mb-2"
                    >#{{ tag.name }}</span
                  >
                </div>
              </div>
            </nuxt-link>
          </div>
        </div> -->
