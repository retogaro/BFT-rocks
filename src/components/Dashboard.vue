<template>
  <div id="dashboard">
    <header>
      <img src="../assets/img/bft-logo.jpg" alt="BFT- Logo" />
      <a href="#">Support</a>
    </header>

    <main>
      <nav>
        <a href="#">
          <img src="../assets/img/user-icon.jpg" alt="user-icon" />
          <span>Users</span>
        </a>
        <a href="#">
          <img src="../assets/img/dashboard-icon.jpg" alt="dashboard-icon" />
          <span>Dashboard</span>
        </a>
        <a href="#">
          <img src="../assets/img/finance-icon.jpg" alt="finance-icon" />
          <span>Finance</span>
        </a>
        <a href="#">
          <img src="../assets/img/calendar-icon.jpg" alt="calendar-icon" />
          <span>Calendar</span>
        </a>
        <a href="#">
          <img src="../assets/img/settings-icon.jpg" alt="settings-icon" />
          <span>Settings</span>
        </a>
      </nav>

      <div id="contacts" class="page">
        <section id="list">
          <table>
            <thead>
              <tr>
                <th>Name</th>
                <th>Company</th>
                <th>Email</th>
                <th>ID</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Jennie Webb</td>
                <td>Eschoir</td>
                <td>Jenniewebb@eschoir.com</td>
                <td>123</td>
              </tr>
              <tr>
                <td>Jacob hughes</td>
                <td>Securia</td>
                <td>Jacobhughes@securia.com</td>
                <td>456</td>
              </tr>
              <tr>
                <td>Knapp Parish</td>
                <td>Chorizon</td>
                <td>Knappparish@chorison.com</td>
                <td>789</td>
              </tr>
              <tr>
                <td>Owen Livingston</td>
                <td>Zillan</td>
                <td>Owenlivingston@zillan.com</td>
                <td>987</td>
              </tr>
              <tr>
                <td>Vanessa Tanner</td>
                <td>Tingles</td>
                <td>Vanessatanner@tingles.com</td>
                <td>654</td>
              </tr>
            </tbody>
          </table>
        </section>

        <section id="card">
          <img
            src="../assets/img/jacob-hughes-picture.jpg"
            alt="Jacob-hughes-picture"
          />
          <h2>Jacob Hughes</h2>
          <h4>jacobhughes@securia.com</h4>

          <div class="contact">
            <div class="left">
              <h3>Phone</h3>
              <span>+61 123 456 789</span>
            </div>
            <div class="right">
              <h3>Location</h3>
              <span>Cheltenham</span>
            </div>
          </div>

          <h3>Personal Details</h3>
          <dl>
            <dt>DOB</dt>
            <dd>16 January 1991</dd>
            <dt>Gender</dt>
            <dd>Male</dd>
            <dt>Relationship</dt>
            <dd>Married</dd>
            <dt>Medical History</dt>
            <dd>High Cholestrol</dd>
          </dl>

          <h3>Membership</h3>
          <dl>
            <dt>Type</dt>
            <dd>Ordinary</dd>
            <dt>Payment</dt>
            <dd>Direct Debit</dd>
          </dl>
        </section>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "Dashboard"
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

main > nav > a {
  display: flex;
  align-items: center;
  text-decoration: none;
  line-height: 65px;
  padding-left: 40px;
  color: #7e7e7e;
}

main > nav > a:hover {
  display: flex;
  align-items: center;
  text-decoration: none;
  line-height: 65px;
  padding-left: 40px;
  color: #7e7e7e;
  background-color: #ffffff;
  width: 102%;
}

main > nav > a > img {
  width: 30px;
  padding-right: 15px;
}

main .page {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: flex-start;
}

#contacts {
  margin-top: 30px;
}

#list table {
  background-color: #ffffff;
  width: 790px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  border-collapse: collapse;
  line-height: 60px;
}

#list > table > thead {
  font-size: 14px;
  text-align: left;
}

#list > table > tbody {
  font-size: 16px;
}

#list > table td:nth-child(1) {
  color: #0c97a3;
  font-weight: bold;
  width: 25%;
}

#list > table td:nth-child(2) {
  width: 15%;
}

#list > table td:nth-child(3) {
  width: 40%;
}

#list > table td:nth-child(4) {
  width: 15%;
}

#list > table > tbody > tr:hover {
  background-color: #0c97b7;
  color: #ffffff;
  outline: 4px solid #0c97b7;
  outline-style: auto;
}

#list > table tr:hover td:nth-child(1) {
  color: #ffffff;
  font-weight: bold;
}

#card {
  background-color: #ffffff;
  width: 320px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

#card > img {
  margin-top: 32px;
}

#card .contact {
  display: flex;
  justify-content: space-evenly;
  text-align: left;
  line-height: 16px;
  margin-top: 15px;
}

#card .contact .left > h3 {
  font-size: 12px;
}

#card .contact .right > h3 {
  font-size: 12px;
}

#card > h3 {
  font-size: 12px;
  text-align: left;
  padding-left: 40px;
}
#card > h2,
h4 {
  color: #0c838f;
  margin: 0;
  text-align: center;
}

#card > dl {
  display: flex;
  flex-wrap: wrap;
  font-size: 13px;
  line-height: 24px;
  text-align: left;
  padding-left: 40px;
}

#card > dl > dt {
  width: 45%;
}

#card > dl > dd {
  width: 55%;
  margin: 0;
}
</style>
