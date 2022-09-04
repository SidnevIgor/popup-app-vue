<template>
    <StackLayout alignItems="center" justifyContent="center">
      <ListView for="item in items" @itemTap="onItemTap">
        <v-template>
          <label :text="item" />
        </v-template>
      </ListView>
      <Button text="Готово" @tap="onCloseTap" class="btn"/>
    </StackLayout>
</template>

<script lang="ts">
  import Vue from "nativescript-vue";

  export default Vue.extend({
    data() {
      return {
        items: ['Пищевая безопасность', 'Охрана труда', 'Эргономика']
      }
    },
    methods: {
      onCloseTap() {
        this.$closeBottomSheet();
      },
      onItemTap() {}
    }
  })
</script>

<style scoped lang="scss">
  .btn {
    background-color: orange;
    width: 80%;
    border-radius: 10;
  }
</style>