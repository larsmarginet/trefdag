<script setup>
defineProps({
    src: String
})
</script>

<template>
    <img class="avatar" :src="src" />
</template>

<style lang='scss' scoped>
.avatar {
    width: 64px;
    height: 64px;
    overflow: hidden;
    border-radius: 100vmax;
}
</style>