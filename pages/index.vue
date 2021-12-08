<template>
  <main class="mainContentWrapper">
    <section class="loginSectionWrapper">
      <figure>
        <img src="images/presentation-banner.jpg" alt="">
      </figure>
      <FormSection />
    </section>
  </main>
</template>

<script>

export default {

  data () {
    return {
      name: 'ThZ1N'
    }
  },
  head: {
    title: 'Slidz | Portal do usuário',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'theme-color', content: '#5D26D0' }
    ]
  }
}
</script>

<style lang="scss" scoped>

.mainContentWrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  min-height: 100vh;

  .loginSectionWrapper {
    display: grid;
    max-width: 1100px;
    grid-template-columns: 960px 434px;
    // column-gap: -294px;

    figure {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      width: 960px;
      height: 650px;
      overflow: hidden;
      border-radius: 2.3rem;
    }

    figure img {
      height: 100%;
      max-height: 650px;
      object-fit: cover;
    }
  }
}
</style>
