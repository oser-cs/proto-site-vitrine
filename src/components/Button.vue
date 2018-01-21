<template>
  <div class="btn">
    <a :href="href" :style="style" @mouseover="mouseOver()" @mouseout="mouseOver()">{{ title }}</a>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    title: {
      type: String,
      required: true
    },
    color: {
      type: String,
      default: "white"
    },
    hoverColor: {
      type: String,
      default: "black"
    },
    href: {
      type: String,
      required: true
    }
  },
  computed: {
    style () {
      let bg = this.hovering ? this.color : "none";
      let color = this.hovering ? this.hoverColor : this.color;
      return `
        background: ${bg};
        color: ${color};
        border: 1px solid ${this.color};
      `;
    }
  },
  data () {
    return {
      hovering: false
    }
  },
  methods: {
    mouseOver () {
      this.hovering = !this.hovering;
    }
  }
}
</script>

<style lang="scss" scoped>
.btn {
  $padding: 8px;
  box-sizing: content-box;
  text-align: center;
  margin: $padding 0;
  a {
    -webkit-appearance: none;
    -webkit-border-radius: 0;
    padding: $padding;
    border-radius: 4px;
    transition: background 0.2s, color 0.2s;
    font-weight: bold;
  }
}
</style>
