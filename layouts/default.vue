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
@import '~assets/scss/fontstyles.scss';

@font-face {
  font-family: 'BluuNext';
  src: url('~static/fonts/bluu-next/Fonts/webfonts/bluunext-bold-webfont.woff')
      format('woff'),
    url('~static/fonts/bluu-next/Fonts/webfonts/bluunext-bold-webfont.woff2')
      format('woff2'),
    url('~static/fonts/bluu-next/Fonts/BluuNext-Bold.otf') format('otf');
}

@font-face {
  font-family: 'ObjektivMk2';
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
  font-family: 'ObjektivMk2';
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
  font-family: 'ObjektivMk2';
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

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

html {
  font-family: 'ObjektivMk2', 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  font-family: 'ObjektivMk2', 'Helvetica Neue', Arial, sans-serif;
  color: #262626;
  width: 100%;
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
    @include desktoptitleh2();

    @media (max-width: $screen-xs-max) {
      @include mobiletitleh2();
    }
  }

  .sub-title {
    @include desktopsubtitle();
    text-transform: uppercase;
    margin-bottom: 10px;

    @media (max-width: $screen-xs-max) {
      @include mobilesubtitle();
    }
  }

  .content {
    @include mobileplarge();
    margin: 30px 0px;

    @media (max-width: $screen-xs-max) {
      @include mobilepregular();
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px 30px 30px;
    line-height: 1.13;
  }
}
.icon {
  width: 18px;
}
.arrow-icon {
  width: 20px;
  margin-left: 10px;
}
.pointer {
  cursor: pointer;
}
</style>
