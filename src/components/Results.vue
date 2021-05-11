<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
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
    if (this.score < 250) {
      this.rank = "SO FAST MY GUY";
    } else if (this.score < 400) {
      this.rank = "Not bad at all";
    } else {
      this.rank = "...Are you awake?";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #940faf;
  font-weight: bold;
}
</style>