<template>
  <div>
    <div class="container-scroller">
      <!-- partial:partials/_navbar.html -->
      <partials-navbar />
      <!-- partial -->
      <div class="container-fluid page-body-wrapper">
        <!-- partial:partials/_sidebar.html -->
        <partials-sidebar />
        <!-- partial -->
        <div class="main-panel">
          <div class="content-wrapper">
            <div class="page-header">
              <h3 class="page-title">
                <span
                  class="page-title-icon bg-gradient-primary text-white mr-2"
                >
                  <i class="mdi mdi-home"></i>
                </span>
                Fullstack Academy
              </h3>
            </div>
            <div class="card">
              <div class="card-body">
                <Nuxt />
              </div>
            </div>
          </div>
          <!-- content-wrapper ends -->
          <!-- partial:partials/_footer.html -->
          <partials-footer />
          <!-- partial -->
        </div>
        <!-- main-panel ends -->
      </div>
      <!-- page-body-wrapper ends -->
    </div>
  </div>
</template>

<style scoped>
.card {
  border-radius: 20px;
}
</style>
