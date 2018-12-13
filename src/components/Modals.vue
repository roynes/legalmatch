<template>
  <div class="modal" :class="showModal">
    <div class="modal-content">
      <div class="header">
        <div class="main-contents">
          <slot name="header-contents"></slot>
        </div>
        <!-- <div class="button-content"> -->
          <span class="close" @click="$emit('close', true)">&times;</span>  
        <!-- </div> -->
      </div>

      <div class="mark">
        <slot name="mark-content"></slot>
      </div>
      
      <div class="contents">
        <slot name="content-slot"></slot>
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
    }
  },

  computed: {
    showModal() {
      if(this.toggle) return { hidden: false, flex: true };
      else return { hidden: true, flex: false }
    }
  }
}
</script>

<style scoped>

.modal {
  position: fixed;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
  z-index: 100;
  @apply items-center justify-center select-none;
}

.modal-content {
  min-width: 300px;
  min-height: 300px;
  @apply bg-white rounded-lg flex flex-col items-center;
}

.header {
  @apply mb-4 w-full flex px-3;
}

.contents {
  @apply w-full px-3 overflow-auto mb-3;
}

.main-contents {
  @apply w-full flex mt-2;
}

.mark {
  @apply w-full px-3;
}

.close {
  color: rgb(228, 220, 220);
  font-size: 28px;
  font-weight: bold;
  position: absolute;
  right: 0px;
  top: 0px;
  margin-right: 10px;
}

.close:hover,
.close:focus {
  color: rgba(224, 209, 209, 0.384);
  text-decoration: none;
  cursor: pointer;
}

</style>


