<template>
  <nav class="navbar navbar-expand-lg navbar-absolute navbar-transparent">
    <!--<profile-data/>-->
    <div class="container-fluid">
      <div class="navbar-wrapper">
        <div class="navbar-toggle d-inline">
            <button type="button" class="navbar-toggler">
              <span class="navbar-toggler-bar bar1"></span>
              <span class="navbar-toggler-bar bar2"></span>
              <span class="navbar-toggler-bar bar3"></span>
            </button>
        </div>
        <a class="navbar-brand" href="javascript:void(0)">{{pagetoshow}}</a>
      </div>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navigation" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-bar navbar-kebab"></span>
        <span class="navbar-toggler-bar navbar-kebab"></span>
        <span class="navbar-toggler-bar navbar-kebab"></span>
      </button>
      <div class="collapse navbar-collapse" id="navigation">
            <ul class="navbar-nav ml-auto">
              <!--<li class="search-bar input-group">
                <button class="btn btn-link" id="search-button" data-toggle="modal" data-target="#searchModal"><i class="fa fa-search"></i>
                  <span class="d-lg-none d-md-block">Search</span>
                </button>
              </li>-->
              <li class="dropdown nav-item">
                <a href="#" class="dropdown-toggle nav-link" data-toggle="dropdown">
                  <div class="photo">
                    <img :src="profileData.avatarfull" :alt="profileData.personaname">
                  </div>
                  <b class="caret d-none d-lg-block d-xl-block"></b>
                  <p class="d-lg-none">
                    Log out
                  </p>
                </a>
                <ul class="dropdown-menu dropdown-navbar">
                  <li class="nav-link">
                    <a href="javascript:void(0)" class="nav-item dropdown-item">Log out as <span>{{profileData.personaname}}</span></a>
                  </li>
                </ul>
              </li>
              <li class="separator d-lg-none"></li>
            </ul>
          </div>
    </div>
  </nav>
</template>

<script>
  import ProfileData from "../Profile/ProfileData.vue";

  export default{
    name: "Topbar",
    props: ["pagetoshow"],
    dependencies: ["profileData"],
    components: {
      "profile-data": ProfileData
    }
  }
</script>
