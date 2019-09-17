<template>
  <div>
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header'
import Footer from '~/components/Footer'
export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
@import url('https://p.typekit.net/p.css?s=1&k=ago3kxj&ht=tk&f=26978.26982.26985&a=5102651&app=typekit&e=css');
@import '~assets/scss/global.scss';

@font-face {
  font-family: 'Bluu Next';
  src: url('~static/fonts/bluu-next/Fonts/webfonts/bluunext-bold-webfont.woff')
      format('woff'),
    url('~static/fonts/bluu-next/Fonts/webfonts/bluunext-bold-webfont.woff2')
      format('woff2'),
    url('~static/fonts/bluu-next/Fonts/BluuNext-Bold.otf') format('otf');
}

@font-face {
  font-family: 'objektiv-mk2';
  src: url('https://use.typekit.net/af/3a2a4a/00000000000000003b9add10/27/l?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n3&v=3')
      format('woff2'),
    url('https://use.typekit.net/af/3a2a4a/00000000000000003b9add10/27/d?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n3&v=3')
      format('woff'),
    url('https://use.typekit.net/af/3a2a4a/00000000000000003b9add10/27/a?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n3&v=3')
      format('opentype');
  font-display: auto;
  font-style: normal;
  font-weight: 300;
}

@font-face {
  font-family: 'objektiv-mk2';
  src: url('https://use.typekit.net/af/e42109/00000000000000003b9add13/27/l?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n5&v=3')
      format('woff2'),
    url('https://use.typekit.net/af/e42109/00000000000000003b9add13/27/d?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n5&v=3')
      format('woff'),
    url('https://use.typekit.net/af/e42109/00000000000000003b9add13/27/a?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n5&v=3')
      format('opentype');
  font-display: auto;
  font-style: normal;
  font-weight: 500;
}

@font-face {
  font-family: 'objektiv-mk2';
  src: url('https://use.typekit.net/af/333f59/00000000000000003b9add18/27/l?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n8&v=3')
      format('woff2'),
    url('https://use.typekit.net/af/333f59/00000000000000003b9add18/27/d?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n8&v=3')
      format('woff'),
    url('https://use.typekit.net/af/333f59/00000000000000003b9add18/27/a?primer=7cdcb44be4a7db8877ffa5c0007b8dd865b3bbc383831fe2ea177f62257a9191&fvd=n8&v=3')
      format('opentype');
  font-display: auto;
  font-style: normal;
  font-weight: 800;
}

html {
  font-family: 'objektiv-mk2', 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  font-family: 'objektiv-mk2', 'Helvetica Neue', Arial, sans-serif;
  color: #262626;
  width: 100%;

  // @media (min-width: 1600px) {
  //   max-width: 1600px;
  //   margin: 0 auto;
  // }
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.container {
  width: calc(100% - 200px);
  padding: 0px;

  @media (max-width: 1000px) {
    width: calc(100vw - 50px);
  }

  @media (max-width: $screen-xs-max) {
    width: 100vw;
  }
}

.topic {
  padding: 50px 20px;
  padding-bottom: 0px;
  text-align: left;

  .title {
    font-size: 14px;
    font-family: 'objektiv-mk2';
    font-weight: 500;
    line-height: 1.79;
    letter-spacing: 3.5px;
    margin-bottom: 10px;

    @media (max-width: $screen-xs-max) {
      font-size: 12px;
    }
  }

  .sub-title {
    font-size: 80px;
    font-family: 'Bluu Next';
    font-weight: bold;
    line-height: 1.13;
    letter-spacing: 1.49px;

    @media (max-width: $screen-xs-max) {
      font-size: 56px;
    }
  }

  .content {
    font-size: 20px;
    font-weight: 300;
    line-height: 1.6;
    letter-spacing: normal;
    margin: 30px 0px;

    @media (max-width: $screen-xs-max) {
      font-size: 17px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px 30px 30px;
    line-height: 1.13;
  }
}
.icon {
  width: 14px;
}
.arrow-icon {
  width: 12px;
  margin-left: 10px;
}
</style>
