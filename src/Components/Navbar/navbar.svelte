<script>
	import { Link } from 'svelte-routing';
</script>

<header
  id="header"
  class="fixed-top d-flex align-items-center header-transparent"
>
  <div class="container d-flex align-items-center justify-content-between">
    <div class="logo">
        <Link to="/"><h1><span>Articulos</span></h1></Link>
    </div>

    <nav id="navbar" class="navbar">
      <ul>
      <Link to="/" class="nav-link scrollto active">  <li><a class="nav-link scrollto active" href="#hero">Home</a></li></Link>

       <!-- svelte-ignore a11y-missing-attribute -->
       <Link to="/Articulo"> <li><a class="nav-link scrollto">Articulos</a></li></Link>
       <Link to="/Contacto"> <li><a class="nav-link scrollto" href="#gallery">Contacto</a></li></Link>
        <li><a class="nav-link scrollto" href="#team">service</a></li>
        <li><a class="nav-link scrollto" href="#pricing"></a></li>
        <li class="dropdown">
          <a href="#"><span>Drop Down</span> <i class="bi bi-chevron-down" /></a
          >
          <ul>
            <li><a href="#">Drop Down 1</a></li>
            <li class="dropdown">
              <a href="#"
                ><span>Deep Drop Down</span>
                <i class="bi bi-chevron-right" /></a
              >
              <ul>
                <li><a href="#">Deep Drop Down 1</a></li>
                <li><a href="#">Deep Drop Down 2</a></li>
                <li><a href="#">Deep Drop Down 3</a></li>
                <li><a href="#">Deep Drop Down 4</a></li>
                <li><a href="#">Deep Drop Down 5</a></li>
              </ul>
            </li>
            <li><a href="#">Drop Down 2</a></li>
            <li><a href="#">Drop Down 3</a></li>
            <li><a href="#">Drop Down 4</a></li>
          </ul>
        </li>
      </ul>
      <i class="bi bi-list mobile-nav-toggle" />
    </nav>
    <!-- .navbar -->
  </div>
</header>

