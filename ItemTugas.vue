<template>
  <div>
    <div class="form-check">
      <input class="form-check-input" onclick="" type="checkbox" value="" id="CheckDefault" />
      <label class="form-check-label item" v-bind:class="{ 'item-completed': tugasSaya.isdone }" for="CheckDefault">{{ tugasSaya.namaTugas }}</label>
    </div>
  </div>
</template>

<script>
export default {
  name: "ItemTugas",
  props: ["tugasSaya"],
};
</script>

<style scoped></style>
