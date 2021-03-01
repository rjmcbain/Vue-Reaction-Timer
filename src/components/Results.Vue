<template>
  <p>Reaction Time Is {{ score }} ms</p>
  <h3 class="rank">{{ rank }}</h3>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 300) {
      this.rank = "Ninja Fast!";
    } else if (this.score < 400) {
      this.rank = "Rapid Reflexes";
    } else {
      this.rank = "Snail pace...";
    }
  },
};
</script>

<style scoped>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
