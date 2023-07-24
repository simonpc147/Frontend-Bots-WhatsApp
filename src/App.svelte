  <script>
// @ts-nocheck

  
    function sidebarActive() {
      document.querySelector(".sb-nav-fixed").classList.toggle("sb-sidenav-toggled")
    }

    function darking() {

    let button = document.querySelector("#darking");
    let buttons = document.querySelector("#dark");

    let titles = document.querySelectorAll("#barra-titulo, #sidenavAccordion, #whatsapp-One, #conexiones-One, #contactos-One, #respuesta-One, #soporte-One, #equipo-One, #chatbots-One, #campaña-One, #informes-One, #configuracion-One, #wps, #notificacion, #mensaje, #icon, #cuenta2");
    let secciones = document.querySelectorAll(".text-h5, .container-seccion, .container-one, .title-active, .two, .subtitle, .buscador2, .jss103, .jss104, .container-two, .title-seccion, .MuiTableCell-head, .multitablet, .container-prymary, .parrafo, .buscador3")


    if (buttons.classList.contains("bi-brightness-low-fill")) {
      console.log("golll");
      buttons.classList.replace("bi-brightness-low-fill", "bi-brightness-low");
    } else {
      console.log("niiii");
      buttons.classList.replace("bi-brightness-low", "bi-brightness-low-fill");
    }

    for (let i = 0; i<titles.length; i++ ){
        titles[i].classList.toggle("active");
    }

    for (let i = 0; i<secciones.length; i++ ){
        secciones[i].classList.toggle("active");
    }
}

    let active = 0;
    let activacion = 1;
    let activaciones = 1;

        




  </script>

