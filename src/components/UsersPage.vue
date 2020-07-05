<template>
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
</template>

<script>
export default {
  name: "UsersPage"
};
</script>

<style>
#contacts.page {
  margin-top: 30px;
}

#contacts.page #list table {
  background-color: #ffffff;
  width: 790px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  border-collapse: collapse;
  line-height: 60px;
}

#contacts.page #list > table > thead {
  font-size: 14px;
  text-align: left;
}

#contacts.page #list > table > tbody {
  font-size: 16px;
}

#contacts.page #list > table td:nth-child(1) {
  color: #0c97a3;
  font-weight: bold;
  width: 25%;
}

#contacts.page #list > table td:nth-child(2) {
  width: 15%;
}

#contacts.page #list > table td:nth-child(3) {
  width: 40%;
}

#contacts.page #list > table td:nth-child(4) {
  width: 15%;
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
