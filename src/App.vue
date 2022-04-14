<template>
  <div id="app">
    <div id="menu">
      <div id="brand">
        <router-link to="/">
          <img
            src="https://elementsdesign.com/wp-content/uploads/2016/10/blog-logo-black-css.jpg"
          />
        </router-link>
      </div>
      <div id="side">
        <router-link to="/profile">
          <div class="menu-item browse">
            <img
              src="https://cdn3.vectorstock.com/i/1000x1000/53/42/user-member-avatar-face-profile-icon-vector-22965342.jpg"
            />
            <p>Profile</p>
          </div>
        </router-link>
        <router-link to="/faq">
          <div class="menu-item">
            <img
              src="https://thumbs.dreamstime.com/b/faq-icon-vector-frequently-illustration-symbol-information-sign-logo-faq-icon-vector-frequently-illustration-symbol-information-158402232.jpg"
            />
            <p>Frequently Asked Questions</p>
          </div>
        </router-link>
      </div>
    </div>
    <router-view />
    <footer>
      <p>
        <a href="https://github.com/brendan-jensen/cs260-creative-project-3"
          >github repo</a
        >
      </p>
    </footer>
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}

footer {
  /* background: #f3f3f3; */
  text-align: center;
  margin-top: 10em;
}

body {
  margin: 50px 100px;
  min-height: 15em;
}

#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "none brand side";
  margin-bottom: 50px;
}

#menu a {
  color: #b84901;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
}

#brand img {
  height: 200px;
}

#side {
  grid-area: side;
  display: flex;
  justify-content: flex-end;
}

#side img {
  width: 50px;
}

.menu-item {
  display: flex;
  flex-direction: column;
}

.menu-item p {
  margin: 0px;
}

.browse {
  margin-right: 50px;
}
</style>