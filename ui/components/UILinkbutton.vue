<template>
  <iframe 
    v-if="props.embedded && props.url"
    :src="props.url"
    style="width: 100%; height: 100%; border: none;"
  ></iframe>
  <v-btn
    v-else
    @click="onClick"
    :text="props.text"
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
      },
      onClick() {
        if (this.props.newTab) window.open(this.props.url, "_blank")
        else window.location.href = this.props.url
      }
    }
  }
</script>