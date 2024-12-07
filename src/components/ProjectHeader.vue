<template>
  <div class="header-container">
    <div class="page-header">
      <h1 class="page-title">Infinite Carousel</h1>
      <h2 class="page-subtitle">Experiment project by <span>Andrew Wang</span></h2>
    </div>
  </div>
</template>

<style scoped>
.header-container {
  width: 100%;
  padding: 20px;
  display: flex;
  justify-content: center;
  color: var(--color-text);
}

.page-header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 16px;
  font-family: 'Roboto';
  padding-bottom: 16px;
  border-bottom: 1px solid var(--color-text);
}

.page-header .page-title {
  font-size: 36px;
  font-weight: 700;
}

.page-header .page-subtitle {
  font-size: 20px;
  font-weight: 400;
}

.page-header .page-subtitle span {
  font-weight: 700;
}
</style>