<script setup>
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";
import Article from "./components/Article.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Header />
  <main class="bg-[#262626] border border-t-2 border-b-0 border-black p-[3%]">
    <!-- first section in main begins-->
    <section class="bg-white px-6 py-7 border rounded-md grid grid-cols-3">
      <div class="col-span-1 pt-2">
        <a href="#">
          <img
            src="https://css-tricks.com/wp-content/uploads/2022/03/css-tricksdo-dark.svg"
            alt="DigitalOcean"
          />
        </a>
      </div>
      <div class="col-span-2 ml-8">
        <p class="font-[Cambria]">
          CSS-Tricks is powered by DigitalOcean. Make your site part of the leading
          solution for simple and scalable cloud-based hosting with a
          <a
            href="https://try.digitalocean.com/css-tricks/?utm_medium=content_acq&amp;utm_source=css-tricks&amp;utm_campaign=global_brand_ad_en&amp;utm_content=conversion_topbanner_leadingsolution"
            class="text-blue-500 hover:text-blue-400"
            ><em class="text-blue-500 hover:text-blue-400">free</em> $200 credit to get
            you started</a
          >!
        </p>
      </div>
    </section>
    <!-- first section in main ends here// article begins -->
    <article
      class="mt-8 border-0 rounded-md grid md:grid-cols-2 overflow-hidden relative sm:grid-row-2 bg-white"
    >
      <div class="relative">
        <a
          href="#"
          class="block max-md:h-[15rem] after:absolute after:top-0 after:left-0 md:after:h-[100%] md:after:w-[100%] max-md:after:h-[100%] max-md:after:w-[100%] after:mix-blend-screen after:bg-gradient-to-r after:from-[#ff7a18] after:via-[#af002d] after:to-[#319197] after:opacity-[.75] after:z-[2] after:pointer-events-none"
        >
          <img
            src="https://css-tricks.com/wp-content/uploads/2023/01/svelte-cache.png"
            class="object-cover w-full max-md:h-[100%] h-[35rem]"
            alt=""
          />
        </a>
      </div>
      <div class="p-[7%] max-md:p-[3%] w-full">
        <div
          class="font-extrabold text-[11px] mr-2 text-orange-500 font-[arial black] uppercase"
        >
          <a href="#" class="">cache</a>
          <a href="#" class="">svelte</a>
          <a href="#" class="">sveltekit</a>
        </div>
        <h1 class="text-[2.8rem] font-bold mb-5">
          <a href="#">Caching Data in SvelteKit</a>
        </h1>
        <!-- card content -->
        <div class="text-gray-600 font-serif">
          <p class="text-[1.2rem]">
            My previous post was a broad overview of SvelteKit where we saw what a great
            tool it is for web development. This post will fork off what we did there and
            dive into every developer’s favorite topic: caching. So, be sure to give my
            last post a read if you haven’t already. The code for […]
          </p>
        </div>
        <!-- author row -->
        <div class="mt-7">
          <a href="#">
            <img
              alt="Avatar"
              src="https://secure.gravatar.com/avatar/d4b0907c0d98a2394568d9bf9e8814c3?s=80&amp;d=retro&amp;r=pg"
              class="inline-block w-10 h-10 border rounded-full"
            />
          </a>
          <div class="font-serif inline-block text-sm">
            <a class="font-bold hover:text-gray-600" href="#">Adam Rackis </a>
            on
            <time datetime="" class="text-sm text-gray-600"> Feb 1, 2023 </time>
          </div>
        </div>
      </div>
    </article>
    <Card />
    <!-- articles card -->
    <section class="bg-red grid grid-cols-12 mb-7 max-md:grid-cols-1">
      <div class="col-span-9 mx-2 md:w-[100%]">
        <div
          class="grid max-md:grid-cols-1 max-md:w-full md:grid-cols-2 mb-10"
          id="articleCardHolder"
        >
          <!-- cards goes in here -->
        </div>
        <p
          class="text-md font-bold block mr-10 cursor-pointer bg-[#5e5e5e] text-white hover:bg-[#535252] hover:text-gray-400 p-4 border-transparent rounded-sm text-center"
        >
          KEEP BROWSING IN THE ARCHIVES
        </p>
      </div>
      <div class="hidden md:block col-span-3 ml-[5%] border-transparent rounded-xl"></div>
    </section>
    <Article />
    <Card />
  </main>
    <Footer />
</template>

<style></style>
