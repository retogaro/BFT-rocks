<template>
  <div id="contacts" class="page">
    <section id="list">
      <table>
        <thead>
          <tr>
            <th>Name</th>
            <th>Gender</th>
            <th>Company</th>
            <th>Email</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="user in users"
            v-bind:key="user.index"
            v-on:click="showUser(user)"
          >
            <td>{{ user.name }}</td>
            <td>{{ user.gender }}</td>
            <td>{{ user.company }}</td>
            <td>{{ user.email }}</td>
          </tr>
        </tbody>
      </table>
    </section>

    <section id="card">
      <h2>{{ shownUser.name }}</h2>
      <h4>{{ shownUser.email }}</h4>

      <div class="contact">
        <div class="left">
          <h3>Phone</h3>
          <span>+61 431 756 223</span>
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
        <dd>{{ shownUser.gender }}</dd>
        <dt>Relationship</dt>
        <dd>Married</dd>
        <dt>Medical History</dt>
        <dd>High Cholestrol</dd>
      </dl>

      <h3>Membership</h3>
      <dl>
        <dt>Company</dt>
        <dd>{{ shownUser.company }}</dd>
        <dt>Type</dt>
        <dd>Ordinary</dd>
        <dt>Payment</dt>
        <dd>Direct Debit</dd>
      </dl>
    </section>
  </div>
</template>

<script>
export default {
  name: "UsersPage",
  data: function() {
    return {
      shownUser: {
        index: 4,
        name: "Vanessa Tanner",
        gender: "female",
        company: "TINGLES",
        email: "vanessatanner@tingles.com"
      },

      users: [
        {
          index: 0,
          name: "Jeannie Webb",
          gender: "female",
          company: "ESCHOIR",
          email: "jeanniewebb@eschoir.com"
        },
        {
          index: 1,
          name: "Jacobs Hughes",
          gender: "male",
          company: "SECURIA",
          email: "jacobshughes@securia.com"
        },
        {
          index: 2,
          name: "Knapp Parrish",
          gender: "male",
          company: "CHORIZON",
          email: "knappparrish@chorizon.com"
        },
        {
          index: 3,
          name: "Owens Livingston",
          gender: "male",
          company: "ZILLAN",
          email: "owenslivingston@zillan.com"
        },
        {
          index: 4,
          name: "Vanessa Tanner",
          gender: "female",
          company: "TINGLES",
          email: "vanessatanner@tingles.com"
        }
      ]
    };
  },
  methods: {
    showUser: function(user) {
      console.log(user.name);
      console.log(user.gender);
      this.shownUser = user;
    }
  }
};
</script>

<style>
#contacts.page {
  margin-top: 30px;
  display: flex;
  justify-content: space-evenly;
}

#contacts.page #list table {
  background-color: #ffffff;
  width: 830px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  border-collapse: collapse;
  text-align: left;
  cursor: pointer;
}

#contacts.page #list > table > thead {
  font-size: 14px;
}

#contacts.page #list > table th {
  padding: 35px 10px 20px 30px;
}

#contacts.page #list > table > tbody {
  font-size: 16px;
}

#contacts.page #list > table td {
  padding: 20px 0px 20px 30px;
}

#contacts.page #list > table td:nth-child(1) {
  color: #0c97a3;
  font-weight: bold;
}

#contacts.page #list > table > tbody > tr:hover {
  background-color: #0c97b7;
  color: #ffffff;
  outline: 4px solid #0c97b7;
  outline-style: auto;
}

#contacts.page #list > table tr:hover td:nth-child(1) {
  color: #ffffff;
  font-weight: bold;
}

#contacts.page #card {
  background-color: #ffffff;
  width: 320px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  padding: 25px 0px;
}

#contacts.page #card > img {
  margin-top: 32px;
}

#contacts.page #card .contact {
  display: flex;
  justify-content: space-evenly;
  text-align: left;
  line-height: 16px;
  margin-top: 15px;
}

#contacts.page #card .contact .left > h3 {
  font-size: 12px;
}

#contacts.page #card .contact .right > h3 {
  font-size: 12px;
}

#contacts.page #card > h3 {
  font-size: 12px;
  text-align: left;
  padding-left: 40px;
}
#contacts.page #card > h2,
#contacts.page #card > h4 {
  color: #0c838f;
  margin: 0;
  text-align: center;
}

#contacts.page #card > dl {
  display: flex;
  flex-wrap: wrap;
  font-size: 13px;
  line-height: 24px;
  text-align: left;
  padding-left: 40px;
}

#contacts.page #card > dl > dt {
  width: 45%;
}

#contacts.page #card > dl > dd {
  width: 55%;
  margin: 0;
}
</style>
