<template>
  <div id="app">
    <button class="accodion" type="button" @click="accodion()" :class="{'active':isOpen}">アコーディオン</button>
    <div class="accodion-content" :class="{'open':isOpen}">
      <p>アコーディオンの中身が入ります</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    accodion() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<style>
.accodion {
  width: 500px;
  height: 50px;
  text-align: left;
  padding-left: 20px;
  font-size: 16px;
}

.accodion-content {
  border: 1px solid;
  width: 500px;
  height: 50px;
  padding-left: 30px;
  box-sizing: border-box;
  font-size: 14px;
}
</style>