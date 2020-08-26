<template>
  <div class="columns is-mobile">
    <div class="column is-one-quarter px-6">
      <div class="box is-rounded">
        <UploadField />
        <template>
          <section class="mt-4">
            <b-input class="is-small" placeholder="Email para envio"></b-input>
          </section>
          <section class="mt-2">
            <b-input placeholder="O seu email"></b-input>
          </section>
          <section class="mt-2">
            <b-input maxlength="200" type="textarea" placeholder="Sua mensagem"></b-input>
          </section>
        </template>
        <template>
          <section>
            <b-button @click="clickMe" class="is-primary">Transferir</b-button>
          </section>
        </template>
        <template>
          <section>

          </section>
        </template>
      </div>
    </div>
    <div class="column is-three-quarters">
      <div class="content">
        <img src="https://images.unsplash.com/photo-1598362731390-688d8f803a33?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=675&q=80" alt="Unsplash">
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import UploadField from "@/components/UploadField.vue";

export default {
  name: "Home",
  components: {
    UploadField
  },
  methods: {
    clickMe() {
      this.$buefy.notification.open('Transferência iniciada')
    }
  }
};
</script>

<style lang="scss" scoped>
.box {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}

</style>
