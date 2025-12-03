<template>
  <v-btn
    text="linkbutton"
  ></v-btn>
</template>

<script>
  export default {
    name: "UILinkbutton",
    inject: ['$dataTracker', '$socket'],
    props: {
      id:    { type: String, required: true },
      props: { type: Object, default: () => ({}) },
      state: { type: Object, default: () => ({ enabled: false, visible: false }) }
    },
    data() {
      return {
        base: null,
        msg: null
      }
    },
    created() {
      this.$dataTracker(this.id, this.onInput, this.onLoad)
    },
    methods: {
      onInput(msg) {
        this.msg = msg
      },
      onLoad(msg, base) {
        this.msg = msg
        this.base = base
      }
    }
  }
</script>