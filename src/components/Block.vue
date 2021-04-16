<template>
  <div class="block" v-if="showBlock">click me</div>
</template>

<script>
export default {
  name: "Block",
  props: ["delay"],
  data() {
    return {
      showBlock: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showBlock = true;
    }, this.delay);
  },
};
</script>

<style>
.block {
  width: 400px;
  border-radius: 20px;
  background: green;
  color: white;
  text-align: center;
  padding: 100px;
  margin: 10px auto;
}
</style>