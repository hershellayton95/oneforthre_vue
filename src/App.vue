<script>
import Button from "./components/Button.vue";
import Input from "./components/Input.vue";
export default {
  components: {
    Button,
    Input,
  },
  data() {
    return {
      value: "",
    };
  },
  methods: {
    handleClick() {
      console.log(this.value);
    },
  },
};
</script>

<template>
  <div>
    <Input type="text" placeholder="inserisci un nome" v-model="value" />
    <Button :onClick="handleClick">Button</Button>
  </div>
  <p>{{ value }}</p>
</template>
