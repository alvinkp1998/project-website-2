<template>
  <div>
    <div
      class="modal fade bd-example-modal-lg"
      tabindex="-1"
      role="dialog"
      aria-labelledby="myLargeModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-lg large">
        <div class="modal-content">
          <div class="modal-header">
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <div class="row">
              <div class="col-md-6">
                <img :src="img" alt="kelas" class="ml-5" />
              </div>
              <div class="col-md-6">
                <h4>{{ name }}</h4>
                <button
                  @click="showText = !showText"
                  class="btn btn-primary btn-sm shadow-sm"
                >
                  Deskripsi
                </button>
                <span class="text-primary ml-2">Jadwal</span>
                <button
                  @click="showText = !showText"
                  class="btn btn-primary btn-sm shadow-sm"
                >
                  jadwal
                </button>
                <p v-show="showText" class="mt-3">{{ desc }}</p>
                <div class="mt-3" v-show="!showText">
                  <p>Mulai : 19 Agustus 2021</p>
                  <p>Selesai : 19 November 2021</p>
                </div>
              </div>
            </div>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-dismiss="modal"
            >
              Tutup
            </button>
            <button type="button" class="btn btn-primary">Lihat Kelas</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    img: { type: String },
    name: { type: String },
    desc: { type: String }
  },
  data() {
    return {
      showText: true
    };
  }
};
</script>

<style scoped>
.large {
  margin-top: 100px;
  width: 1000px;
}
</style>
