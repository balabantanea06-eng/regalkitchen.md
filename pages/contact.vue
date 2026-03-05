
<template>

<Navbar />
<Hero title="Contact" />

<div class="container-fluid contact py-6 wow bounceInUp">
  <div class="container">
    <div class="p-md-5 p-3 bg-light rounded contact-form">

      <div class="row g-4">

        <div class="col-12">
          <small class="fw-bold text-uppercase bg-light border border-primary rounded-pill px-4 py-1 mb-3">
            {{ $t('getInTouch') }}
          </small>

          <h1 class="display-5 mb-0">
            {{ $t('contactUs') }}
          </h1>
        </div>

        <!-- Form -->
        <div class="col-md-6 col-lg-7">

          <form @submit.prevent="sendForm">

            <input
              v-model="name"
              type="text"
              class="form-control p-3 mb-4 border-primary bg-light"
              :placeholder="$t('enterName')"
              required
            />

            <input
              v-model="email"
              type="email"
              class="form-control p-3 mb-4 border-primary bg-light"
              :placeholder="$t('enterEmail')"
              required
            />

            <textarea
              v-model="message"
              rows="4"
              class="form-control p-3 mb-4 border-primary bg-light"
              :placeholder="$t('yourMessage')"
              required
            ></textarea>

            <button
              class="btn btn-primary w-100 p-3 rounded-pill"
              type="submit"
            >
              {{ $t('submitNow') }}
            </button>

          </form>

        </div>

        <!-- Contact Info -->
        <div class="col-md-6 col-lg-5">

          <div class="border border-primary p-4 rounded mb-4">
            <h5>{{ $t('address') }}</h5>
            <p>
              Str. Chișinăului 64, Cricova, Moldova
            </p>
          </div>

          <div class="border border-primary p-4 rounded mb-4">
            <h5>{{ $t('email') }}</h5>
            <p>
              regalkitch3n@gmail.com
            </p>
          </div>

          <div class="border border-primary p-4 rounded">
            <h5>{{ $t('telephone') }}</h5>
            <p>
              (+373) 611 377 74
            </p>
          </div>

        </div>

      </div>

    </div>
  </div>
</div>

<Footer />
<BackToTop />

</template>

<script setup lang="ts">

useHead({
  title: "Contact - Regal Kitchen"
})

const name = ref('')
const email = ref('')
const message = ref('')

function sendForm() {
  alert("Message sent!")

  name.value = ''
  email.value = ''
  message.value = ''
}

</script>

<style scoped>

.contact-form{
box-shadow:0 10px 25px rgba(0,0,0,0.1);
}

</style>
