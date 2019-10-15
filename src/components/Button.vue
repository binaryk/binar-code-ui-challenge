<template>
  <div class="button-style">
      <button class="button-master">
          <div class="button-content">
              <div class="button-text">Send</div>
              <svg data-v-04d2d661="" viewBox="0 0 32 32" saria-hidden="true" class="send-arrow"><path data-v-04d2d661="" d="M5.975 17.504l14.287.001-6.367 6.366L16.021 26l10.004-10.003L16.029 6l-2.128 2.129 6.367 6.366H5.977z"></path></svg>
          </div>
      </button>
  </div>
</template>

<script>
export default {
    name: "button-master"
}
</script>

<style>

button-style {
    font-family: 'Montserrat', sans-serif;
}

.button-master {
    font-weight: bold;
    font-size: 18px;
    width: 180px;
    height: 50px;
    border-radius: 10px;
    margin: 60px;
    outline: 0;
}

.button-content {
    display: inline-flex;
}

.button-text {
    margin: auto 0 auto 0;
}

.send-arrow {
    width: 25px;
    margin: 7px;
}

</style>