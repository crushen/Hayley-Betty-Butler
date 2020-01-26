<template>
  <section id="contact" class="section">
    <div class="content">

      <div class="title">
        <h1>Get in touch</h1>
        <div class="line"></div>
      </div>

      <div class="social">
        <a href=""><i class="fab fa-facebook-f"></i></a>
        <a href=""><i class="fab fa-instagram"></i></a>
      </div>

      <a href="mailto:hayley.butler83@gmail.com">hayley.butler83@gmail.com</a>

      <footer>
        <p>&copy;2020 Hayley Betty Butler.</p>
        <p>Website by <a href="https://charlotterushen.com/">Charlotte Rushen</a></p>
      </footer>

    </div>
  </section>
</template>

<script>

export default {

}
</script>

<style scoped>
.social {
  font-size: 25px;
  margin-bottom: 16px;
}

a {
  color: var(--text);
  margin-right: 25px;
}

.line {
  margin-bottom: 32px;
}

footer {
  padding: 80px 0 24px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

footer p {
  font-size: 10px;
  padding-bottom: 8px;
  opacity: 0.5;
}

footer a {
  margin: 0;
}

</style>