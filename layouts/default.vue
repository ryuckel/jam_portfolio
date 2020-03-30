<template>
  <div class="font-main flex flex-wrap justify-around">
    <Header />
    <main class="mt-10 p-2">
      <nuxt />
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header";
export default {
  components: {
    Header
  }
};
</script>

<style>
main {
  width: 550px;
}
.photo {
  min-width: 4rem;
  min-height: 4rem;
  background-image: url("https://1.bp.blogspot.com/-xb3JjvmmE0U/UPyIwu_nFJI/AAAAAAAAKw4/EM5Ote8wM4I/s1600/knight.png");
}
button:focus {
  outline: none;
}
</style>
