<template>
  <div 
    class="drop-down text-left absolute mt-20 rounded-lg border bg-white h-48 mx-1 p-4"
    :class="showDropDown"
  >
    <div class="inner text-grey-dark leading-loose cursor-pointer overflow-y-auto h-full relative">
      <div 
        class="px-12 hover:text-black hover:bg-grey" 
        v-for="(item, index) in contents" 
        :key="index"
        @click="$emit('content-click', { v: item, tog: true})"
      >
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    toggle: {
      type: Boolean,
      default: false,
    },
    contents: {
      type: Array,
      default() {
        return [];
      }
    }
  },

  computed: {
    showDropDown() {
      if(this.toggle) return { hidden: false };
      else return { hidden: true }
    }
  }
}
</script>

<style scoped>
div.drop-down {
  width: 33.1rem;
}
</style>
