<template>
  <div class="picker">
    <input ref="colorInput" type="text" @keyup="validateInput" placeholder="#FFF"/>

    <div class="display-area" :style="color">

    </div>
  </div>
</template>

<script>
  export default {
    name: 'picker',
    data() {
      return {
        color: '',
        colorValue: ''
      }
    },
    methods: {
      validateInput: function () {
        const check = this.$refs.colorInput.value.match(/(#[0-9a-zA-Z]{3,8})|((rgba*)\(.+\))/g);
        if (check) {
          this.setColor();
        }
      },
      setColor: function () {
        this.color = `background: ${this.$refs.colorInput.value};`;
      }
    }
  }
</script>

<style scoped>
input {
  width: 80%;
  height: 30px;
  font-size: 20px;
  margin-bottom: 50px;
}
.picker {
  display: inline-block;
  margin: 50px;
}
.display-area {
  width: 500px;
  height: 500px;
}
</style>
