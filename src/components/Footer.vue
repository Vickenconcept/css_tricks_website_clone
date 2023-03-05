<template>
  <footer class="mb-12 relative bg-[#262626]">
    <svg
      class="bg-gradient-to-r stroke-red-600 from-[#ff7a18] via-[#af002d] after:to-[#319197] w-[110px] h-[110px]"
      viewBox="0 0 362.62 388.52"
      data-spin-me="false"
    >
      <path
        d="M156.58,239l-88.3,64.75c-10.59,7.06-18.84,11.77-29.43,11.77-21.19,0-38.85-18.84-38.85-40C0,257.83,14.13,244.88,27.08,239l103.6-44.74L27.08,148.34C13,142.46,0,129.51,0,111.85,0,90.66,18.84,73,40,73c10.6,0,17.66,3.53,28.25,11.77l88.3,64.75L144.81,44.74C141.28,20,157.76,0,181.31,0s40,18.84,36.5,43.56L206,149.52l88.3-64.75C304.93,76.53,313.17,73,323.77,73a39.2,39.2,0,0,1,38.85,38.85c0,18.84-12.95,30.61-27.08,36.5L231.93,194.26,335.54,239c14.13,5.88,27.08,18.83,27.08,37.67,0,21.19-18.84,38.85-40,38.85-9.42,0-17.66-4.71-28.26-11.77L206,239l11.77,104.78c3.53,24.72-12.95,44.74-36.5,44.74s-40-18.84-36.5-43.56Z"
      ></path>
    </svg>
    <form
      class="absolute right-12 top-16 w-[650px] border-transparent rounded-b-md p-6 bg-[#434343]"
      autocomplete="off"
      target=""
      action=""
      method="post"
    >
      <h2 class="text-orange-500 font-bold text-3xl mb-1">KEEP UP TO DATE ON WEB DEV</h2>
      <p class="text-white font-thin font-serif text-sm">
        with our hand-crafted newsletter
      </p>
      <input
        type="email"
        name="email"
        id="email"
        class="bg-gray-200 w-[470px] text-sm mr-4 mt-6 border-transparent p-4 rounded-sm"
      />
      <input
        type="submit"
        value="SUBSCRIBE"
        class="shadow-sm shadow-black border-transparent p-3 rounded-sm text-white font-bold bg-[#5a5a5a] hover:bg-[#434343]"
      />
    </form>
    <div class="bg-[#141313]">
      <div class="px-10 mb-4 py-10">
        <h1 class="font-serif text-2xl text-white">CSS-Tricks is powered by</h1>
        <a href="#" class="font-serif text-blue-600 text-2xl hover:text-blue-900"
          >DigitalOcean</a
        >
        <span class="text-white">.</span>
      </div>
      <div class="flex justify-start" id="footerLinks">
        <!-- links goes in here -->
        <ul v-for="link in links" class="px-10 pb-14">
          <li class="text-orange-500 font-bold uppercase">{{ link.linkDis }}</li>
          <li class="text-gray-400 font-serif hover:text-white text-xl font-extralight">
            <a href="#">{{ link.link1 }}</a>
          </li>
          <li class="text-gray-400 font-serif hover:text-white text-xl font-extralight">
            <a href="#">{{ link.link2 }}</a>
          </li>
          <li class="text-gray-400 font-serif hover:text-white text-xl font-extralight">
            <a href="#">{{ link.link3 }}</a>
          </li>
          <li class="text-gray-400 font-serif hover:text-white text-xl font-extralight">
            <a href="#">{{ link.link4 }}</a>
          </li>
          <li class="text-gray-400 font-serif hover:text-white text-xl font-extralight">
            <a href="#">{{ link.link5 }}</a>
          </li>
        </ul>
      </div>
    </div>
    <a href="#"></a>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          linkDis: "DIGITALOCEAN",
          link1: "DigitalOcean",
          link2: "DigitalOcean Community",
          link3: "About DigitalOcean",
          link4: "Legal",
          link5: "Free Credit Offer",
        },
        {
          linkDis: "CSS-TRICKS",
          link1: "Email",
          link2: "Guest Writing",
          link3: "Book",
          link4: "Advertizing",
          link5: "",
        },
        {
          linkDis: "follow",
          link1: "Mastodon",
          link2: "Guest Writing",
          link3: "Book",
          link4: "Advertizing",
          link5: "",
        },
        {
          linkDis: "",
          link1: "CodePen",
          link2: "iTunes",
          link3: "RSS",
          link4: "",
          link5: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