<style>
  #header {
    height: 80px;
    transition: all 0.5s;
    z-index: 997;
    transition: all 0.5s;
    background: rgba(255, 255, 255, 0.9);
  }

  #header.header-transparent {
    background: transparent;
  }

  #header.header-scrolled {
    background: rgba(255, 255, 255, 0.9);
    height: 60px;
  }

  #header .logo h1 {
    font-size: 28px;
    margin: 0;
    padding: 0;
    line-height: 1;
    font-weight: 700;
  }

  #header .logo h1 a,
  #header .logo h1 a:hover {
    color: rgb(7, 7, 7);
    text-decoration: none;
  }

  #header .logo img {
    padding: 0;
    margin: 0;
    max-height: 40px;
  }

  /*--------------------------------------------------------------
# Navigation Menu
--------------------------------------------------------------*/
  /**
* Desktop Navigation 
*/
  .navbar {
    padding: 0;
  }

  .navbar ul {
    margin: 0;
    padding: 0;
    display: flex;
    list-style: none;
    align-items: center;
  }

  .navbar li {
    position: relative;
  }

  .navbar a,
  .navbar a:focus {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 0 10px 30px;
    font-size: 15px;
    font-weight: 500;
    font-family: "Poppins", sans-serif;
    color: rgb(255, 255, 255);
    white-space: nowrap;
    transition: 0.3s;
  }

  .navbar a i,
  .navbar a:focus i {
    font-size: 12px;
    line-height: 0;
    margin-left: 5px;
  }

  .navbar > ul > li > a:before {
    content: "";
    position: absolute;
    width: 0;
    height: 2px;
    bottom: 3px;
    left: 30px;
    background-color: #fff;
    visibility: hidden;
    width: 0px;
    transition: all 0.3s ease-in-out 0s;
  }

  .navbar a:hover:before,
  .navbar li:hover > a:before,
  .navbar .active:before {
    visibility: visible;
    width: 25px;
  }

  .navbar a:hover,
  .navbar .active,
  .navbar .active:focus,
  .navbar li:hover > a {
    color: rgb(255, 255, 255);
  }

  .navbar .dropdown ul {
    display: block;
    position: absolute;
    left: 30px;
    top: calc(100% + 30px);
    margin: 0;
    padding: 10px 0;
    z-index: 99;
    opacity: 0;
    visibility: hidden;
    background: rgb(0, 0, 0);
    box-shadow: 0px 0px 30px rgba(127, 137, 161, 0.25);
    transition: 0.3s;
    border-radius: 4px;
  }

  .navbar .dropdown ul li {
    min-width: 200px;
  }

  .navbar .dropdown ul a {
    padding: 10px 20px;
    font-size: 14px;
    font-weight: 500;
    text-transform: none;
    color: #ffffff;
  }

  .navbar .dropdown ul a i {
    font-size: 12px;
  }

  .navbar .dropdown ul a:hover,
  .navbar .dropdown ul .active:hover,
  .navbar .dropdown ul li:hover > a {
    color: #ffffff;
  }

  .navbar .dropdown:hover > ul {
    opacity: 1;
    top: 100%;
    visibility: visible;
  }

  .navbar .dropdown .dropdown ul {
    top: 0;
    left: calc(100% - 30px);
    visibility: hidden;
  }

  .navbar .dropdown .dropdown:hover > ul {
    opacity: 1;
    top: 0;
    left: 100%;
    visibility: visible;
  }

  @media (max-width: 1366px) {
    .navbar .dropdown .dropdown ul {
      left: -90%;
    }

    .navbar .dropdown .dropdown:hover > ul {
      left: -100%;
    }
  }

  /**
* Mobile Navigation 
*/
  .mobile-nav-toggle {
    color: rgb(255, 255, 255);
    font-size: 28px;
    cursor: pointer;
    display: none;
    line-height: 0;
    transition: 0.5s;
  }

  @media (max-width: 991px) {
    .mobile-nav-toggle {
      display: block;
    }

    .navbar ul {
      display: none;
    }
  }

  .navbar-mobile {
    position: fixed;
    overflow: hidden;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background: rgba(255, 255, 255, 0.9);
    transition: 0.3s;
    z-index: 999;
  }

  .navbar-mobile .mobile-nav-toggle {
    position: absolute;
    top: 15px;
    right: 15px;
  }

  .navbar-mobile ul {
    display: block;
    position: absolute;
    top: 55px;
    right: 15px;
    bottom: 15px;
    left: 15px;
    padding: 10px 0;
    border-radius: 8px;
    background-color: rgb(255, 255, 255);
    overflow-y: auto;
    transition: 0.3s;
  }

  .navbar-mobile > ul > li > a:before {
    left: 20px;
  }

  .navbar-mobile a,
  .navbar-mobile a:focus {
    padding: 10px 20px;
    font-size: 15px;
    color: #0205a1;
  }

  .navbar-mobile a:hover,
  .navbar-mobile .active,
  .navbar-mobile li:hover > a {
    color: #3f43fd;
  }

  .navbar-mobile .getstarted,
  .navbar-mobile .getstarted:focus {
    margin: 15px;
  }

  .navbar-mobile .dropdown ul,
  .navbar-mobile .dropdown .dropdown ul {
    position: static;
    display: none;
    margin: 10px 20px;
    padding: 10px 0;
    z-index: 99;
    opacity: 1;
    visibility: visible;
    background: rgb(255, 255, 255);
    box-shadow: 0px 0px 30px rgba(127, 137, 161, 0.25);
  }

  .navbar-mobile .dropdown ul li,
  .navbar-mobile .dropdown .dropdown ul li {
    min-width: 200px;
  }

  .navbar-mobile .dropdown ul a,
  .navbar-mobile .dropdown .dropdown ul a {
    padding: 10px 20px;
  }

  .navbar-mobile .dropdown ul a i,
  .navbar-mobile .dropdown .dropdown ul a i {
    font-size: 12px;
  }

  .navbar-mobile .dropdown ul a:hover,
  .navbar-mobile .dropdown ul .active:hover,
  .navbar-mobile .dropdown ul li:hover > a,
  .navbar-mobile .dropdown .dropdown ul a:hover,
  .navbar-mobile .dropdown .dropdown ul .active:hover,
  .navbar-mobile .dropdown .dropdown ul li:hover > a {
    color: #ffffff;
  }

  .navbar-mobile .dropdown > .dropdown-active,
  .navbar-mobile .dropdown .dropdown > .dropdown-active {
    display: block;
  }
</style>
