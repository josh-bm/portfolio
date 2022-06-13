<template>
  <Popover class="relative bg-slate-800 shadow-lg mb-10">
    <div
      class="flex justify-between items-center py-6 md:justify-start md:space-x-10 frame"
    >
      <!-- Logo -->
      <div>
        <nuxt-link to="/" class="flex">
          <span class="text-4xl text-white logo">J</span>
        </nuxt-link>
      </div>
      <div class="-mr-2 -my-2 md:hidden">
        <PopoverButton
          class="rounded-md p-2 inline-flex items-center justify-center text-white hover:text-gray-500 hover:bg-gray-100 focus:outline-none"
        >
          <span class="sr-only">Open menu</span>
          <MenuIcon class="h-6 w-6" aria-hidden="true" />
        </PopoverButton>
      </div>
      <!-- Menu items -->
      <div class="hidden md:flex-1 md:flex md:items-center md:justify-between">
        <PopoverGroup as="nav" class="flex space-x-10 text-white">
          <nuxt-link to="/projects" class="text-base font-medium hover:text-cyan-300">
            Projects
          </nuxt-link>
          <nuxt-link to="/about" class="text-base font-medium hover:text-cyan-300">
            About
          </nuxt-link>
        </PopoverGroup>
        <div class="flex items-center space-x-10 text-white">
          <a
            href="https://www.linkedin.com/in/joshbmdev/"
            target="_blank"
            class="flex space-x-2 items-center"
          >
            <span>
              <i
                class="fa-brands fa-linkedin cursor-pointer hover:text-slate-300 text-4xl"
              ></i>
            </span>
          </a>

          <a
            href="https://github.com/josh-bm"
            target="_blank"
            class="flex space-x-2 items-center"
          >
            <span
              ><i
                class="fa-brands fa-github cursor-pointer hover:text-slate-300 text-4xl"
              ></i
            ></span>
          </a>
        </div>
      </div>
    </div>

    <transition
      enter-active-class="duration-200 ease-out"
      enter-from-class="opacity-0 scale-95"
      enter-to-class="opacity-100 scale-100"
      leave-active-class="duration-100 ease-in"
      leave-from-class="opacity-100 scale-100"
      leave-to-class="opacity-0 scale-95"
    >
      <PopoverPanel
        focus
        class="absolute top-0 inset-x-0 transition transform origin-top-right md:hidden"
      >
        <div
          class="rounded-lg shadow-lg bg-slate-800 divide-y-2 divide-gray-50 "
        >
          <div class="pt-5 pb-6 px-5">
            <div class="flex items-center justify-between">
              <div>
                <nuxt-link to="/" class="flex">
                  <span class="text-4xl logo  text-white">J</span>
                </nuxt-link>
              </div>
              <div class="-mr-2">
                <PopoverButton
                  class="rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                >
                  <span class="sr-only">Close menu</span>
                  <XIcon class="h-6 w-6" aria-hidden="true" />
                </PopoverButton>
              </div>
            </div>
            <div class="mt-6">
              <nav class="grid gap-6">
                <a
                  v-for="item in solutions"
                  :key="item.name"
                  :href="item.href"
                  class="-m-3 p-3 flex items-center rounded-lg hover:bg-slate-700"
                >
                  <div
                    class="flex-shrink-0 flex items-center justify-center h-10 w-10 rounded-md bg-teal-600 text-white"
                  >
                    <component
                      :is="item.icon"
                      class="h-6 w-6"
                      aria-hidden="true"
                    />
                  </div>
                  <div class="ml-4 text-base font-medium text-white">
                    {{ item.name }}
                  </div>
                </a>
              </nav>
            </div>
          </div>
          <div class="py-6 px-5">
            <div class="flex items-center space-x-5 text-white">
              <a
                href="https://www.linkedin.com/in/joshbmdev/"
                target="_blank"
                class="flex space-x-2 items-center"
              >
                <span>
                  <i
                    class="fa-brands fa-linkedin cursor-pointer hover:text-teal-600 text-4xl"
                  ></i>
                </span>
              </a>

              <a
                href="https://github.com/josh-bm"
                target="_blank"
                class="flex space-x-2 items-center"
              >
                <span
                  ><i
                    class="fa-brands fa-github cursor-pointer hover:text-teal-600 text-4xl"
                  ></i
                ></span>
              </a>
            </div>
          </div>
        </div>
      </PopoverPanel>
    </transition>
  </Popover>
</template>

<script setup>
import {
  Popover,
  PopoverButton,
  PopoverGroup,
  PopoverPanel,
} from "@headlessui/vue";
import {
  MenuIcon,
  XIcon,
  FolderIcon,
  IdentificationIcon,
} from "@heroicons/vue/outline";
import { ChevronDownIcon } from "@heroicons/vue/solid";

const solutions = [
  {
    name: "Projects",
    description:
      "Get a better understanding of where your traffic is coming from.",
    href: "/projects",
    icon: FolderIcon,
  },
  {
    name: "About",
    description: "Speak directly to your customers in a more meaningful way.",
    href: "/about",
    icon: IdentificationIcon,
  },
];
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Sacramento&display=swap");

.logo {
  font-family: "Sacramento", cursive;
}
</style>
