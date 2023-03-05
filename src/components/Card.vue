<template>
  <!-- popular article starts here -->
  <section class="bg-red grid grid-cols-12">
    <div class="col-span-3 px-4 mt-10 mr-1">
      <div class="bg-black text-white h-96 px-6 pt-[13rem] border rounded-xl">
        <h2 class="font-bold text-4xl font-sans">Popular <br />this <br />month</h2>
        <p class="header-card-sponsor font-serif font-extralight text-sm">
          Powered by
          <br />
          <a href="#" class="text-blue-700">DigitalOcean</a>
        </p>
      </div>
    </div>
    <!-- article cards -->
    <div
      class="col-span-9 flex pt-10 gap-4 overflow-x-auto h-[26rem] after:border-transparent after:rounded-md  relative after:h-[100%] after:p-[0.20rem] after:sticky after:right-0 after:scroll after:top-0 after:bg-gradient-to-b after:from-[#ff7a18] after:via-[#af002d] after:to-[#319197] "
      id="articleContainer"
    >
      <!-- article cards goes in here -->
      <article
        v-for="item in items"
        class="p-5 hover:rotate-12 h-80 w-[18rem] shadow-2xl shadow-black bg-gradient-to-r from-[#434343] to-[#262626] flex flex-col m-0 transition text-white border-transparent rounded-xl"
      >
        <time
          datetime="2023-01-25"
          title="Originally published Jan 25, 2023"
          class="font-[serif] font-bold text-gray-200 text-sm"
        >
          Article<span class="font-light"> {{ item.date }}</span>
        </time>
        <h3 class="">
          <a href="#" class="font-bold text-xl hover:text-gray-300">
            {{ item.title }}
          </a>
        </h3>
        <div
          class="font-extrabold text-[11px] mr-2 text-orange-500 font-[arial black] uppercase w-[17rem] mb-[8rem] mt-4"
        >
          <a href="#" class="mr-3">{{ item.link1 }}</a>
          <a href="#" class="mr-3">{{ item.link2 }}</a>
          <a href="#" class="mr-3">{{ item.link3 }}</a>
          <a href="#" class="mr-3">{{ item.link4 }}</a>
        </div>
        <div>
          <a href="#">
            <img
              alt=""
              :src="item.img"
              class="inline-block w-10 h-10 border-transparent rounded-full"
            />
          </a>
          <a class="author-name" href="#"> {{ item.name }}</a>
        </div>
      </article>
    </div>
  </section>
</template>

<script>
import { ref } from "vue";

export default {
  data() {
    return {
      html: "",
      items: [
        {
          date: "on Jan 25, 2023",
          title: "  Animating CSS Grid (How To + Examples)",
          link1: "animation",
          link2: "grid",
          link3: "grid-template-columns",
          link4: "grid-template-rows",
          img:
            "https://secure.gravatar.com/avatar/d4b0907c0d98a2394568d9bf9e8814c3?s=80&amp;d=retro&amp;r=pg",
          name: "Daniel Schwarz ",
        },
        {
          date: "on Jan 25, 2023",
          title: "  Animating CSS Grid (How To + Examples)",
          link1: "animation",
          link2: "grid",
          link3: "grid-template-columns",
          link4: "grid-template-rows",
          img:
            "https://secure.gravatar.com/avatar/1a1b5ca4b139c0c8caaea26ef437d943?s=80&d=retro&r=pg",
          name: "Daniel Schwarz ",
        },
        {
          date: "on Jan 25, 2023",
          title: "  Animating CSS Grid (How To + Examples)",
          link1: "animation",
          link2: "grid",
          link3: "grid-template-columns",
          link4: "grid-template-rows",
          img:
            "https://secure.gravatar.com/avatar/7ba2dc4a8a6c5c08b49bf00a55f322d7?s=80&amp;d=retro&amp;r=pg",
          name: "Daniel Schwarz ",
        },
        {
          date: "on Jan 25, 2023",
          title: "  Animating CSS Grid (How To + Examples)",
          link1: "animation",
          link2: "grid",
          link3: "grid-template-columns",
          link4: "grid-template-rows",
          img:
            "https://secure.gravatar.com/avatar/1a1b5ca4b139c0c8caaea26ef437d943?s=80&d=retro&r=pg",
          name: "Daniel Schwarz ",
        },
        {
          date: "on Jan 25, 2023",
          title: "  Animating CSS Grid (How To + Examples)",
          link1: "animation",
          link2: "grid",
          link3: "grid-template-columns",
          link4: "grid-template-rows",
          img:
            "https://secure.gravatar.com/avatar/2c12e74c8162614e08a31d704ed9e193?s=80&d=retro&r=pg",
          name: "Daniel Schwarz ",
        },
        {
          date: "on Jan 25, 2023",
          title: "  Animating CSS Grid (How To + Examples)",
          link1: "animation",
          link2: "grid",
          link3: "grid-template-columns",
          link4: "grid-template-rows",
          img:
            "https://secure.gravatar.com/avatar/8081b26e05bb4354f7d65ffc34cbbd67?s=80&d=retro&r=pg",
          name: "Daniel Schwarz ",
        },
      ],
    };
  },
};
</script>

<style></style>
