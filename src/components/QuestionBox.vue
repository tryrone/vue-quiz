<template>
  <div class="wrap">
    <b-jumbotron>
      <template v-slot:lead>
        Question here?
      </template>

      <hr class="my-4" />

      <p>
        List of answers
      </p>

      <b-button variant="primary" href="#">Submit</b-button>
      <b-button variant="success" href="#">Next</b-button>
    </b-jumbotron>
  </div>
</template>

<style>
.wrap {
  margin-top: 2em;
}
</style>
