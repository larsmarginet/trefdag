<template>
  <div class="wrapper">
    <div class="inner">
      <NuxtPage />
    </div>
  </div>
</template>

<style lang="scss"> 
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  background-color: black;
}

.inner {
  width: var(--body-width);
  min-height: var(--body-height);
  max-height: 100vh;
  background-color: white;
}
</style>
