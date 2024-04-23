<template>
  <div class="container-contact">
    <h2 class="title">Contact me</h2>

    <span class="contact-message"><message-contact /></span>

    <form action="#" class="form">
      <input class="input" name="name" placeholder="Enter your name" required type="text" maxlength="100" />
      
      <input class="input" name="email" placeholder="Enter a valid email address" required type="email" />

      <textarea class="input" name="message" placeholder="Enter your message" required rows="4" cols="50"></textarea>

      <div class="u-form-group u-form-submit u-label-none">
        <a href="#" class="btn-primary">Submit</a>
      </div>

      <div class="notify-success">Thank you! Your message has been sent.</div>
      <div class="notify-error">Unable to send your message. Please fix errors then try again.</div>      
    </form>
  </div>
</template>

<script setup>
import MessageContact from "./MessageContact.vue";
</script>
