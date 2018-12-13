<template>
  <label class="flex items-center checkbox cursor-pointer">
    <input type="checkbox" class="checkbox-input">
    <span class="checkmark"></span>
    <p class="ml-4">
      <slot></slot>
    </p>
  </label>
</template>

<style scoped>
input.checkbox-input {
  position: relative;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

.checkbox input:checked ~ .checkmark {
  background-color: #032d6c;
}

.checkmark {
  @apply rounded border border-grey;

  position: relative;
  top: 0;
  left: 0;
  height: 17px;
  width: 17px;
}

.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

.checkbox input:checked ~ .checkmark:after {
  display: block;
}

.checkbox .checkmark:after {
  left: 5px;
  top: 2px;
  width: 5px;
  height: 10px;
  border: solid white;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}
</style>
