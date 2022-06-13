<script setup>
const generals = [
  {
    name: "HTML",
    img_url: "/HTML.svg",
  },
  {
    name: "CSS",
    img_url: "/CSS3.svg",
  },
  {
    name: "JS",
    img_url: "JS.png",
  },

  {
    name: "Node.js",
    img_url: "Node.svg",
  },

  {
    name: "Git",
    img_url: "git.png",
  },
];

const frameworks = [
  {
    name: "Vue, Nuxt",
    img_url: "Vue.svg",
  },
  {
    name: "React",
    img_url: "React.svg",
  },
];

const databases = [
  {
    name: "MySQL",
    img_url: "mysql.png",
  },
  {
    name: "MongoDB",
    img_url: "MongoDB.svg",
  },
  {
    name: "Firebase",
    img_url: "Firebase.svg",
  },
];

const backends = [
  {
    name: "C#",
    img_url: "C.svg",
  },
  {
    name: "ASP.NET",
    img_url: "Net.svg",
  },
];

const cmss = [
  {
    name: "Umbraco",
    img_url: "Umbraco.png",
  },
  {
    name: "Drupal",
    img_url: "Drupal.svg",
  },

  {
    name: "WordPress",
    img_url: "WordPress.svg",
  },
];

const mobiles = [
  {
    name: "Kotlin",
    img_url: "Kotlin.svg",
  },
];
</script>

<template>
  <div class="">
    <Navbar />
    <div class="frame text-white">
      <div class="lg:flex">
        <div class="">
          <img
            class="inline-block w-72 h-72 object-cover rounded-full"
            src="/portrait.jpg"
            alt=""
          />
          <div class="mt-5 space-y-1">
            <a
              href="https://www.linkedin.com/in/joshbmdev/" target="_blank"
              class="flex space-x-2 items-center"
            >
              <span>
                <i
                  class="fa-brands fa-linkedin cursor-pointer hover:text-slate-300 text-2xl"
                ></i>
              </span>
              <span>joshbmdev</span>
            </a>

            <a
              href="https://github.com/josh-bm" target="_blank"
              class="flex space-x-2 items-center"
            >
              <span
                ><i
                  class="fa-brands fa-github cursor-pointer hover:text-slate-300 text-2xl"
                ></i
              ></span>
              <span>josh-bm</span>
            </a>
            <a
              href="mailto:joshuabacuriomercado@gmail.com" target="_blank"
              class="flex space-x-2 items-center"
            >
              <span
                ><i
                  class="fa-solid fa-envelope cursor-pointer hover:text-slate-300 text-2xl"
                ></i
              ></span>
              <span>joshuabacuriomercado@gmail.com</span>
            </a>
          </div>
        </div>
        <div class="lg:pl-24 space-y-5 mt-5 lg:mt-0">
          <h2 class="text-2xl">About me</h2>
          <p class="text-lg">
            My name is Joshua and I'm a Multimedia Designer that is currently
            finishing a PBA in Web Development. I love coding and creating
            websites.
          </p>
          <p class="text-lg">
            I am a quick learner and love learning new things when it comes to
            coding. I can work independently but I am also team oriented and
            easily get along with others in a team setting.
          </p>
          <a
            href="/Joshua Bacurio Mercado - CV.pdf"
            class="cursor-pointer inline-flex items-center px-4 py-2.5 text-base rounded-lg shadow-lg border border-transparent bg-teal-600 hover:bg-teal-700 focus:outline-none"
            download
            >Download my CV</a
          >
        </div>
      </div>

      <div class="mt-28">
        <h2 class="text-3xl mb-10 text-center">Skills</h2>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-20">
          <div class="space-y-3 text-center">
            <h2 class="text-xl">General</h2>
            <div class="grid grid-cols-2">
              <div
                v-for="general in generals"
                :key="general.name"
                class="space-y-5"
              >
                <img :src="general.img_url" class="h-14 w-14 mx-auto" alt="" />
                <p>{{ general.name }}</p>
              </div>
            </div>
          </div>

          <div class="space-y-3 text-center">
            <h2 class="text-xl">JS Frameworks</h2>
            <div class="grid grid-cols-2">
              <div
                v-for="framework in frameworks"
                :key="framework.name"
                class="space-y-5"
              >
                <img :src="framework.img_url" class="h-14 w-14 mx-auto" alt="" />
                <p>{{ framework.name }}</p>
              </div>
            </div>
          </div>

          <div class="space-y-3 text-center">
            <h2 class="text-xl">Database</h2>
            <div class="grid grid-cols-2">
              <div
                v-for="database in databases"
                :key="database.name"
                class="space-y-5"
              >
                <img :src="database.img_url" class="h-14 w-14 mx-auto" alt="" />
                <p>{{ database.name }}</p>
              </div>
            </div>
          </div>

          <div class="space-y-3 text-center">
            <h2 class="text-xl">Backend</h2>
            <div class="grid grid-cols-2">
              <div
                v-for="backend in backends"
                :key="backend.name"
                class="space-y-5"
              >
                <img :src="backend.img_url" class="h-14 w-14 mx-auto" alt="" />
                <p>{{ backend.name }}</p>
              </div>
            </div>
          </div>

          <div class="space-y-3 text-center">
            <h2 class="text-xl">CMS</h2>
            <div class="grid grid-cols-2">
              <div v-for="cms in cmss" :key="cms.name" class="space-y-5">
                <img :src="cms.img_url" class="h-14 w-14 mx-auto" alt="" />
                <p>{{ cms.name }}</p>
              </div>
            </div>
          </div>

          <div class="space-y-3 text-center">
            <h2 class="text-xl">Mobile App</h2>
            <div class="grid grid-cols-2">
              <div
                v-for="mobile in mobiles"
                :key="mobile.name"
                class="space-y-5"
              >
                <img :src="mobile.img_url" class="h-14 w-14 mx-auto" alt="" />
                <p>{{ mobile.name }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
