<template>
  <span ref="countup" id="countup"></span>
</template>

<script>
import { CountUp } from "countup.js";

export default {
  name: "app",
  props: {
    start: {
      type: Number,
      default: 0
    },
    end: {
      type: Number,
      default: 2017
    },
    decimal: {
      type: Number,
      default: 0
    },
    duration: {
      type: Number,
      default: 2.5
    },
    options: {
      type: Object
    },
    autoplay: {
      type: Boolean,
      required: false,
      default: true
    }
  },
  data() {
    return {
      numAnim: null,
      // options:{

      // }
    };
  },
  mounted() {
    this.initCountUp();
  },
  methods: {
    initCountUp() {
      this.options.startVal = this.start
      this.numAnim = new CountUp(this.$refs.countup, this.end, this.options);
      if (!this.numAnim.error && this.autoplay) {
        this.numAnim.start();
      } else {
        console.log(this.numAnim.error);
      }
    }
  }
};
</script>

