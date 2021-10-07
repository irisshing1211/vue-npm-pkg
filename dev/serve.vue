<script>
import Vue from "vue";
import RightMenu from "../src/lib-components/RightMenu.vue";
// Uncomment import and local "components" registration if library is not registered globally.
// import { IrisTestNpmpkgSample } from '@/entry.esm';

export default Vue.extend({
  components: { RightMenu },
  name: "ServeDev",
  data:()=> ({
    menuItems:[{name:"Partner", to:"Partner",icon:"bar-chart-fill"},
    {name:"Partner2", to:"Partner2",icon:"card-image"}]
  }),
  // components: {
  //  IrisTestNpmpkgSample,
  // }
});
</script>

<template>
  <div id="app">
    <large-btn txt="12345" />
    <right-menu :items="menuItems" bgColor="#0088d1" />
  </div>
</template>
