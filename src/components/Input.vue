<script>
export default {
  props: {
    type: String,
    value: String,
    placeholder: String,
    onChange: {
      type: Function,
    },
  },
};
</script>

<template>
  <input
    class="inline-block my-2 mx-1 py-[0.35rem] px-2 leading-6 align-middle rounded-sm outline outline-2 focus:outline-offset-1 outline-gray-400 placeholder:italic"
    :type="type"
    :value="value"
    :placeholder="placeholder"
    @input="onChange" /><!--v-on:input="onChange" -->
</template>
