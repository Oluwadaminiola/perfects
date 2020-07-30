<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12">
        <div class="d-flex row justify-content-end pt-2 px-3">
          <div class="ml-3 pt-2">
            <a class="fc-black" href="#">Gmail</a>
          </div>
          <div class="ml-3 pt-2">
            <a class="fc-black" href="#">Images</a>
          </div>
          <div class="ml-3 pt-2">
            <a href="#">
              <i class="fas fa-bars"></i>
            </a>
          </div>
          <div class="ml-2">
            <button class="btn btn-blue">Sign In</button>
          </div>
        </div>
      </div>
      <div class="col-lg-5 m-auto">
        <div class="mid-section d-flex row flex-column justify-content-center align-item-center">
          <div class="px-3">
            <p class="text-center">
              <a href="https://google.com" target="_blank">
                <img src="../../public/Google_logo.svg" alt />
              </a>
            </p>
            <div class="input-group search">
              <div class="input-group-prepend pl-3">
                <i class="fas fa-search"></i>
              </div>
              <input type="text" class="form-control" v-model="searchText" />
              <div class="input-group-append pr-3">
                <i class="fas fa-microphone"></i>
              </div>
            </div>
          </div>
          <div class="d-flex justify-content-center mt-3">
            <button class="btn btn-search mr-2" @click="search()">Google Search</button>
            <button class="btn btn-search" @click="perfect()">I'm Feeling Lucky</button>
            <!-- <a :href="'https://google.com/search?q=' + searchText" target="_blank">
              <button class="btn btn-secondary mr-2">Google Search</button>
            </a>
            <a href="https://perfects.engineering" target="_blank">
              <button class="btn btn-secondary">I'm Feeling Lucky</button>
            </a>-->
          </div>
          <div class="d-flex justify-content-center mt-5 row">
            <div class="mr-3">
              <p class="m-0">Google offered in:</p>
            </div>
            <div class="mr-3">
              <a href="#" class="fc-blue">Hausa</a>
            </div>
            <div class="mr-3">
              <a href="#" class="fc-blue">Igbo</a>
            </div>
            <div class="mr-3">
              <a href="#" class="fc-blue">Èdè Yorùbá</a>
            </div>
            <div class="mr-3">
              <a href="#" class="fc-blue">Nigerian Pidgin</a>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-12 px-0">
        <div class="bg-grey border-bottom py-2 px-lg-4 px-3">
          <p class="m-0 fs-15 fc-lbl">Nigeria</p>
        </div>
      </div>
      <div class="col-lg-12 px-0">
        <div class="bg-grey py-2 px-lg-3 px-2">
          <div class="row">
            <div class="col-lg-6 order-sm-1 order-2">
              <div class="d-flex row justify-content-lg-start justify-content-center px-4">
                <div class="mr-2">
                  <a href="#" class="fc-black fs-14">Advertising</a>
                </div>
                <div class="mr-2">
                  <a href="#" class="fc-black fs-14">Business</a>
                </div>
                <div class="mr-2">
                  <a href="#" class="fc-black fs-14">About</a>
                </div>
                <div class="mr-2">
                  <a href="#" class="fc-black fs-14">How Search Works</a>
                </div>
              </div>
            </div>
            <div class="col-lg-6 order-sm-2 order-1">
              <div class="d-flex row justify-content-center justify-content-lg-end px-4">
                <div class="ml-2">
                  <a href="#" class="fc-black fs-14">Privacy</a>
                </div>
                <div class="ml-2">
                  <a href="#" class="fc-black fs-14">Terms</a>
                </div>
                <div class="ml-2">
                  <a href="#" class="fc-black fs-14">Settings</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      searchText: "",
    };
  },
  components: {},
  methods: {
    search() {
      if (this.searchText == "") {
        alert("Your input field is empty");
      } else {
        window.open("https://google.com/search?q=" + this.searchText);
      }
    },
    perfect() {
      window.open("https://perfects.engineering");
    },
  },
  mounted() {
    $(document).ready(function () {
      $(".input-group.search > input")
        .focus(function (e) {
          $(this).parent().addClass("nav-input-group-focus");
        })
        .blur(function (e) {
          $(this).parent().removeClass("nav-input-group-focus");
        });
    });
  },
};
</script>