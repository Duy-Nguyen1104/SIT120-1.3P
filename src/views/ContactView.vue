<template>
  <div class="contact-container">
    <h2 class="contact-header">Contact Me</h2>
    <form class="contact-form">
      <div class="form-group" v-for="(field, index) in formFields" :key="index">
        <label :for="'field-' + index">{{ field.label }}</label>
        <input type="text" :id="'field-' + index" v-model="field.value">
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" v-model="message"></textarea>
      </div>
      <button @click.prevent="submitForm">Submit</button>
    </form>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .contact {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<script>
export default {
  data() {
    return {
      formFields: [
        { label: "Name", value: "" },
        { label: "Email", value: "" },
        { label: "Phone", value: "" },
      ],
      message: "",
    };
  },
  methods: {
    submitForm() {
      console.log("Form submitted");
    },
  },
};
</script>

<style scoped>
.contact-container {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    max-width: 400px; /* Change width to max-width for responsiveness */
    margin: 0 auto; /* Center horizontally */
    text-align: center;
}

.contact-header {
    font-size: 24px;
    margin-bottom: 20px;
}

.contact-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.form-group {
    margin: 10px 0;
}

label {
    font-weight: bold;
}

input[type="text"], textarea {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 10px 20px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}
</style>
