<script>
export default {
  props: {
    onClick: {
      type: Function,
    },
  },
};
</script>
<template>
  <button
    class="inline-block bg-blue-500 hover:bg-blue-600 active:scale-[0.95] text-white my-2 mx-1 py-2 px-3 leading-6 text-center align-middle cursor-pointer rounded select-none"
    @click="onClick">
    <slot />
  </button>
</template>
