<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-secondary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="/GoogleLogo.png" style="width: 50px" alt=""/>
        </a>
        <button class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent"
                aria-expanded="false"
                aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <nuxt-link  to="/" class="btn-outline-primary p-4 text-decoration-none text-white">Posts</nuxt-link>
            </li>
             <li class="nav-item">
               <nuxt-link to="/CreatePost" class="btn-outline-primary p-4 text-decoration-none text-white">Create Post</nuxt-link>
             </li>
            <li>
              <nuxt-link to="/UnDraw" class="btn-outline-primary p-4 text-decoration-none text-white">UnDraw</nuxt-link>
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