<div class="sb-nav-fixed">
  <!-- H E A D E R  P R I N C I P A L -->
          <nav class="sb-topnav navbar navbar-expand navbar-dark bg-dark " id="barra-titulo">
              <!-- Barra de Titulo-->
              <a class="navbar-brand ps-3" id="wps" href="#a">Whatsapp/Technojet </a>
              <!-- Barra de Menus-->
              <button class="btn btn-link btn-sm order-1 order-lg-0 me-4 me-lg-0" on:click={sidebarActive} id="sidebarToggle">
                <i class="bi bi-list"></i>
              </button>
              <!-- Boton de Dark-->
              <ul class="navbar-nav d-none d-md-inline-block form-inline ms-auto me-3 me-3 my-1 my-md-0" >
                  <li class="nav-item dropdown">
                      <a href="#a"  id="darking" on:click={darking} style="padding-left: var(--bs-navbar-nav-link-padding-x); padding-right: var(--bs-navbar-nav-link-padding-x);">
                        <i id="dark" class="bi bi-brightness-low"></i>
                        <!-- <i class="bi bi-brightness-low-fill"></i> OSCURO -->
                      </a>
                  </li>
              </ul>
               <!-- Boton de Notificacion-->
              <ul class="navbar-nav ms-auto ms-md-0 me-3 me-lg-4">
                  <li class="nav-item dropdown">
                      <a href="#a"  style="padding-left: var(--bs-navbar-nav-link-padding-x); padding-right: var(--bs-navbar-nav-link-padding-x);">
                          <i class="bi bi-bell" id="notificacion"></i>
                      </a>
                  </li>
              </ul>
               <!-- Boton de Mensajes-->
               <ul class="navbar-nav ms-auto ms-md-0 me-3 me-lg-4">
                  <li class="nav-item dropdown">
                      <a href="#a"  style="padding-left: var(--bs-navbar-nav-link-padding-x); padding-right: var(--bs-navbar-nav-link-padding-x);">
                          <i class="bi bi-chat-left-text" id="mensaje"></i>
                      </a>
                  </li>
              </ul>
               <!-- Navbar-->
              <ul class="navbar-nav ms-auto ms-md-0 me-3 me-lg-4">
                  <li class="nav-item dropdown">
                      <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                        <i class="bi bi-person-circle"></i>
                      </a>
                      <ul class="dropdown-menu dropdown-menu-end" id="cuenta2" aria-labelledby="navbarDropdown">
                          <li><a class="dropdown-item" href="#!"> Nombre de la persona.. </a></li>
                          <li><a class="dropdown-item" on:click={()=> active = 10} href="#!">Configuracion de cuenta</a></li>
                          <li><hr class="dropdown-divider" /></li>
                          <div>
                              <a class="button-salida" href="#!">
                                  <i class="bi bi-box-arrow-right"></i>
                                  Cerrar sección
                              </a>
                          </div>
                      </ul>
                  </li>
              </ul>
          </nav>
  <!--F I N  H E A D E R  P R I N C I P A L -->
  
  <!--  B A R R A  L A T E R A L -->
          <div id="layoutSidenav">
              <div id="layoutSidenav_nav">
  
                  <nav class="sb-sidenav accordion sb-sidenav-dark" id="sidenavAccordion">
                      <div class="sb-sidenav-menu">
                          <div class="nav">
  <!-- PRINCIPAL -->
                          <div class="sb-sidenav-menu-heading">Principal</div>
                              
                              <a class="nav-link" on:click={()=> active = 0} id="whatsapp-One" data-target="#whatsapp" href="#a">
                                  <div class="sb-nav-link-icon" ><i class="bi bi-whatsapp"></i></div>
                                  Whatsapp
                              </a>
                             
                              <a class="nav-link" on:click={()=> active = 1}  id="conexiones-One" data-target="#conexiones" href="#a">
                                
                                  <div class="sb-nav-link-icon" ><i class="bi bi-arrow-left-right"></i></div>
                                  Conexiones
                              </a>
                            
                              <a class="nav-link" on:click={()=> active = 2}  id="contactos-One" data-target="#contactos" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-person-rolodex"></i></div>
                                  Contactos
                              </a>
                              <a class="nav-link" on:click={()=> active = 5} id="respuesta-One" data-target="#documentos" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-card-text"></i></div>
                                  Documentos
                              </a>
                              <a class="nav-link" on:click={()=> active = 4} id="respuesta-One" data-target="#respuesta" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-card-text"></i></div>
                                  Respuestas rápidas
                              </a>
                              <!-- <a class="nav-link" on:click={()=> active = 5} id="soporte-One" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-person-fill-gear"></i></div>
                                 Soporte
                              </a> -->
  <!-- ADMINISTRACION -->
                          <div class="sb-sidenav-menu-heading">Administración</div>
  
                              <a class="nav-link" on:click={()=> active = 6} id="equipo-One" data-target="#equipo" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-people-fill"></i></div>
                                 Equipo
                              </a>
                              <a class="nav-link" on:click={()=> active = 7} id="chatbots-One" data-target="#chatbots" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-robot"></i></div>
                                 Chatbots
                              </a>
                              <a class="nav-link" on:click={()=> active = 8} id="campaña-One" data-target="#campaña" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-person-fill-gear"></i></div>
                                 Campaña
                              </a>
                              <!-- <a class="nav-link"  data-target="#suscripcion" href="#">
                                  <div class="sb-nav-link-icon"><i class="bi bi-person-fill-gear"></i></div>
                                 Suscripción
                              </a> -->
                              <a class="nav-link" on:click={()=> active = 9} id="informes-One" data-target="#informes" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-person-fill-gear"></i></div>
                                 Informes
                              </a>
                              <a class="nav-link" on:click={()=> active = 10} id="configuracion-One" data-target="#configuracion" href="#a">
                                  <div class="sb-nav-link-icon"><i class="bi bi-person-fill-gear"></i></div>
                                 Configuración
                              </a>
                              <!-- <a class="nav-link footer-vacio" >
                                <div class="sb-nav-link-icon"></div>
                              </a> -->
  
                          </div>
                      </div>
                  </nav>
              </div>
  <!--  F I N  B A R R A  L A T E R A L -->
  
  
              <div id="layoutSidenav_content">
  
  
  <!-- Whatsapp -->
                  <div class="container-fluid px-4 {active === 0 ? 'active' : ''}" data-content id="whatsapp">
                      <main>
                          <div class="contenedorP">
                              <div class="contenedorP-container">
  
                              <div class="panel-1">
                                      <div class="card mb-4 container-one three8">
                                          <div class="card-header">
                                              <ul class="nav-tabs">
                                                  <li class="nav-item" on:click={()=> activacion = 1} id="abierto">
                                                      <i class="bi bi-envelope-paper-fill two"></i>
                                                      <a href="#a" class="title-active">Abiertos</a>
                                                  </li>
                                                  <li class="nav-item" on:click={()=> activacion = 2} id="resuelto">
                                                      <i class="bi bi-check-square-fill two"></i>
                                                      <a href="#a" class="title-active">Resueltos</a>
                                                  </li>
                                              </ul>
                                          </div>
  
                                          <div class="buscador">
                                              <div class="buscador2">
                                                  <i class="bi bi-search"></i>
                                                  <input type="text" class="inputP three" placeholder="Buscar">
                                              </div>
                                          </div>
  
                                          <div class="abiertos {activacion === 1 ? 'active' : ''}" data-content id="open">
                                              <div class="abiertos-two">
                                                  <div class="nav-tabs">
  <!-- Mis Chats-->
                                                      <div class="nav-item" style="display: flex;" id="chats">
                                                          <a class="nav-link subtitle" on:click={()=> activaciones = 2} style="padding-right:7px;" href="#a">Mis chats </a>
                                                          <a class="nav-link dropdown-toggle subtitle2" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false"></a>
                                                          <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                                              <li><a class="dropdown-item" href="#!">Todos los chats</a></li>
                                                          </ul>
                                                      </div>
   <!-- En espera -->
                                                      <div class="nav-item" on:click={()=> activaciones = 3} id="espera">
                                                          <a class="nav-link subtitle" href="#a">En espera</a>
                                                      </div>
                                                  </div>
                                              </div>
  
                                              <ul class="line"></ul>
  
  <!-- Mis Chats-content -->
                                              <div class="multi-select {activaciones === 2 ? 'active' : ''}" data-content id="chats-content">
                                                  <div class="seccion-m">
                                                      <ul class="nav-tabs">
                                                          <span class="jss617"></span>
                                                          <div class="">
                                                              <i class=""></i>
                                                          </div>
                                                          <div class="multiline">
                                                              <span class="jss609"></span>
                                                              <span class="jss609"></span>
                                                          </div>
                                                      </ul>
                                                  </div>
                                              </div>
  <!-- Espera-content -->
                                              <div class="espera {activaciones === 3 ? 'active' : ''}" data-content id="espera-content">
                                                  <div class="jss100">
                                                      <ul class="nav-tabs">
                                                           <div class="jss105 ">
                                                              <span class="jss104">¡Nada acá!</span>
                                                              <p class="jss103" >No se encontraron chats con este término de búsqueda</p>
                                                           </div>
                                                      </ul>
                                                  </div>
                                              </div>
                                          </div>
  
  <!-- Resueltos -->
                                          <div class="resueltos {activacion === 2 ? 'active' : ''}" data-content id="resolved">
                                              <div class="jss100">
                                                  <div class="jss101">
                                                      <ul class="nav-tabs">
                                                       <div class="jss105 ">
                                                          <span class="jss104">¡Nada acá!</span>
                                                          <p class="jss103">No se encontraron chats con este término de búsqueda</p>
                                                       </div>
                                                      </ul>
                                                  </div>
                                              </div>
                                          </div>
  
                                      </div>
                              </div>
  
                              <div class="panel-2">
                                  <div class="card mb-4 container-two">
                                      <p class="jss104">Selecciona un chat para empezar a chatear</p>
                                  </div>
                              </div>
                            </div>
                          </div>
                      </main>
                  </div>
                  
  
  
  <!-- Conexiones -->
                  <div class="container-fluid px-4 {active === 1 ? 'active' : ''}"  data-content id="conexiones">
                      <div class="panel-seccion">
                          <div class="card mb-4 container-seccion">
                              <div class="jss1007">
                                  <div class="jss1008">
                                      <h2 class="text-h5">Conexiones</h2>
                                      <div class="jss1009">
                                          <button class="container-prymary">
                                              <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false">AGREGAR </a>
                                              <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                                  <li><a class="dropdown-item" href="#!"><i class="bi bi-whatsapp"></i> Whatsapp</a></li>
                                                  <!-- <li><a class="dropdown-item" href="#!"><i class="bi bi-facebook"></i> Facebook</a></li>
                                                  <li><a class="dropdown-item" href="#!"><i class="bi bi-instagram"></i> Instagram</a></li> -->
                                              </ul>
                                          </button>
                                      </div>
                                  </div>
                                  <div class="panel-2">
                                      <table class="multitablet">
                                          <thead class="title-seccion">
                                              <tr>
                                                  <th class="MuiTableCell-head">Canal</th>
                                                  <th class="MuiTableCell-head dos">Nombre</th>
                                                  <th class="MuiTableCell-head dos2">Telefono</th>
                                                  <th class="MuiTableCell-head dos3">Estado</th>
                                                  <th class="MuiTableCell-head dos4">Seccion</th>
                                                  <th class="MuiTableCell-head dos5">Ultima Actualizacón</th>
                                                  <th class="MuiTableCell-head dos6">Acciones</th>
                                              </tr>
                                          </thead>
                                          <tbody class="multitablet">
                                              <tr>
                                                  <td class="MuiTableCell-text">..</td>
                                                  <td class="MuiTableCell-text">...</td>
                                                  <td class="MuiTableCell-text">...</td>
                                                  <td class="MuiTableCell-text">...</td>
                                                  <td class="MuiTableCell-text">...</td>
                                                  <td class="MuiTableCell-text">...</td>
                                                  <td class="MuiTableCell-text">...</td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </div>
                                  <div id="qr-code">Hola</div>
                              </div>
                           </div>
                      </div>
                  </div>
  
  
   <!-- Contacto -->
          <div class="container-fluid px-4 {active === 2 ? 'active' : ''}" data-content id="contactos">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three">
                      <div class="jss1007">
                          <div class="jss1008">
                              <h2 class="text-h5 two">Contactos</h2>
                              <div class="jss1009">
                                  <div class="buscador" >
                                      <div class="buscador3" >
                                          <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false" >Etiquetas </a>
                                          <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                              <div class="buscador">
                                                  <div class="buscador-etiquetas">
                                                      <i class="bi bi-search"></i>
                                                      <input type="text" class="inputP" placeholder="Buscar">
                                                  </div>
                                                  <ol style="border-top: 2px solid rgba(0, 0, 0, 0.12);"></ol>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                              </div>
                                          </ul>
                                      </div>
                                  </div>
                                  <div class="buscador">
                                      <div class="buscador3">
                                          <i class="bi bi-search"></i>
                                          <input type="text" class="inputP" placeholder="Buscar">
                                      </div>
                                  </div>
                                  <div class="jss1009" >
                                      <button class="container-prymary button">
                                          <a class="nav-link" href="#a">AGREGAR CONTACTO</a>
                                      </button>
                                      <button class="container-prymary button2">
                                          <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false"></a>
                                          <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                              <li><a class="dropdown-item" href="#!"><i class="bi bi-arrow-bar-up"></i> Importar XLSX</a></li>
                                              <li><a class="dropdown-item" href="#!"><i class="bi bi-arrow-bar-down"></i> Exportar</a></li>
                                          </ul>
                                      </button>
                                  </div>
                              </div>
  
  
                          </div>
                          <div class="panel-2">
                              <table class="multitablet">
                                  <thead class="title-seccion">
                                      <tr>
                                          <th class="MuiTableCell-head">Nombre</th>
                                          <th class="MuiTableCell-head">Whatsapp</th>
                                          <th class="MuiTableCell-head">Correo Electronico</th>
                                          <th class="MuiTableCell-head">Etiquetas</th>
                                          <th class="MuiTableCell-head">Acciones</th>
                                      </tr>
                                  </thead>
                                  <tbody class="multitablet">
                                      <tr>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                      </tr>
                                  </tbody>
                              </table>
                          </div>
                      </div>
                    </div>
                  </div>
              </div>
   <!-- Respuestas... -->
          <div class="container-fluid px-4 {active === 4 ? 'active' : ''}" data-content id="respuesta">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three2">
                      <div class="jss1007">
                          <div class="jss1008">
                              <h2 class="text-h5 two2">Respuestas rápidas</h2>
                              <div class="jss1009">
                                  <div class="buscador">
                                      <div class="buscador3">
                                          <i class="bi bi-search"></i>
                                          <input type="text" class="inputP" placeholder="Buscar">
                                      </div>
                                  </div>
                                  <div class="buscador etiquetas" >
                                      <div class="buscador2" >
                                          <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false" >Etiquetas </a>
                                          <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                              <div class="buscador">
                                                  <div class="buscador-etiquetas">
                                                      <i class="bi bi-search"></i>
                                                      <input type="text" class="inputP" placeholder="Buscar">
                                                  </div>
                                                  <ol style="border-top: 2px solid rgba(0, 0, 0, 0.12);"></ol>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                    <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                              </div>
                                          </ul>
                                      </div>
                                  </div>
                                  <div class="jss1009" >
                                       <button class="container-prymary">
                                      <a class="nav-link" id="navbarDropdown" href="#a" >AÑADIR RESPUESTA RÁPIDA </a>
                                  </button>
                                  </div>
                              </div>
  
  
                          </div>
                          <div class="panel-2">
                              <table class="multitablet">
                                  <thead class="title-seccion">
                                      <tr>
                                          <th class="MuiTableCell-head">Atajo</th>
                                          <th class="MuiTableCell-head">Mensaje</th>
                                          <th class="MuiTableCell-head">Comparte</th>
                                      </tr>
                                  </thead>
                                  <tbody class="multitablet">
                                      <tr>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                      </tr>
                                  </tbody>
                              </table>
                          </div>
                      </div>
                   </div>
              </div>
          </div>
  
  <!-- Documento -->
           <div class="container-fluid px-4 {active === 5 ? 'active' : ''}" data-content id="documentos">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three2">
                      <div class="jss1007">
                          <div class="jss1008">
                              <h2 class="text-h5 two2">Documentos</h2>
                              <!-- <div class="jss1009">
                                  <div class="buscador">
                                      <div class="buscador3">
                                          <i class="bi bi-search"></i>
                                          <input type="text" class="inputP" placeholder="Buscar">
                                      </div>
                                  </div>
                                  <div class="buscador etiquetas" >
                                      <div class="buscador2" >
                                          <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false" >Etiquetas </a>
                                          <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                              <div class="buscador">
                                                  <div class="buscador-etiquetas">
                                                      <i class="bi bi-search"></i>
                                                      <input type="text" class="inputP" placeholder="Buscar">
                                                  </div>
                                                  <ol style="border-top: 2px solid rgba(0, 0, 0, 0.12);"></ol>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                    <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                              </div>
                                          </ul>
                                      </div>
                                  </div>
                                  <div class="jss1009" >
                                       <button class="container-prymary">
                                      <a class="nav-link" id="navbarDropdown" href="#" >AÑADIR RESPUESTA RÁPIDA </a>
                                  </button>
                                  </div>
                              </div> -->
  
  
                          </div>
                          <!-- <div class="panel-2">
                              <table class="multitablet">
                                  <thead class="title-seccion">
                                      <tr>
                                          <th class="MuiTableCell-head">Atajo</th>
                                          <th class="MuiTableCell-head">Mensaje</th>
                                          <th class="MuiTableCell-head">Comparte</th>
                                      </tr>
                                  </thead>
                                  <tbody class="multitablet">
                                      <tr>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                      </tr>
                                  </tbody>
                              </table>
                          </div> -->
                      </div>
                   </div>
              </div>
          </div>
  
  
   <!-- Equipo -->
          <div class="container-fluid px-4 {active === 6 ? 'active' : ''}" data-content id="equipo">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three3">
                      <div class="jss1007">
                          <div class="jss1008">
                              <h2 class="text-h5 two3">Equipo de Trabajo</h2>
                              <div class="jss1009">
                                  <div class="buscador">
                                      <div class="buscador3">
                                          <i class="bi bi-search"></i>
                                          <input type="text" class="inputP" placeholder="Buscar">
                                      </div>
                                  </div>
                                  <div class="jss1009"  style="padding-left: 10px ;">
                                       <button class="container-prymary">
                                      <a class="nav-link" id="navbarDropdown" href="#a" >AGREGAR USUARIO </a>
                                  </button>
                                      <form action="">
  
                                      </form>
                                  </div>
                              </div>
  
  
                          </div>
                          <div class="panel-2">
                              <table class="multitablet">
                                  <thead class="title-seccion">
                                      <tr>
                                          <th class="MuiTableCell-head">Nombre</th>
                                          <th class="MuiTableCell-head">Correo Electronico</th>
                                          <th class="MuiTableCell-head">Ultima Sección</th>
                                          <th class="MuiTableCell-head">Acciónes</th>
                                      </tr>
                                  </thead>
                                  <tbody class="multitablet">
                                      <tr>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                      </tr>
                                  </tbody>
                              </table>
                          </div>
                      </div>
                   </div>
              </div>
          </div>
  
   <!-- Chatbots -->
          <div class="container-fluid px-4 {active === 7 ? 'active' : ''}" data-content id="chatbots">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three4">
                      <div class="jss1007">
                          <div class="jss1008">
                              <h2 class="text-h5 two4">Chatbots</h2>
                              <div class="jss1009">
                                  <div class="jss1009"  style="padding-left: 10px ;">
                                          <button class="container-prymary">
                                      <a class="nav-link" id="navbarDropdown" href="#a" >AGREGAR DEPARTAMENTO </a>
                                  </button>
                                      <form action="">
  
                                      </form>
                                  </div>
                              </div>
  
  
                          </div>
                          <div class="panel-2">
                              <table class="multitablet">
                                  <thead class="title-seccion">
                                      <tr>
                                          <th class="MuiTableCell-head">Nombre</th>
                                          <th class="MuiTableCell-head">Color</th>
                                          <th class="MuiTableCell-head">Mensaje de saludo</th>
                                          <th class="MuiTableCell-head">Comportamiento</th>
                                      </tr>
                                  </thead>
                                  <tbody class="multitablet">
                                      <tr>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                      </tr>
                                  </tbody>
                              </table>
                          </div>
                      </div>
                   </div>
               </div>
          </div>
  
   <!-- Campaña -->
          <div class="container-fluid px-4 {active === 8 ? 'active' : ''}" data-content id="campaña">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three5">
                      <div class="jss1007">
                          <div class="jss1008">
                              <h2 class="text-h5 two5">Campaña</h2>
                              <div class="jss1009">
                                  <div class="buscador">
                                      <p class="parrafo">Mensajes restantes: X</p>
                                  </div>
                                  <div class="buscador etiquetas" >
                                      <div class="buscador2" >
                                          <a class="nav-link dropdown-toggle" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false" >Etiquetas </a>
                                          <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                              <div class="buscador">
                                                  <div class="buscador-etiquetas">
                                                      <i class="bi bi-search"></i>
                                                      <input type="text" class="inputP" placeholder="Buscar">
                                                  </div>
                                                  <ol style="border-top: 2px solid rgba(0, 0, 0, 0.12);"></ol>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                  <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                                    <div class="buscador-etiquetas">
                                                      <input type="checkbox" class="inputP" placeholder="Buscar">
                                                      <input type="text">
                                                  </div>
                                              </div>
                                          </ul>
                                      </div>
                                  </div>
                                  <div class="jss1009" >
                                       <button class="container-prymary">
                                      <a class="nav-link" id="navbarDropdown" href="#a" >AÑADIR RESPUESTA RÁPIDA </a>
                                  </button>
                                  </div>
                              </div>
                          </div>
  
                          <div class="panel-2">
                              <table class="multitablet">
                                  <thead class="title-seccion">
                                      <tr>
                                          <th class="MuiTableCell-head">Atajo</th>
                                          <th class="MuiTableCell-head">Mensaje</th>
                                          <th class="MuiTableCell-head">Comparte</th>
                                      </tr>
                                  </thead>
                                  <tbody class="multitablet">
                                      <tr>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                          <td class="MuiTableCell-text">...</td>
                                      </tr>
                                  </tbody>
                              </table>
                          </div>
                      </div>
                   </div>
              </div>
          </div>
   <!-- Suscripcion -->
                   <!-- <div class="container-fluid px-4" data-content id="suscripcion">
                      <h1 class="mt-4">Suscripción</h1>
                      <ol class="breadcrumb mb-4"></ol>
                   </div> -->
  
   <!-- Informes -->
          <div class="container-fluid px-4 {active === 9 ? 'active' : ''}" data-content id="informes">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion two6">
                      <div class="contenedorP">
                          <div class="contenedorP-container">
  
                          <div class="panel-2 informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel-2 informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel-2 informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel-2 informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
  
                      </div>
  
                          <div class="panel informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
                          <div class="panel informe">
                              <div class="card mb-4 container-three">
                                  Selecciona un chat para empezar a chatear.
                              </div>
                          </div>
  
                      </div>
                    </div>
              </div>
          </div>
  
   <!-- Configuracion -->
           <div class="container-fluid px-4 {active === 10 ? 'active' : ''}" data-content id="configuracion">
              <div class="panel-seccion">
                  <div class="card mb-4 container-seccion three6">
                      <h1 class="text-h5 configuration">Configuración</h1>
                      <ol class="breadcrumb mb-4"></ol>
                      <div class="contenedorP">
                          <div class="contenedorP-container" style="width: 55%;">
                              <div class="panel-2 informe">
                                  <div class="card mb-4 container">
                                      <div class="">
                                          <div class="jss1010">
                                              <div class="buscador" >
                                                  <p class="parrafo2">Idioma de los mensajes generados automáticamente.</p>
                                              </div>
                                              <div class="buscador etiquetas" >
                                                  <div class="buscador2 input-button2" >
                                                      <a class="nav-link dropdown-toggle input-a" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                                          <input type="button" class="input-button" name="" id="">
                                                      </a>
                                                      <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                                          <li><a class="dropdown-item" href="#!"> Portugués</a></li>
                                                          <li><a class="dropdown-item" href="#!"> Español</a></li>
                                                          <li><a class="dropdown-item" href="#!"> Inglés</a></li>
                                                      </ul>
                                                  </div>
                                              </div>
                                          </div>
                                      </div>
                                      <hr class="MuiDivider-root ">
                                      <div class="">
                                          <div class="jss1010">
                                              <div class="buscador">
                                                  <p class="parrafo2">Uso horario.</p>
                                              </div>
                                              <div class="buscador etiquetas" >
                                                  <div class="buscador2 input-button2" >
                                                      <a class="nav-link dropdown-toggle input-a" id="navbarDropdown" href="#a" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                                          <input type="button" class="input-button" name="" id="">
                                                      </a>
                                                      <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                                                          <li><a class="dropdown-item" href="#!"> Portugués</a></li>
                                                          <li><a class="dropdown-item" href="#!"> Español</a></li>
                                                          <li><a class="dropdown-item" href="#!"> Inglés</a></li>
                                                      </ul>
                                                  </div>
                                              </div>
                                          </div>
                                      </div>
                                      <hr class="MuiDivider-root ">
                                      <div class="">
                                          <div class="jss1010">
                                              <div class="buscador">
                                                  <a href="#a" style="text-decoration: none; color: black;" >
                                                      <p class="parrafo2">Borrar datos de la cuenta.</p>
                                                  </a>
                                              </div>
                                          </div>
                                      </div>
                                  </div>
                              </div>
                          </div>
                      </div>
                   </div>
              </div>
           </div>
  
          <footer class=" bg-light mt-auto">
          <div class="container-footer px-4 three7">
              <div class="d-flex align-items-center justify-content-between small">
                  <div class="text-muted">Copyright &copy; Whatsapp/Technojet 2023</div>
                  <div>
                      <a href="#a">Privacy Policy</a>
                      &middot;
                      <a href="#a">Terms &amp; Conditions</a>
                  </div>
              </div>
          </div>
          </footer>
      </div>
  </div>
</div>

