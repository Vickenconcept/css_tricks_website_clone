<template>
  <section class="bg-red grid grid-cols-12 mb-7 max-md:grid-cols-1">
    <div class="col-span-9 mx-2 md:w-[100%]">
      <div
        class="grid max-md:grid-cols-1 max-md:w-full md:grid-cols-2 mb-10"
        id="articleCardHolder"
      >
        <!-- cards goes in here -->

        <div
          v-for="card in cards"
          class="mr-[5%] border-transparent rounded-xl grid grid-row-2 overflow-hidden relative max-md:w-[100%]"
        >
          <article
            class="border-0 rounded-md mt-10 mr-5 grid overflow-hidden relative grid-row-2 bg-white"
          >
            <div class="relative">
              <a
                href="#"
                class="block max-md:h-[15rem] after:absolute after:top-0 after:left-0 md:after:h-[100%] md:after:w-[100%] max-md:after:h-[100%] max-md:after:w-[100%] after:mix-blend-screen after:bg-gradient-to-r after:from-[#ff7a18] after:via-[#af002d] after:to-[#319197] after:opacity-[.75] after:z-[2] after:pointer-events-none"
              >
                <img
                  :src="card.cardImg"
                  class="object-cover w-full max-md:h-[100%] h-[10rem]"
                  alt=""
                />
              </a>
            </div>
            <div class="p-[7%] max-md:p-[3%] w-full">
              <div
                class="font-extrabold text-[11px] text-orange-500 font-[arial black] uppercase"
              >
                <a href="#" class="hover:text-orange-300 mr-2">{{ card.nav1 }}</a>
                <a href="#" class="hover:text-orange-300 mr-2">{{ card.nav2 }}</a>
                <a href="#" class="hover:text-orange-300 mr-2">{{ card.nav3 }}</a>
                <a href="#" class="hover:text-orange-300 mr-2">{{ card.nav4 }}</a>
                <a href="#" class="hover:text-orange-300 mr-2">{{ card.nav5 }}</a>
                <a href="#" class="hover:text-orange-300 mr-2">{{ card.nav6 }}</a>
              </div>
              <h1 class="text-[1.5rem] font-extrabold mb-5 uppercase">
                <a href="#">{{ card.title }}</a>
              </h1>
              <!-- card content -->
              <div class="my-7">{{ card.additionalCont }}</div>
              <div class="text-gray-600 font-serif">
                <p class="text-base">{{ card.desc }}</p>
              </div>
              <!-- author row -->
              <div class="mt-7">
                <a href="#">
                  <img
                    alt="Avatar"
                    :src="card.authorImg"
                    class="inline-block w-10 h-10 border rounded-full"
                  />
                </a>
                <div class="font-serif inline-block text-sm">
                  <a class="font-bold hover:text-gray-600" href="#">{{
                    card.authorName
                  }}</a>
                  <span class="text-gray-600">on</span>
                  <time datetime="" class="text-sm text-gray-600">{{ card.time }}</time>
                </div>
              </div>
            </div>
          </article>
        </div>
      </div>
      <p
        class="text-md font-bold block mr-10 cursor-pointer bg-[#5e5e5e] text-white hover:bg-[#535252] hover:text-gray-400 p-4 border-transparent rounded-sm text-center"
      >
        KEEP BROWSING IN THE ARCHIVES
      </p>
    </div>
    <div class="hidden md:block col-span-3 ml-[5%] border-transparent rounded-xl"></div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          cardImg: "https://css-tricks.com/wp-content/uploads/2023/01/svelte-cache.png",
          title: "Caching Data in SvelteKit",
          additionalCont: ``,
          desc:
            "My previous post was a broad overview of SvelteKit where we saw what a great tool it is for web development. This post will fork off what we did there and dive into every developer’s favorite topic: caching. So, be sure to give my last post a read if you haven’t already. The code for […]",
          authorImg:
            "https://secure.gravatar.com/avatar/d4b0907c0d98a2394568d9bf9e8814c3?s=80&amp;d=retro&amp;r=pg",
          authorName: "Adam Rackis",
          time: "Feb 1, 2023 ",
          nav1: "cache",
          nav2: "svelte",
          nav3: "sveltekit",
          nav4: "",
          nav5: "",
          nav6: "",
        },
        {
          cardImg: "https://css-tricks.com/wp-content/uploads/2023/02/react-lemons.jpg",
          title: "Healthcare, Selling Lemons, and the Price of Developer Experience",
          additionalCont: ``,
          desc:
            "Every now and then, a one blog post is published and it spurs a reaction or response in others that are, in turn, published as blogs posts, and a theme starts to emerge. That’s what happened this past week and …",
          authorImg:
            "https://secure.gravatar.com/avatar/1a1b5ca4b139c0c8caaea26ef437d943?s=80&d=retro&r=pg",
          authorName: "Geoff Graham ",
          time: "Feb 9, 2023 ",
          nav1: "DX",
          nav2: "JAVASCRIPT FRAMEWORK",
          nav3: "THIRD-PARTY",
          nav4: "user",
          nav5: "TESTING",
          nav6: "ux",
        },
        {
          cardImg:
            "https://css-tricks.com/wp-content/uploads/2023/01/movable-background.png",
          title: "Moving Backgrounds",
          additionalCont: ``,
          desc:
            "We often think of background images as texture or something that provides contrast for legible content — in other words, not really content. If it was content, you’d probably reach for an <img> anyway, accessibility and whatnot. <br><br>But there are …",
          authorImg:
            "https://css-tricks.com/wp-content/uploads/2022/06/OIGzYSYs_400x400-80x80.jpg",
          authorName: "Saleh Mubashar ",
          time: "Feb 9, 2023 ",
          nav1: "animation",
          nav2: "BACKGROUND-IMAGE",
          nav3: "background-position",
          nav4: "",
          nav5: "",
          nav6: "",
        },
        {
          cardImg:
            "https://css-tricks.com/wp-content/uploads/2023/01/edge-devtools-selector-stats.png",
          title: "The truth about CSS selector performance",
          additionalCont: ` <div class=" uppercase font-bold inline text-white py-2 px-5 bg-[#5a5a5a] hover:bg-[#434343] shadow-sm shadow-black border-transparent rounded-sm">
                                    <a href="#" > direct link</a><span class="text-orange-700 font-extrabold text-2xl"> &#8594;</span>
                                    </div>`,
          desc:
            "Geez, leave it to Patrick Brosset to talk CSS performance in the most approachable and practical way possible. Not that CSS is always what’s gunking up the speed, or even the lowest hanging fruit when it comes to improving …",
          authorImg:
            "https://secure.gravatar.com/avatar/1a1b5ca4b139c0c8caaea26ef437d943?s=80&d=retro&r=pg",
          authorName: "Geoff Graham ",
          time: "Feb 12, 2023 ",
          nav1: "Devtools",
          nav2: "edge",
          nav3: "PERFORMANCE",
          nav4: "",
          nav5: "",
          nav6: "",
        },
        {
          cardImg:
            "https://css-tricks.com/wp-content/uploads/2023/02/featured-image-avatar.png",
          title: "A Fancy Hover Effect For Your Avatar",
          additionalCont: ``,
          desc:
            "Do you know that kind of effect where someone’s head is poking through a circle or hole? The famous Porky Pig animation where he waves goodbye while popping out of a series of red rings is the perfect example, and …",
          authorImg:
            "https://secure.gravatar.com/avatar/2c12e74c8162614e08a31d704ed9e193?s=80&d=retro&r=pg",
          authorName: "Temani Afif  ",
          time: "Feb 3, 2023 ",
          nav1: "GRADIENTS",
          nav2: "hover",
          nav3: "mask",
          nav4: "scale",
          nav5: "",
          nav6: "",
        },
        {
          cardImg:
            "https://css-tricks.com/wp-content/uploads/2016/09/art_3d_gotchas_2.png",
          title: "Animating CSS Grid (How To + Examples)",
          additionalCont: ``,
          desc:
            "I’m pleased to shine a light on the fact that the CSS grid-template-rows and grid-template-columns properties are now animatable in all major web browsers! Well, CSS Grid has technically supported animations for a long time, as it’s baked right …",
          authorImg:
            "https://secure.gravatar.com/avatar/7ba2dc4a8a6c5c08b49bf00a55f322d7?s=80&d=retro&r=pg",
          authorName: "Geoff Graham ",
          time: "Feb 9, 2023 ",
          nav1: "ANIMATION",
          nav2: "grid",
          nav3: "GRID-TEMPLATE-COLUMNS",
          nav4: "GRID-TEMPLATE-ROWS",
          nav5: "",
          nav6: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
