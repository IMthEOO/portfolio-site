<template>
  <div class="navbar">
    <div class="content">
      <div class="mail-content">
        <a :href="'mailto:ogbeosose@gmail.com'">
          <img alt="mail icon" src="../assets/img/mail.svg" />
          <span>ogbeosose@gmail.com</span>
        </a>
      </div>
      <ul class="nav-links">
        <li><a href="">Works</a></li>
        <li><a href="">Services</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>