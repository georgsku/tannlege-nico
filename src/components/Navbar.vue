<template>
  <nav >
     
      <div class="navbar-container mt-3">
        <div class="nav-btn" @click="navbarClick('#about')">
          <img src="../assets/nav/tooth.svg" alt="">
          <p>Om oss</p>
        </div>  
        <div class="nav-btn" @click="navbarClick('#calendar')">
          <img src="../assets/nav/calendar.svg" alt="">
          <p>Timebestillinger</p>
        </div>  
        <div class="navbar-logo-container">
           <img src="../assets/tooth2.svg" class="navbar-logo mt-4" alt="">
          <h1 class="font-weight-bolder m-0" style="color: #88d8e5">Tannlege</h1>
          <h4 style="color: #88d8e5; white-space: nowrap;">&mdash; Nicolay Nilssen &mdash;</h4>
        </div>
        <div class="nav-btn" @click="navbarClick('#opening-hours')">
          <img src="../assets/nav/clock-time-four.svg" alt="">
          <p>Åpningstider</p>
        </div>  
        <div class="nav-btn" @click="navbarClick('.employee')">
          <img src="../assets/nav/account-group.svg" alt="">
          <p>Ansatte</p>
        </div> 
      </div>  
  </nav>
</template>

<script>
export default {
  components: {},
  props: {},
  data() {
    return {
    }
  },
  computed: {
  },
  methods: {
    navbarClick(element) {
      document.querySelector(element).scrollIntoView({behavior: "smooth", block: "center",});
    }
  },
  mounted() {
  }
}
</script>

<style lang="scss">

  nav {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .navbar-logo-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .navbar-logo {
    height: 90px;
    width: auto;
  }

  .navbar-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  .nav-btn {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0 30px;
    cursor: pointer;

    & > p {
      font-size: 17px;
      margin: 5px 0;
      color: #88d8e5;
      font-weight: 600;
    }

    & > img {
      height: 40px;
    }

    &:hover {
      transform:  translateY(-3px);
      filter: drop-shadow(0 0.5rem 1.0rem rgba(0, 0, 0, .15));
    }
  }

  @media only screen and (max-width: 768px) {
        
    .nav-btn {
      display: none;
    }

  }

  
</style>