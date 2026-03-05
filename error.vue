<template>
  <Navbar />
  <Hero title="404" />

  <!-- 404 Start -->
  <div class="container-fluid py-6 wow fadeInUp" data-wow-delay="0.1s">
    <div class="container text-center">
      <div class="row justify-content-center">
        <div class="col-lg-6">

          <i class="bi bi-exclamation-triangle display-1 text-primary"></i>

          <h1 class="display-1">404</h1>

          <h2 class="mb-4">Page Not Found</h2>

          <p class="mb-4">
            Sorry, the page you are looking for does not exist.
            Please return to the home page.
          </p>

          <NuxtLink
            to="/"
            class="btn btn-primary rounded-pill py-3 px-5"
          >
            Go Back Home
          </NuxtLink>

        </div>
      </div>
    </div>
  </div>
  <!-- 404 End -->

  <Footer />
  <BackToTop />
</template>

<script lang="ts" setup>
useHead({
  title: "404 - Page Not Found"
})
</script>

<style scoped>

</style>
