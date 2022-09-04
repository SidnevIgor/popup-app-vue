<template>
  <Page>
    <ActionBar>
      <Label text="Popup app"/>
    </ActionBar>

    <FlexboxLayout alignItems="center" justifyContent="center">
      <Button text="Открыть попап" @tap="onOpenPopup"></Button>
    </FlexboxLayout>
  </Page>
</template>

<script lang="ts">
  import { VueBottomSheetOptions } from "@nativescript-community/ui-material-bottomsheet/vue";
  import Vue from "nativescript-vue";
  import BottomSheet from "./BottomSheet.vue";
  

  export default Vue.extend({
    methods: {
      onOpenPopup() {
        console.log("Open popup");
        const options: VueBottomSheetOptions = {
        };
        this.$showBottomSheet(BottomSheet, options); 
      }
    }
  });
</script>

<style scoped lang="scss">
  
</style>
