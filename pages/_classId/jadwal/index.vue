<template>
  <div>
    <div class="row">
      <div class="col-md-3 overflow-auto pb-5">
        <div
          class="nav flex-column nav-pills"
          id="v-pills-tab"
          role="tablist"
          aria-orientation="vertical"
        >
          <a
            class="`nav-link d-flex justify-content-between my-2 py-3"
            id="menu-schedule"
            data-toggle="pill"
            href="#content-schedule"
            role="tab"
          >
            Session 1
            <i class="fas fa-ellipsis-v pointer" data-toggle="dropdown"></i>
            <div class="dropdown-menu">
              <a class="dropdown-item" href="#">Sunting</a>
              <a class="dropdown-item" href="#">Hapus</a>
            </div>
          </a>
          <a
            class="`nav-link d-flex justify-content-between my-2 py-3"
            id="menu-schedule"
            data-toggle="pill"
            href="#content-schedule"
            role="tab"
          >
            Session 2
            <i class="fas fa-ellipsis-v pointer" data-toggle="dropdown"></i>
            <div class="dropdown-menu">
              <a class="dropdown-item" href="#">Sunting</a>
              <a class="dropdown-item" href="#">Hapus</a>
            </div>
          </a>
        </div>
        <div class="text-center">
          <nuxt-link :to="`/${$route.params.classId}/jadwal/add`"
            ><button class="btn btn-primary badge-pill btn-sm mt-3">
              <span style="font-size:14px; padding:10px">Tambah Jadwal</span>
            </button></nuxt-link
          >
        </div>
      </div>
      <div class="col-md-9">
        <div class="text-center">
          <button class="btn btn-primary badge-pill  btn-sm mt-3">
            <span style="font-size:14px; padding:10px">Tambah Materi</span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    id: { type: String, default: "materi-id" },
    type: { type: String, default: "Materi" },
    title: { type: String, default: "Judul Jadwal" },
    schedule: { type: String, default: "2021-12-24" },
    file: String,
    img: String
  }
};
</script>

<style scoped>
.pill {
  border-radius: 10px;
}
</style>
