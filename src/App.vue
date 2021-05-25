<template>
  <div class="main-container">
    <!-- Left navigation bar  -->
    <div class="nav">
      <router-link to="/">
        <img
          src="https://black-box.com.au/wp-content/themes/blackbox/images/logo.png"
          alt="logo"
        />
      </router-link>
      <!-- router-link is Vue element, which replaces anchor tag -->
      <div class="links">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/gallery">Gallery</router-link>
      </div>
    </div>

    <!-- The element / pages will be rendered in router-view -->
    <div class="view-container">
      <router-view class="render-element"></router-view>
    </div>
  </div>
</template>

<style lang="scss">
*,
html {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  a {
    margin-top: 1rem;
    font-weight: bold;
    color: #333;
    text-decoration: none;
    &:hover {
      color: #faa419;
    }
  }
}

.main-container {
  width: 100%;
  display: flex;
  flex-direction: row;
}

.nav {
  background-color: #f3f3f3;
  width: 13rem;
  height: 100vh;
  display: flex;
  flex-direction: column;
  padding: 1rem;
  border-right: 1px solid #e0e0e0;
  img {
    width: 90%;
    margin-bottom: 2rem;
  }

  .links {
    display: flex;
    flex-direction: column;
    a {
      margin-top: 1rem;
      font-weight: bold;
      color: #333;
      text-decoration: none;
      &:hover {
        color: #faa419;
      }
    }
  }
}

.view-container {
  width: 100%;
  padding: 1rem;

  .render-element {
    border-radius: 2px;
    box-shadow: rgba(0, 0, 0, 0.12) 0px 1px 3px, rgba(0, 0, 0, 0.24) 0px 1px 2px;

    // &:hover {
    //   box-shadow: rgba(0, 0, 0, 0.11) 0px 5px 10px,
    //     rgba(0, 0, 0, 0.2) 0px 3px 3px;
    // }
  }
}
</style>
