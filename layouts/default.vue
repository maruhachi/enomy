<template>
  <section class="section">
    <header class="header">
      <div class="container">
        <nav class="navbar">
          <div class="navbar-menu">
            <div class="navbar-start">
              <a href="" class="navbar-item button is-medium">index</a>
              <a href="" class="navbar-item button is-medium"><i class="fab fa-twitter"></i>pictures</a>
            </div>
          </div>
        </nav>
      </div>
    </header>
    <nuxt/>
    <footer class="footer">
      <div class="container">
      <div class="content has-text-centered">
        <p>{{ branchName }}</p>
      </div>
      </div>
    </footer>
  </section>
</template>

<script>
export default {
  data() {
    return {
      branchName: process.env.branchName
    };
  }
}
</script>


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
</style>
