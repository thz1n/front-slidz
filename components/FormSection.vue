<template>
  <div class="formSectionWrapper">
    <title class="topForm">
      <h1 class="logo">slidz</h1>
      <router-link to="/">
      <button type="button" class="homeButton">
      <i class="fal fa-home fa-2x"></i>
      </button>
      </router-link>
    </title>
    <div class="bodyForm">
      <form action="">
        <label for="account-input">Your Account</label>
        <input
          id="account-input"
          name="form-account"
          type="text"
          autocomplete="off"
          placeholder="slidz"
          required
        >

        <label for="pass-input">Your Password</label>

        <div class="passgroup">
          <input
            id="pass-input"
            name="form-password"
            :type="!showPass ? 'password' : 'text' "
            autocomplete="off"
            placeholder="****************"
            required
          >
          <i :class=" !showPass ? 'fal fa-eye' : 'fal fa-eye-slash' " @click="changePass" />
        </div>

        <div class="buttonGroup">
          <button class="mainButton">
            sign in
          </button>
          <router-link to="/register">
            new account
          </router-link>
        </div>
        <router-link to="/forgot-password">
          forgot password
        </router-link>
      </form>
    </div>
  </div>
</template>

<script>

export default {

  data () {
    return {
      showPass: false
    }
  },
  methods: {
    changePass () {
      this.showPass = !this.showPass
    }
  }
}
</script>

<style lang="scss" scoped>

    .formSectionWrapper {
      display: flex;
      flex-direction: column;
      position: relative;
      max-height: 580px;
      align-self: center;
      background-color: #5D26D0;
      border-radius: 2.3rem;
      filter: drop-shadow(0 0 3.125rem rgba(0,0,0,0.15));
      left: -294px;

      .topForm {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 1rem 2.5rem;

        .logo {
          color: white;
          font-size: 48px;
        }

        .homeButton {
          display: flex;
          align-items: center;
          justify-content: center;
          color: white;
          background: rgba(0,0,0,0.3);
          border-radius: 50%;
          width: 60px;
          aspect-ratio: 1 / 1;
        }
      }

      .bodyForm {
        display: flex;
        flex-direction: column;
        padding: 3rem 3.5rem;
        background-color: white;
        border-radius: 2.3rem;

        form {
          display: flex;
          flex-direction: column;

          label {
            margin-bottom: .3rem;
          }

          input[type=text],
          input[type=password] {
            width: 100%;
            border: 2px solid #5D26D0;
            padding: 1.5rem;
            border-radius: 0.9375rem;
            background-color: #F5F5F5;
            color: #868686;
            font-size: 16px;
            margin-bottom: 1rem;
          }

          input[type=text]:focus,
          input[type=password]:focus {
            outline: none;
          }
          .buttonGroup {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background-color: #F1F1F1;
            border-radius: 10rem;
            margin-top: 2rem;

            button.mainButton {
              background-color: #5D26D0;
              color: white;
              padding: 1rem;
              border-radius: 10rem;
              width: 50%;
            }
            & > a {
              width: 50%;
              text-align: center;
            }
          }
          > a {
            width: 100%;
            text-align: center;
            margin-top: 1rem;
          }
          .passgroup {
            display: flex;
            align-items: center;
            position: relative;
            width: 100%;

            i {
              position: absolute;
              right: 20px;
              top: 30px;
              color: #5D26D0;
              cursor: pointer;
            }
          }
        }
      }
    }
</style>
