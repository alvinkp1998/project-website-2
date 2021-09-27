<template>
  <div id="app">
    <div class="main-wrapper">
      <partials-navbar />
      <partials-sidebar />

      <!-- Main Content -->
      <div class="main-content">
        <section class="section">
          <div class="section-header">
            <h1>Blank Page</h1>
            <!-- <img src="@/assets/img/example-image.jpg" alt=""> -->
          </div>
          <div class="section-body">
            <Nuxt />
          </div>
        </section>
      </div>
      <partials-footer />
    </div>
  </div>
</template>
