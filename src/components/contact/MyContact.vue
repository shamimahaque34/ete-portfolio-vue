<template>
   <div class="container">
      <div class="row">
        <div class="col-md-6 details-left connect-info">
          <div class="info-item">
            <strong>Phone</strong>
            <p class="mb-0">+880 1313 924 759</p>
          </div>

          <div class="info-item">
            <strong>Email</strong>
            <p class="mb-0">haqueshamima34@gmail.com</p>
          </div>

          <div class="info-item">
            <strong>Address</strong>
            <p class="mb-0">68/8-B,Zigatola,Dhanmondi,Dhaka-1209,Bangladesh</p>
          </div>
        </div>

        <div class="col-md-6">
          <form class="contact-form">
            <input type="text" name="name" placeholder="Your name" />
            <input type="text" name="email" placeholder="Your email" />
            <textarea
              name="message"
              rows="4"
              placeholder="Your message"
            ></textarea>

            <button type="submit" name="send" class="main-button">
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </template>
  
  
  <script>
  export default{
    name:'MyContact',
    components:{}
  }
  </script>
  
  
  <style scoped>
  
  </style>
  