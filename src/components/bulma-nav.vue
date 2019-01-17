<template>
  <nav class="navbar is-primary" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="/">
       <h2 class="subtitle">Gridsome/Bulma</h2>
      </a>
      <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item" href="/documentation">Starter template</a>
      </div>

      <div class="navbar-end">
        <div class="navbar-item field has-addons">
          <p class="control">
            <a class="button">
              <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
            </a>
          </p>
          <p class="control">
            <a class="button">
              <img src="https://gridsome.org/logos/logo-normal.svg" width="112" height="28">
            </a>
          </p>          
       
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "BulmaNav",
  mounted() {
    // Get all "navbar-burger" elements
    const $navbarBurgers = Array.prototype.slice.call(
      document.querySelectorAll(".navbar-burger"),
      0
    );
    // Check if there are any navbar burgers
    if ($navbarBurgers.length > 0) {
      // Add a click event on each of them
      $navbarBurgers.forEach(el => {
        el.addEventListener("click", () => {
          // Get the target from the "data-target" attribute
          const target = el.dataset.target;
          const $target = document.getElementById(target);

          // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
          el.classList.toggle("is-active");
          $target.classList.toggle("is-active");
        });
      });
    }
  }
};
</script>

