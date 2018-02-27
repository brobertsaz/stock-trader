<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <router-link to="/" class="navbar-brand">Stock Trader</router-link>

    <div class="collapse navbar-collapse">
      <ul class="navbar-nav mr-auto">
        <router-link to="/portfolio" activeClass="active" tag="li" class="nav-link">Portfolio</router-link>
        <router-link to="/stocks" activeClass="active" tag="li" class="nav-link">Stocks</router-link>
      </ul>
      <ul class="navbar-nav ml-auto">
        <li class="nav-link"><a href="#">End Day</a></li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle"
             href="#"
             role="button"
             data-toggle="dropdown"
             aria-haspopup="true"
             aria-expanded="false">Save and Load</a>

          <div class="dropdown-menu" aria-labelledby="navbarDropdown">
            <a class="dropdown-item" href="#">Save Data</a>
            <a class="dropdown-item" href="#">Load Data</a>
          </div>
        </li>
      </ul>
    </div>
  </nav>
</template>
