<template>
  <header class="md:w-64 w-full h-64 px-2">
    <div class="md:w-64 w-full md:mt-24 mt-12 relative md:fixed">
      <div class="flex">
        <div
          class="bg-center bg-cover w-16 h-16 mr-2 rounded-full shadow photo"
        ></div>
        <div>
          <h1 class="font-bold">Ryusuke Miyaji</h1>
          <p class="text-xs text-justify">
            Ruby on Rails/Vue.jsを主に使用しているエンジニアです。<br />
            Python/Docker/AWS(ECS,ECRが中心) も使えます。<br />
            TypeScript/Go/Kotlin/数学や統計学なども勉強しています。<br />
            ご依頼はメールアドレスからお願いします。<br />
            Email:bkuce826@gmail.com
          </p>
        </div>
      </div>
      <div class="flex justify-around mt-5 text-xs">
        <nuxt-link to="/">
          <button>
            <fa-layers full-width class="fa-2x block mx-auto mb-1">
              <fa :icon="faCode" />
            </fa-layers>
            Works
          </button>
        </nuxt-link>
        <a href="http://" target="_blank" rel="noopener noreferrer">
          <button>
            <fa-layers full-width class="fa-2x block mx-auto mb-1">
              <fa :icon="faTwitter" />
            </fa-layers>
            Twitter
          </button>
        </a>
        <a
          href="https://github.com/si-zerodarkthirty"
          target="_blank"
          rel="noopener noreferrer"
        >
          <button>
            <fa-layers full-width class="fa-2x block mx-auto mb-1">
              <fa :icon="faGithub" />
            </fa-layers>
            GitHub
          </button>
        </a>
      </div>
      <input
        type="text"
        placeholder="Keywords"
        class="bg-gray-300 p-2 text-xs rounded w-full mt-5 focus:outline-none"
        v-model="keyword"
        @keypress.enter="$router.push('/search/' + keyword)"
      />
    </div>
  </header>
</template>

<script>
import { faTwitter } from "@fortawesome/free-brands-svg-icons";
import { faGithub } from "@fortawesome/free-brands-svg-icons";
import { faCode } from "@fortawesome/free-solid-svg-icons";
export default {
  data() {
    return {
      keyword: ""
    };
  },
  computed: {
    faTwitter() {
      return faTwitter;
    },
    faGithub() {
      return faGithub;
    },
    faCode() {
      return faCode;
    }
  }
};
</script>
