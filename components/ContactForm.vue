<template>
  <div class="contact-form">   
   <form action="#" method="post">
  <h1>Contact Us</h1>
  <div class="column">
    <label for="the-name">Your Name</label>
    <input type="text" name="name" id="the-name">

    <label for="the-email">Email Address</label>
    <input type="email" name="email" id="the-email">
  </div>
    <label for="the-message">Message</label>
    <textarea name="message" id="the-message"></textarea>
    <label>
    <input type="checkbox" name="newsletter" value="yes"> Join our mailing list?
    </label>
    <input type="submit" value="Send Message">
</form>
  </div>
</template>

<style scoped>
.contact-form{
    padding:20px;
    min-width: 500px;
}
h1, p{
  text-align: center;
}
label{
  display:block;
  margin:1em 0 .2em;
}
/* single-line text, checkbox, and button */
input, select, textarea{
  display:block;
  width:100%;
  padding:.3em;
  font-size:20px;
  background-color:#fbfbfb;
  border:solid 1px #CCC;
  resize:vertical;
}
textarea{
  min-height:180px;
}
select{
  color:indigo;
}
option{
  color:blue;
  background: lavenderBlush;
}
input[type=checkbox]{
  display:inline;
  width:auto;
  color:red;
}

input[type=submit]{
  background: #1a1e66;;
  margin:1em 0 0;
  color:white;
  border:none;
  border-radius:8px;
  transition:all .3s ease-out;
}

/* hover and focus states */
input[type=submit]:hover,
input[type=submit]:focus{
  outline:none;
}

@media screen and (min-width:600px) {
  /*  make the form 2 columns */
  form:after{
    content:'';
    display:block;
    clear:both;
  }
}
</style>