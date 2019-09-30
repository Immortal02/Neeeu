<template>
  <div class="container main-content">
    <header>
      <div class="wrap">
        <nuxt-link to="/" class="logo">
          <img src="~/assets/images/logo.svg" />
        </nuxt-link>
        <nav id="menu" :class="isWhiteMenu() ? 'white-menu' : 'black-menu'">
          <li class="drop">
            <div>
              <a>
                <div
                  class="menu-item drop-item"
                  @mouseover="display_drop_menu()"
                  @mouseleave="remove_drop_menu()"
                  @click="display_mobile_drop_menu()"
                >
                  We Create
                  <img
                    v-if="isWhiteMenu()"
                    class="icon"
                    src="~/assets/icons/chevron-down-white.svg"
                  />
                  <img
                    v-else
                    class="icon"
                    src="~/assets/icons/chevron-down-black.svg"
                  />
                </div>
              </a>
              <ul
                class="drop_menu"
                @mouseleave="remove_drop_menu()"
                @mouseover="display_drop_menu()"
              >
                <div class="drop-menu-body">
                  <nuxt-link to="/Career">
                    <div @click="display_menu()">products & services</div>
                  </nuxt-link>
                  <nuxt-link to="/">
                    <div @click="display_menu()">museum experiences</div>
                  </nuxt-link>
                  <nuxt-link to="/Wow">
                    <div @click="display_menu()">media installations</div>
                  </nuxt-link>
                </div>
              </ul>
            </div>
          </li>
          <li>
            <nuxt-link to="/Project">
              <div class="menu-item" @click="display_menu()">Work</div>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/Vision">
              <div class="menu-item" @click="display_menu()">Approach</div>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/About">
              <div class="menu-item" @click="display_menu()">About</div>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/Contact">
              <div class="menu-item" @click="display_menu()">Contact</div>
            </nuxt-link>
          </li>
        </nav>
        <div
          id="hamburger"
          :class="isWhiteMenu() ? 'white-menu' : 'black-menu'"
          @click="display_menu()"
        >
          <img
            v-if="isMenuDisplayed"
            src="~/assets/icons/cross-white.svg"
            class="hamburger-icon"
          />
          <img
            v-else-if="isWhiteMenu()"
            src="~/assets/icons/menu-white.svg"
            class="hamburger-icon"
          />
          <img
            v-else
            src="~/assets/icons/menu-black.svg"
            class="hamburger-icon"
          />
        </div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isWhiteMenu() {
        if (this.$nuxt.$route.path === '/') return true
        if (this.$nuxt.$route.path === '/Contact') return true
        if (this.$nuxt.$route.path === '/Wow') return true
        return false
      },
      isDropDown: false,
      isMenuDisplayed: false
    }
  },
  methods: {
    display_menu() {
      const body = document.getElementsByTagName('body')[0]
      !body.classList.contains('display_menu')
        ? body.classList.add('display_menu')
        : body.classList.remove('display_menu')

      !body.classList.contains('display_menu')
        ? (this.isMenuDisplayed = false)
        : (this.isMenuDisplayed = true)
    },
    display_drop_menu() {
      const dropMenu = event.target.parentElement.parentElement.getElementsByClassName(
        'drop_menu'
      )[0]
      if (!dropMenu) return
      const dropMenus = document.getElementsByClassName('drop_menu')

      Array.from(dropMenus).forEach(function(e) {
        e.classList.remove('display')
      })
      const lis = document.getElementById('menu').getElementsByTagName('li')
      Array.from(lis).forEach(function(e) {
        e.style.marginTop = 0
      })
      dropMenu.classList.add('display')
    },
    remove_drop_menu() {
      const dropMenus = document.getElementsByClassName('drop_menu')
      Array.from(dropMenus).forEach(function(e) {
        e.classList.remove('display')
      })
      this.isDropDown = true
    },
    display_mobile_drop_menu() {
      const dropMenu = event.target.parentElement.parentElement.getElementsByClassName(
        'drop_menu'
      )[0]
      if (!dropMenu) return
      const dropMenus = document.getElementsByClassName('drop_menu')

      Array.from(dropMenus).forEach(function(e) {
        if (e !== dropMenu) {
          e.classList.remove('display')
        }
      })
      const lis = document.getElementById('menu').getElementsByTagName('li')
      Array.from(lis).forEach(function(e) {
        e.style.marginTop = 0
      })
      !dropMenu.classList.contains('display')
        ? dropMenu.classList.add('display')
        : dropMenu.classList.remove('display')
    }
  }
}
window.addEventListener('resize', function(event) {
  closeAllMenu()
  document.getElementsByTagName('body')[0].classList.remove('display_menu')
})
function closeAllMenu() {
  const lis = document.getElementById('menu').getElementsByTagName('li')
  Array.from(lis).forEach(function(e) {
    e.style.marginTop = 0
  })
  const dropMenus = document.getElementsByClassName('drop_menu')
  Array.from(dropMenus).forEach(function(e) {
    e.classList.remove('display')
  })
}
</script>

