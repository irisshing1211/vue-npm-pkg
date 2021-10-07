<template>
  <ul class="menu list-unstyled mb-0" :style="`background-color: ${bgColor}`">
    <li
      :class="{ active: isActiveItem(item.to) }"
      v-for="item in items"
      :key="item.name"
    >
      <b-link :to="{ name: item.to }">
        <b-icon
          :icon="item.icon"
          style="color: #ffffff"
          class="menu-img mx-2"
        ></b-icon>
        <b-icon
          :icon="item.icon"
          :style="`color: ${bgColor}`"
          class="menu-img-active mx-2"
        ></b-icon>

        <span>{{ item.name }}</span>
      </b-link>
    </li>
  </ul>
</template>

<script>
export default {
  name: "RightMenu",
  props: {
    current: String, //this.$route.meta.rootMenu
    items: Array, //[{name:"Partner", to:"Partner",icon:"bootstrap icon"}]
    bgColor: String,
  },
  methods: {
    isActiveItem(rootMenu) {
      return this.current === rootMenu;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "~bootstrap/scss/functions";

.menu {
  display: flex;
  flex-direction: column;
  border-radius: 1.25rem;
  box-shadow: -10px -10px 20px 0 #fff, 10px 10px 20px 0 rgba(174, 174, 192, 0.4),
    inset 4px 4px 6px 0 rgba(255, 255, 255, 0.4);
  z-index: 10;
  padding: 0.75rem;

  li {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    border-radius: 50%;
    width: 3rem;
    height: 3rem;
    background: linear-gradient(-42deg, #0077c6 0%, #00a7e0 95%);
    margin: 0.75rem 0;

    span {
      display: none;
    }

    .menu-img-active {
      display: none;
    }

    &:hover {
      a {
        position: absolute;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        width: 9rem;
        background-color: rgba(242, 243, 247, 0.7);
        border-radius: 1.5rem;
        text-decoration: none;
        font-weight: 500;
        box-shadow: 10px 10px 20px 0 rgb(174 174 192 / 40%),
          inset 2px 2px 6px 0 rgb(255 255 255 / 80%);
        backdrop-filter: blur(10px);
        top: 0;
        bottom: 0;
        left: 0;
        margin: 0;
      }

      .menu-img {
        display: none;
      }

      .menu-img-active {
        display: inline-block;
      }

      span {
        display: inline-block;
      }
    }

    &.active {
      background: #f0f0f3;

      .menu-img {
        display: none;
      }

      .menu-img-active {
        display: inline-block;
      }
    }
  }
}
</style>
