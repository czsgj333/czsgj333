<template>
  <img
    class="avatar_container"
    :src="url"
    :style="{ height: size + 'px', width: size + 'px' }"
  />
</template>

<script>
export default {
  props: {
    url: {
      type: String,
      required: true,
    },
    size: {
      type: Number,
      default: 150,
    },
  },
};
</script>

<style scoped>
.avatar_container {
  border-radius: 50%;
  object-fit: cover;
  display: block;
}
</style>
