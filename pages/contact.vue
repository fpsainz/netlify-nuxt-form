<template>
  <v-container grid-list-md>
    <h1 class="title">
      Contact
    </h1>
      <v-form v-model="valid" name="contact"
      action="/thank-you"
      netlify-honeypot="bot-field"
      method="post" netlify>
        <input type="hidden" name="form-name" value="contact" />
        <p class="hidden">     
          <label>Don’t fill this out: <input name="bot-field"></label>   
        </p> 
        <v-text-field
            v-model="name"
            :rules="nameRules"
            :counter="10"
            label="Nome:"
            required
            class="form-field"
            name="name" id="name"
        ></v-text-field>
        <v-text-field
            v-model="email"
            :rules="emailRules"
            label="Email:"
            required
            class="form-field"
            name="email" id="email"
        ></v-text-field>
        <label class="form-label" for="message">
          Message:
        </label>
        <v-textarea
            class="form-field"
            name="message" id="message"
            label="Deixe aqui o seu recado!"
            value=""
            hint="Hint text"
        ></v-textarea>
        <v-btn class="form-button" 
        type="submit" 
        value="Send message" 
        color="success" block >Send message</v-btn>
      </v-form>
  </v-container>
</template>