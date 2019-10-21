<template>
  <div class="hello container py-8 mx-auto text-center">
    <img class="head mx-auto w-16 h-16" alt="sjf logo" src="../assets/head.jpeg" />
    <h1 class="text-4xl md:text-6xl">{{ msg }}</h1>
    <p class="text-lg md:text-2xl">Web Developer from Minneapolis</p>
    <p class="text-md pt-4">
      Current: Software Engineer at
      <a href="https://www.optum.com" target="_blank" rel="noopener">
        Optum
        <img
          class="inline-block mb-1 w-3 h-3"
          src="../assets/icons/external-link.svg"
          alt="Opens in a new window"
        />
      </a>
    </p>
    <p class="text-md pt-4">
      <a href="https://lucid-snyder-1b0faa.netlify.com/" target="_blank" rel="noopener">
        Portfolio
        <img
          class="inline-block mb-1 w-3 h-3"
          src="../assets/icons/external-link.svg"
          alt="Opens in a new window"
        />
      </a>
    </p>
    <ul class="py-6">
      <li class="inline-block py-2 mx-3 md:mx-6" v-for="(link, index) in links" v-bind:key="index">
        <a v-bind:href="link.href" target="_blank" rel="noopener">
          <img class="icon inline w-6 h-6 md:w-8 md:h-8" v-bind:src="getIcon(link)" v-bind:alt="link.name" />
        </a>
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
          name: "Gmail",
          href: "mailto:sam.j.fortin@gmail.com",
          icon: "gmail"
        },
        {
          name: "GitHub",
          href: "https://github.com/sjfortin",
          icon: "github"
        },
        {
          name: "LinkedIn",
          href: "https://www.linkedin.com/in/samfortin/",
          icon: "linkedin"
        },
        {
          name: "CodePen",
          href: "https://codepen.io/sjfortin/",
          icon: "codepen"
        },
        {
          name: "Twitter",
          href: "https://twitter.com/sjfortin/",
          icon: "twitter"
        },
        {
          name: "Spotify",
          href: "https://open.spotify.com/user/sjfortin",
          icon: "spotify"
        }
      ]
    };
  },
  methods: {
    getIcon(link) {
      return require(`../assets/icons/${link.icon}.svg`);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img.head {
  border-radius: 50%;
  width: 140px;
  height: 140px;
}
img.icon {
  opacity: 0.6;
}
img.icon:hover,
img.icon:focus {
  opacity: 1;
}
</style>
