<template>
  <v-checkbox
    class="checkbox"
    v-model="valueLocal"
    v-bind="$attrs"
    v-on="$listeners"
  />
</template>

<script>
export default {
  props: {
    value: Boolean,
  },

  computed: {
    valueLocal: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit('input', val);
      },
    },
  },
};
</script>

<style lang="scss">
// Your custom styles
.checkbox {
  display: inline-block;
  .v-label {
    font-size: 0.9em;
  }
}
</style>
