<script></script>

<template>
  <div>
    <Navbar />
    <div class="flex items-center justify-center frame lg:pt-10">
      <div class="w-full lg:flex lg:space-x-10 lg:items-center text-white">
        <div class="w-full">
          <figure class="w-full">
            <img src="/banner.png" class="w-full" alt="" />
          </figure>
        </div>
        <div class="text-center lg:w-full">
          <p class="text-cyan-300 text-xl lg:text-lg xl:text-2xl">
            Hi, my name is
          </p>
          <h2 class="text-3xl lg:text-2xl xl:text-4xl mt-1">
            Joshua Bacurio Mercado
          </h2>
          <p class="text-xl lg:text-lg mt-3">
            <span>Web Developer</span> | <span>Multimedia designer</span>
          </p>
          <div class="flex space-x-5 mt-5 justify-center">
            <nuxt-link to="/projects">
              <span
                class="cursor-pointer inline-flex items-center px-6 py-2.5 text-lg lg:text-sm xl:text-lg rounded-lg shadow-lg border border-transparent bg-teal-600 hover:bg-teal-700 focus:outline-none"
                >My work</span
              >
            </nuxt-link>

            <nuxt-link to="/about">
              <span
                class="cursor-pointer inline-flex items-center px-6 py-2.5 text-lg lg:text-sm xl:text-lg rounded-lg shadow-lg border border-teal-600 text-teal-600 bg-transparent hover:bg-teal-700 hover:border-transparent hover:text-white focus:outline-none"
                >Get in touch</span
              >
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>
