<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

:root {
  --primary-bg-color: #121212;
  --primary-paper-color: #313131;
  --primary-color: #ef6c00;
  --primary-color-light: #ff9d3f;
  --primary-color-dark: #b53d00;
  --secondary-color: #039be5;
  --secondary-color-light: #63ccff;
  --secondary-color-dark: #006db3;
  --primary-text-color: rgba(255, 255, 255, 0.87);
  --secondary-text-color: rgba(255, 255, 255, 0.6);
  --disabled-text-color: rgba(255, 255, 255, 0.38);
}

h1,
h2,
h3,
h4,
h5 {
  color: var(--primary-color);
}
</style>
