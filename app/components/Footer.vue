<template>
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-content">
        <p>Matthias van Houtum</p>

        <a
          href="https://www.instagram.com/houtum.van.matthias/"
          target="_blank"
          rel="noopener noreferrer"
        >
          <img
            height="20"
            src="/65f06158687aa96545270241_instagram.svg"
            alt="Instagram"
          />
        </a>
      </div>

      <p id="Copyright">© Copyright {{ new Date().getFullYear() }}</p>
    </div>
  </footer>
</template>

<style scoped lang="scss">
.footer {
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: #fff;
  margin-top: 59px;
  font-family:
    Arial,
    Helvetica Neue,
    Helvetica,
    sans-serif;
  text-align: center;
}

.footer-container {
  width: 1120px;
  border-top: 2px solid #000;
  padding: 29px 0 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.footer-content {
  display: flex;
  flex-direction: row;
  margin-top: 17px;

  & p {
    margin: 0 20px 0 0;
    font-size: 18px;
    line-height: 20px;
  }
}

#Copyright {
  font-size: 16px;
  font-weight: 400;
  margin-top: 27px;
  line-height: 20px;
}

@media (max-width: 1120px) {
  .footer-container {
    width: 100%;
  }
}
</style>