<style lang="scss" scoped>
$cwhite: white;
$cblack: black;

.header {
  margin: 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.main-content {
  margin: 30px auto;
  max-width: 1600px;
}
.white-menu {
  .menu-item {
    color: rgba(255, 255, 255, 0.8);
  }
  .bars {
    color: white;
  }
}
.black-menu {
  .menu-item {
    color: #262626;
  }
  .bars {
    color: #262626;
  }
}
.display_menu {
  overflow-y: hidden;
}
ul {
  padding: 0;
  margin: 0;
}
li {
  list-style: none;
}
.logo {
  z-index: 1;
}
.menu-item {
  padding: 10px 30px;
  color: $cblack;
  text-decoration: none;
  display: flex;
  align-items: center;
  text-align: center;

  @media (max-width: 1024px) {
    font-size: 14px;
    padding: 10px 8px;
  }
}
.arrow-icon {
  margin-left: 10px;
  font-size: 14px;
}
a:hover .menu-item,
a:active .menu-item,
a.nuxt-link-active .menu-item {
  color: white;
  filter: drop-shadow(0px 4px 8px rgba(76, 87, 123, 0.28));

  &:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: -1;
    background-image: linear-gradient(to right, #ff6969, #9900ce);
    clip-path: polygon(10px 0%, 100% 0%, calc(100% - 10px) 100%, 0% 100%);
  }
}
header {
  display: flex;
  z-index: 1;
  padding: 10px 0;
  background-color: transparent;
  width: 100%;
  top: 0;
  justify-content: center;
  transition: 0.33s;

  .wrap {
    padding: 0 2%;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  img {
    width: 100px;
  }

  .icon {
    margin-left: 10px;
    width: 18px;

    @media (max-width: 1090px) {
      margin-left: 20px;
      width: 30px;
    }
  }

  .hamburger-icon {
    width: 36px;
  }

  #menu {
    display: flex;
    flex-direction: row;
    font-family: 'Bluu Next';
    font-size: 18px;
    font-weight: bold;
    color: $cblack;

    li {
      position: relative;
      user-select: none;
      i {
        width: 12px;
        height: 12px;
        background-color: $cblack;
      }
      a {
        cursor: pointer;
        border: none;
        transition: 0.15s;
        background: none;
        text-decoration: none;
        &:hover {
          color: #0000ff;
        }
      }
    }
  }

  .drop_menu {
    position: absolute;
    display: block;
    transform: scaleY(0);
    width: auto;
    transform-origin: top;
    padding-top: 10px;
    font-size: 14px;
    font-family: 'objektiv-mk2';
    font-weight: 400;
    line-height: 2.08;
    letter-spacing: 3px;
    width: 250px;
    transition: 0.25s;

    .drop-menu-body {
      background-image: linear-gradient(to bottom, #560065, #120078);
      box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.1);
      padding-bottom: 10px;
    }

    a {
      margin-left: 20px;
      display: block;
      transition: 0.45s;
      opacity: 0;
      margin-right: 20px;
      padding: 10px 0 0 0;
    }
  }

  .drop_menu.display {
    transform: scaleY(1);
    a {
      opacity: 1;
      color: white;
    }
  }

  #hamburger {
    cursor: pointer;
    border-radius: 50%;
    position: absolute;
    display: none;
    transform: translateY(-50%);

    span {
      height: 2px;
      margin-top: 5px;
      margin-bottom: 5px;
      background-color: $cblack;
      display: block;
      transition: 0.33s;
      &:nth-child(1) {
        width: 12px;
      }
      &:nth-child(2) {
        width: 24px;
      }
      &:nth-child(3) {
        width: 12px;
      }
    }

    span:nth-child(1) {
      transform: rotate(45deg) translate(2px, 1px);
    }
    span:nth-child(2) {
      transform: rotate(-45deg);
    }
    span:nth-child(3) {
      transform: rotate(45deg) translate(6px, -9px);
    }
  }
}
@media (max-width: 1090px) {
  .main-content {
    margin: 0px auto;
    padding: 0px;
    max-width: 1600px;
  }
  .menu-item {
    color: white !important;
    font-family: 'Bluu Next';
    font-size: 56px;
    font-weight: bold;
    line-height: 0.7;
    display: block;
    text-align: left;
    margin-left: 5px;
  }
  a:hover .menu-item,
  a:active .menu-item,
  a.nuxt-link-active .menu-item {
    color: white;
    background-image: none;
    clear: none;

    &:before {
      content: '';
      position: relative;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      z-index: 0;
      background-image: none;
      clip-path: initial;
    }
  }
  header {
    max-height: 100vh;
    left: 0;
  }
  header .drop-item {
    display: flex;
  }
  header .wrap {
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding-top: 15px;
  }
  header .logo {
    align-self: flex-start;
    margin-left: 30px;
    margin-top: 15px;
  }
  header .bars {
    font-size: 24px;
    font-weight: 200;
  }
  header img {
    width: 75px;
  }
  header #hamburger {
    display: block;
    right: 20px;
    top: 56px;
  }
  header #menu {
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    height: 0;
    // transform-origin: 50% 0;
    // transition: 0.33s ease;
    flex-direction: column;
  }
  .display_menu header {
    background-image: linear-gradient(to bottom, #0b004d, #560065),
      url('~@/assets/images/footer.png');
    background-blend-mode: multiply;
    background-size: cover;
    position: fixed;

    .bars {
      color: white;
    }
  }
  .display_menu header #menu {
    height: 100vh;
    color: white;
    margin: 50px 0px;
    padding-left: 20px;

    .white-menu {
      .menu-item {
        color: white;
      }
    }
    .black-menu {
      .menu-item {
        color: white;
      }
    }

    li {
      height: auto;
      // transition: 0.25s ease;
      opacity: 1;
      display: block;
    }

    .drop_menu.display {
      height: auto;
    }
  }
  header #menu li {
    height: 0;
    opacity: 0;
    margin-left: 0;
    // transition: 0.25s ease;
    i {
      position: absolute;
      right: 20px;
      top: 50%;
      transform: translateY(-50%);
      background-color: $cblack;
    }
  }
  header .drop_menu {
    top: auto;
    box-shadow: none;
    left: 0;
    height: 0px;
    padding-bottom: 0;
    width: 100%;
    top: 20%;
    background-image: none;
    position: relative;
    transition: 0.1s;
    a {
      width: 100%;
      text-align: left;
      padding: 0px !important;
      margin-left: 20px;
    }
    .drop-menu-body {
      background-image: none;
      box-shadow: none;
    }
  }
}
</style>
