<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>{{ now }}</p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      now: new Date()
    };
  },
  methods: {
    updateDate() {
      this.now = new Date();
    },
  },
  mounted() {
    setInterval(() => {
      this.updateDate();
    }, 1000);
  },
}
</script>