<template>
  <div id="dashboard">
    <header>
      <img src="../assets/img/bft-logo.jpg" alt="BFT- Logo" />
      <a href="#">Support</a>
    </header>

    <main>
      <nav>
        <button v-on:click="setPage('users')">
          <img src="../assets/img/user-icon.jpg" alt="user-icon" />
          <span>Users</span>
        </button>
        <button v-on:click="setPage('subscriptions')">
          <img src="../assets/img/dashboard-icon.jpg" alt="dashboard-icon" />
          <span>Subscriptions</span>
        </button>
        <button v-on:click="setPage('finance')">
          <img src="../assets/img/finance-icon.jpg" alt="finance-icon" />
          <span>Finance</span>
        </button>
        <button v-on:click="setPage('calendar')">
          <img src="../assets/img/calendar-icon.jpg" alt="calendar-icon" />
          <span>Calendar</span>
        </button>
        <button v-on:click="setPage('settings')">
          <img src="../assets/img/settings-icon.jpg" alt="settings-icon" />
          <span>Settings</span>
        </button>
      </nav>

      <UsersPage v-if="showPage === 'users'"></UsersPage>

      <SubscriptionsPage
        v-if="showPage === 'subscriptions'"
      ></SubscriptionsPage>

      <FinancePage v-if="showPage === 'finance'"></FinancePage>

      <CalendarPage v-if="showPage === 'calendar'"></CalendarPage>

      <SettingsPage v-if="showPage === 'settings'"></SettingsPage>
    </main>
  </div>
</template>

<script>
import UsersPage from "./UsersPage.vue";
import SubscriptionsPage from "./SubscriptionsPage.vue";
import FinancePage from "./FinancePage.vue";
import CalendarPage from "./CalendarPage.vue";
import SettingsPage from "./SettingsPage.vue";

export default {
  name: "Dashboard",
  components: {
    UsersPage,
    SubscriptionsPage,
    FinancePage,
    CalendarPage,
    SettingsPage
  },

  data: function() {
    return {
      showPage: "users"
    };
  },
  methods: {
    setPage: function(page) {
      console.log(page);
      this.showPage = page;
    }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap");

body {
  margin: 0;
  padding: 0;
  color: #868686;
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #ffffff;
}

header img {
  width: 210px;
  height: 70px;
}

header > a {
  margin-right: 30px;
  text-decoration: none;
  color: #7e7e7e;
  font-size: 17px;
}

main {
  background-color: #f0f0f0;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  height: 91vh;
}

main > nav {
  width: 200px;
  flex-shrink: 0;
  margin-top: 30px;
}

main > nav > button {
  display: flex;
  align-items: center;
  text-decoration: none;
  line-height: 65px;
  padding-left: 40px;
  color: #7e7e7e;
  border: 0;
  outline: 0;
  background: none;
  cursor: pointer;
}

main > nav > button:hover {
  display: flex;
  align-items: center;
  text-decoration: none;
  line-height: 65px;
  padding-left: 40px;
  color: #7e7e7e;
  background-color: #ffffff;
  width: 102%;
}

main > nav > button > img {
  width: 30px;
  padding-right: 15px;
}

main .page {
  width: 100%;
  display: flex;
  justify-content: center;
}

main .page h1 {
  margin-top: 100px;
}
</style>
