<script setup>
defineProps({
    isActive: {
    type: Boolean,
    required: false
  }
})

</script>

<template>
  <div class="hamburger" :class="{ isActive: isActive }">
    <span class="line-1"></span>
    <span class="line-2"></span>
    <span class="line-3"></span>
  </div>
</template>

<style scoped>
.hamburger span {
  display: block;
  width: 30px;
  height: 3px;
  background-color: #000;
  margin-top: 5px;
}

.hamburger.isActive .line-1 {
  transform: rotate(45deg) translateX(12px);
  transition: 0.25s ease-in-out;
}

.hamburger.isActive .line-2 {
  opacity: 0;
  transition: 0.25s ease-in-out;
}

.hamburger.isActive .line-3 {
  transform: rotate(-45deg) translateX(12px);
  transition: 0.25s ease-in-out;
}
</style>
