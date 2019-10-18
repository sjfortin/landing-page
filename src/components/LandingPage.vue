<template>
  <div class="hello container py-8 mx-auto text-center">
    <img class="head mx-auto w-16 h-16" alt="sjf logo" src="../assets/head.jpeg" />
    <h1 class="text-4xl md:text-6xl">{{ msg }}</h1>
    <p class="text-lg md:text-2xl">Web Developer from Minneapolis</p>
    <p class="text-md pt-4">
      Current: Sr Software Engineer at
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
          icon: "gmail",
          svg:
            '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-mail"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>'
        },
        {
          name: "GitHub",
          href: "https://github.com/sjfortin",
          icon: "github",
          svg:
            '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-github"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>'
        },
        {
          name: "LinkedIn",
          href: "https://linkedin.com/sjfortin",
          icon: "linkedin",
          svg:
            '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-linkedin"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>'
        },
        {
          name: "CodePen",
          href: "https://codepen.io/sjfortin/",
          icon: "codepen",
          svg:
            '<?xml version="1.0" ?><svg height="24" viewBox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><polygon fill="none" points="12 2 22 8.5 22 15.5 12 22 2 15.5 2 8.5 12 2" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/><line fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="12" x2="12" y1="22" y2="15.5"/><polyline fill="none" points="22 8.5 12 15.5 2 8.5" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/><polyline fill="none" points="2 15.5 12 8.5 22 15.5" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/><line fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="12" x2="12" y1="2" y2="8.5"/></svg>'
        },
        {
          name: "Twitter",
          href: "https://twitter.com/sjfortin/",
          icon: "twitter",
          svg:
            '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-twitter"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path></svg>'
        },
        {
          name: "Spotify",
          href: "https://open.spotify.com/user/sjfortin",
          icon: "spotify",
          svg:
            '<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-twitter"><path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path></svg>'
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
