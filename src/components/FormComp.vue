<script setup lang="ts">
import { ref } from "vue";

const send = () => {
  alert("Your message has been sent!");
};
</script>

<template>
  <div class="container">
    <h1>Contact Us</h1>
    <form @submit.prevent="send">
      <div>
        <label for="fname">First Name</label>
        <input required type="text" id="fname" name="fname" placeholder="Your name.." />
      </div>

      <div>
        <label for="lname">Last Name</label>
        <input
          required
          type="text"
          id="lname"
          name="lname"
          placeholder="Your last name.."
        />
      </div>

      <div class="gg">
        <label for="email">Email Address</label>
        <input
          required
          type="email"
          name="email"
          id="email"
          placeholder="Your email.."
        />
      </div>
      <label class="gg" for="query">Query Type</label>

      <div class="rr">
        <input
          required
          class="rad"
          type="radio"
          id="general-enquiry"
          name="query-type"
          value="general-enquiry"
        />
        <label class="lab" for="general-enquiry">General Enquiry</label>
      </div>

      <div class="rr">
        <input
          required
          class="rad"
          type="radio"
          id="support-request"
          name="query-type"
          value="support-request"
        />
        <label class="lab" for="support-request">Support Request</label>
      </div>

      <div class="gg">
        <label for="message ">Message</label>
        <textarea
          required
          id="message"
          name="message"
        ></textarea>
      </div>

      <div class="gg vv ">
        <input required type="checkbox" id="consent" name="consent" />
        <label class="cons"for="consent">I consent to being contacted by the team</label>
      </div>

      <button class="gg zz" type="submit">Sumbit</button>
    </form>
  </div>
</template>

<style scoped>
form {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 10px;
}
.container {
  background-color: white;
  width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
}
.cons{
  font-size: 11px;
}
.gg {
  grid-column: 1/3;
}
.vv {
  display: grid;
  grid-template-columns: 7% 93%;
  justify-items: left;
  align-items: center;
}
.zz {
  height: 40px;
  background-color: #45a049;
  color: white;
}
.zz:hover{
  cursor: pointer;
}
.rr {
  border:  1px solid #ccc;
  width: 100%;
}
h1 {
  text-align: left;
  margin-bottom: 20px;
}

label {
  display: block;
}

input[type="text"],
input[type="email"],
textarea {
  width: 100%;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  padding: 0;
}

input[type="checkbox"] {
  margin-right: 5px;
}

input[type="submit"] {
  background-color: #4caf50;
  color: white;

  border: none;
  cursor: pointer;
  float: right;
}

input[type="submit"]:hover {
  background-color: #45a049;
}

.rad {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  width: 16px;
  height: 16px;
  border: 1px solid #ccc;
  border-radius: 50%;
  outline: none;
  cursor: pointer;
}

.rad:checked {
  background-color: #009688;
}

.lab {
  display: inline-block;
  margin-left: 5px;
  cursor: pointer;
}

@media screen and (max-width: 600px) {
  .container {
    width: 100%;
    padding: 10px;
  }

 form{
  grid-template-columns: 100%;

 }
 .gg{
  grid-column: 1/2;

 }
  
}
</style>
