<script>
export default {
  props: {
    modelValue: {
      type: String,
    },
    type: {
      type: String,
    },
    placeholder: {
      type: String,
    },
    onChange: {
      type: Function,
    },
  },
  emits: ["update:modelValue"],
};
</script>

<template>
  <input
    class="inline-block my-2 mx-1 py-[0.35rem] px-2 leading-6 align-middle rounded-sm outline outline-2 focus:outline-offset-1 outline-gray-400 placeholder:italic"
    :type="type"
    :placeholder="placeholder"
    :value="modelValue"
    @input="$event => $emit('update:modelValue', $event.target.value)" />
</template>
