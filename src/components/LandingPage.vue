<template>
  <div class="hello container mx-auto text-center">
    <img class="mx-auto" alt="sjf logo" src="../assets/head.jpeg" />
    <h1 class="text-4xl">{{ msg }}</h1>
    <p>Web Developer from Minneapolis.</p>
    <ul class="my-4">
      <li class="inline mx-2" v-for="link in links" v-bind:key="link.name">
        <a class="text-purple-500 hover:text-purple-700 focus:text-purple-700" v-bind:href="link.href" target="_blank" rel="noopener">{{link.name}}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "LandingPage",
  props: {
    msg: String
  },
  data() {
    return {
      links: [
        {
          name: "gmail",
          href: "mailto:sam.j.fortin@gmail.com"
        },
        {
          name: "github",
          href: "https://github.com/sjfortin"
        },
        {
          name: "linked",
          href: "https://linkedin.com/sjfortin"
        },
        {
          name: "codepen",
          href: "https://codepen.io/sjfortin/"
        },
        {
          name: "(old) portfolio",
          href: "https://sjfortin.com"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  border-radius: 50%;
  width: 140px;
  height: 140px;
}
</style>
