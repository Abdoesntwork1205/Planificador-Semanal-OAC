<template>
  <div class="modal fade" id="aboutModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">{{ $t("about.about") }}</h5>
          <i class="bi-x close-modal" data-bs-dismiss="modal"></i>
        </div>
        <div class="modal-body">
          <div class="d-flex flex-column" style="text-align: center; margin-top: 10px">
            <img
              class="logo align-self-center"
              src="/img/weektodo-isologo-color.svg"
              alt="WeekToDo"
              title="WeekToDo Logo"
              width="256"
            />
            <img
              class="logo logo-white align-self-center"
              src="/img/weektodo-isologo-white.svg"
              alt="WeekToDo"
              title="WeekToDo Logo"
              width="256"
            />
            <!-- <h5 style="margin-top: 15px; margin-bottom: 2px;">WeekToDo</h5> -->
            <span class="mt-3" style="font-size: 0.75rem"
              >{{ $t("about.version") }} {{ version }} •
              <a
              >
                {{ $t("ui.changeLog") }}
              </a>
            </span>
            <span>
              <div class="visit-site mt-2 mb-3" style="font-size: 0.75rem">
                <a href="https://linktr.ee/fleetwood.vzla" target="_blank">{{ $t("about.site") }}</a>
              </div>
            </span>
            <div class="d-flex align-self-center">
              <a href="https://www.instagram.com/abdoesntwork/" target="_blank" title="Instagram"> <i class="bi-rss mx-2"></i></a>
              <!-- <a href="https://twitter.com/abdoesntwork" target="_blank" title="Twitter"> <i class="bi-twitter mx-2"></i></a> -->
              <a href="https://github.com/Abdoesntwork1205" target="_blank" title="Github">
                <i class="bi-github mx-2"></i
              ></a>
              <a href="mailto:abdielasad12@gmail.com"> <i class="bi-envelope mx-2" :title="$t('about.email')"></i></a>
            </div>
          </div>
          <div class="horizontal-divider mt-3 mb-3"></div>
          <div>
            <div style="margin-top: -5px">
              <div class="row">
                <a href="https://github.com/Abdoesntwork1205" target="_blank" class="row" style="text-decoration: none">
                  <div class="col-md-3 d-flex justify-content-center align-items-center">
                    <img
                      style="display: block; margin-left: 70px;"
                      src="Avatar.webp"
                      alt="Abdiel Urbina"
                      title="Abdiel Urbina"
                      width="64"
                    />
                  </div>
                  <div class="col-md-9 pt-3 text-md-left text-center" style="margin-top: -5px;">
                    <h6 class="mb-1">{{ $t("about.devName") }}</h6>
                    <div style="font-size: 0.7rem; opacity: 0.7">{{ $t("about.dev") }}</div>
                  </div>
                </a>
              </div>
              <div
                class="text-center text-uppercase px-2 d-flex justify-content-center flex-wrap"
                style="font-size: 0.8rem; opacity: 0.8; line-height: 10px"
              >
              </div>
              <div class="horizontal-divider mt-2 mb-3"></div>
              <div class="d-flex justify-content-center">
                <span style="margin-top: 10px; right-top: 10px;"
                  >{{ $t("about.madeWith") }} <i class="bi-heart-fill" style="color: red"></i> {{ $t("about.inVenezuela") }}</span
                >

              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <sponsor-modal ref="sponsorsModal"></sponsor-modal>
  <collaborators-modal ref="collaboratorsModal"></collaborators-modal>
</template>

<script>
import version_json from "../../public/version.json";

export default {
  name: "aboutModal",
  data() {
    return {
      version: version_json.version,
    };
  },
};
</script>

<style scoped>
.modal-dialog {
  max-width: 360px;
}

a,
a:hover {
  color: unset;
}

.visit-site {
  cursor: pointer;
}
</style>

<style>
.logo-white {
  display: none;
}

.dark-theme {
  .modal-dialog .logo {
    display: none;
  }
  .modal-dialog .logo-white {
    display: block;
    opacity: 0.95;
  }
}
</style>
