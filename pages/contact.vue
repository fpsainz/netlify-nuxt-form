<template>
  <div class="container">
    <h1 class="title">
      Contact
    </h1>
    <div class="content">
      <v-form v-model="valid" name="contact" action="" method="post" netlify>

        <v-text-field
      v-model="name"
      :rules="nameRules"
      :counter="10"
      label="Nome:"
      required
      name="name" id="name"
    ></v-text-field>
        <v-text-field
      v-model="email"
      :rules="emailRules"
      label="Email:"
      required
      name="email" id="email"
    ></v-text-field>
        <label class="form-label" for="message">
          Message:
        </label>
        <v-textarea
          name="message" id="message"
          label="Deixe aqui o seu recado!"
          value=""
          hint="Hint text"
        ></v-textarea>
        <v-btn @click="submit" color="success" block >Send message</v-btn>
        <input type="hidden" name="form-name" value="contact" />
      </v-form>
    </div>
  </div>
</template>