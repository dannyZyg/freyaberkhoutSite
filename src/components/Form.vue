<template>
<div>
<form 
  name="contact"
  method="post"
  v-on:submit.prevent="handleSubmit"
  action="/success/"
  data-netlify="true"
  data-netlify-honeypot="bot-field"
>
  <input type="hidden" name="form-name" value="contact" />
  <p hidden>
    <label>
      Don’t fill this out: <input name="bot-field" />
    </label>
  </p>
  <div class="sender-info">
    <div>
      <label for="first-name" class="label" >First Name</label>
      <input type="text" name="first name" v-model="formData.firstName" required/>
    </div>
    <div>
      <label for="last-name" class="label" >Last Name</label>
      <input type="text" name="last name" v-model="formData.lastName" required/>
    </div>
    <div>
      <label for="email">Your email</label>
      <input type="email" name="email" v-model="formData.email" required/>
    </div>
  </div>
  <div>
    <label for="subject">Subject</label>
    <input type="text" name="subject" v-model="formData.subject" required/>
  </div>
  <div class="message-wrapper">
    <label for="message">Message</label>
    <textarea name="message" v-model="formData.message" required></textarea>
  </div>

  <button type="submit">Submit form</button>
</form>
</div>
</template>

<script>
export default {
  data() {
    return {
      formData: {},
    }
  }
}
</script>
