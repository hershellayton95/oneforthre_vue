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
    setValue(input) {
      this.value = input;
    },
    handleClick() {
      console.log(this.value);
    },
    handleChange(e) {
      this.setValue(e.target.value);
    },
  },
};
</script>

<template>
  <div>
    <Input
      type="text"
      placeholder="inserisci un nome"
      :value="value"
      :onChange="handleChange" />
    <Button :onClick="handleClick">Button</Button>
  </div>
  <p>{{ value }}</p>
</template>
