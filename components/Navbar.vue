<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-warning ">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="/GoogleLogo.png" style="width: 25px" alt=""/>
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon text-white"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <nuxt-link  to="/" class="primary text-decoration-none text-white pe-4">Posts</nuxt-link>
            </li>
             <li class="nav-item">
               <nuxt-link to="/CreatePost" class="primary  text-decoration-none text-white pe-4">Create Post</nuxt-link>
             </li>
            <li>
              <nuxt-link to="/UnDraw" class="primary text-decoration-none text-white pe-4">UnDraw</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/nasted" class="primary text-decoration-none text-white">nasted</nuxt-link>
            </li>
          </ul>
          <form class="d-flex">
            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-primary" type="submit">Search</button>
          </form>
        </div>
      </div>
    </nav>
  </div>
</template>
