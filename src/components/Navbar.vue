<template>
  <nav
    class="navbar navbar-expand-lg navbar-light bg-light"
    style="position: sticky"
  >
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Hidden brand</a>
      <div class="search">
        <i class="bi bi-search"></i>
        <input />
        <button class="btn btn-outline-success" type="submit">Search</button>
      </div>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarToggler"
        aria-controls="navbarToggler"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="collapse navbar-collapse justify-content-end"
        id="navbarToggler"
      >
        <ul class="navbar-nav mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">사이트 소개</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">스터디</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">동호회</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">커뮤니티</a>
          </li>
        </ul>
        <div class="verticalLine"></div>
        <button class="btn btn-outline-success" type="submit">로그인</button>
        <button class="btn btn-outline-success" type="submit">회원가입</button>
      </div>
    </div>
  </nav>
</template>

<script setup></script>

<style>
.navbar {
  display: block;
  box-shadow: rgb(234 234 236) 0px 1px 0px;
  position: sticky;
  top: 0px;
  z-index: 100;
  width: 100%;
  background-color: rgba(255, 255, 255, 0.72);
  margin-bottom: 20px;
}

.search {
  display: flex;
  background-color: rgb(245, 245, 247);
  border-radius: 1rem;
  width: auto;
  border: 1px solid rgb(245, 245, 247);
  box-shadow: none;
}

.verticalLine {
  width: 1px;
  height: 16px;
  margin: 0px 1rem;
  display: block;
  background-color: rgb(234, 234, 236);
}
</style>
