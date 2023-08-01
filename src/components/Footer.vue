<template>
  <footer>
    <div class="row footer__row">
      <a href="/" class="footer__anchor">
        <h3 class="footer__logo">MB</h3>
        <span class="footer__logo--popper">
        Top
        <i class="bx bx-up-arrow-alt" />
      </span>
      </a>
      <div class="footer__social--list">
        <a
            href="https://github.com/M4TThys123"
            target="_blank" rel="noreferrer"
            class="footer__social--link link__hover-effect link__hover-effect--white"
        >GitHub</a
        >
        <a
            href="https://www.linkedin.com/in/matthijs-blauw-9a9573235/"
            target="_blank" rel="noreferrer"
            class="footer__social--link link__hover-effect link__hover-effect--white"
        >LinkedIn</a
        >
        <a
            href="mailto:matthijs.blauw@gmail.com"
            target="_blank"
            class="footer__social--link link__hover-effect link__hover-effect--white"
        >Email</a
        >
        <a
            href="/"
            target="_blank"
            class="footer__social--link link__hover-effect link__hover-effect--white"
        >CV</a
        >
      </div>
      <div class="footer__copyright">Copyright © 2022 Matthijs Blauw</div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent"
}
</script>

<style scoped>
/* FOOTER */
footer{
  background-color: #242424;
}

.row {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  padding: 0 12px;
}

.footer__row{
  padding: 8% 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.footer__anchor{
  position: relative;
  margin-bottom: 20px;
}

.footer__anchor:hover .footer__logo--popper{
  transform: translateX(60px);
  opacity: 1;
}

.footer__logo{
  color: #fff;
  font-size: 50px;
}

.footer__logo--popper{
  color: #fff;
  position: absolute;
  right: 0;
  top: 30px;
  font-weight: 700;
  opacity: 0;
  transition: all 300ms ease;
}
.footer__social--list{
  margin-bottom: 28px;
  width: 100%;
  max-width: 500px;
  display: flex;
  justify-content: space-around;

}
.footer__social--link,
.footer__copyright{
  color: #fff;
}
.link__hover-effect:after{
  content: "";
  position: absolute;
  background-color: black;
  height: 3px;
  width: 0;
  bottom: -3px;
  right: 0;
  transition: all 300ms ease;
}

.link__hover-effect:hover:after{
  width: 100%;
  left: 0;
}

.link__hover-effect--white::after{
  background-color: white;
}
</style>