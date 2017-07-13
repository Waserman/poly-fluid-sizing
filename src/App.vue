<template>
  <div id="app">
    <div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
@import './sass/base';

html {
  box-sizing: border-box;
  height: 100%;
  margin: 0;
  padding: 0;
}

*:not(html):not(head):not(script) {
  box-sizing: inherit;

  &:after,
  &:before {
    box-sizing: inherit;
  }
}

html,
body {
  width: 100%;
  height: 100%;
  font-size: 100%;
}

body {
  position: relative;
}

</style>

