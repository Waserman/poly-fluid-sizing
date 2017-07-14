<template>
  <div id="app">
    <div>
      <p id="fontsize">this is the font size: {{ fontSize }}</p>
      the view port is: {{ vw }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      fontSize: '',
      vw: ''
    }
  },
  mounted () {
    window.addEventListener('resize', (e) => {
      this.$nextTick(() => {
        this.vw = document.documentElement.clientWidth
        let paragraph = document.querySelector('#fontsize')
        let font_size = window.getComputedStyle(paragraph, null).getPropertyValue('font-size')

        this.fontSize = parseFloat(font_size) + 'px'

      })
    })
  }
}
</script>

<style lang="scss">
  @import './sass/base';
    html {
        box-sizing: border-box;
        height: 100%;
        margin:0;
        padding: 0;
    }
    *:not(html):not(head):not(script) {
        box-sizing: inherit;
        &:after, &:before {
            box-sizing: inherit;
        }
    }
    html, body {
        width: 100%;
        height: 100%;
        padding: 30px;
    }

    #fontsize {
      @include poly-fluid-sizing('font-size', (640px: 24px, 1920px: 40px)); 
    }
</style>

