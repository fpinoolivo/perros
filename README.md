<! doctype html >
< html  lang = " es " >
< cabeza >
  < meta  charset = " UTF-8 " >
  < meta  name = " viewport " content = " ancho = ancho del dispositivo, escala inicial = 1 " >

  < título > Katana Lite - Sistema de Tienda en Línea </ título >

  < link  rel = " stylesheet " type = " text / css " href = " res / lib / bootstrap / css / bootstrap.min.css " >
  < link  rel = " stylesheet " type = " text / css " href = " res / lib / fontawesome / css / fontawesome.min.css " >
  < link  rel = " stylesheet " type = " text / css " href = " res / lib / fontawesome / css / all.min.css " >
  < script  src = " res / lib / jquery / jquery.min.js " > </ script >

</ cabeza >
< cuerpo  >
< sección >
  < div  class = " container " >
    < div  class = " row " >
      < div  class = " col-md-3 col-xs-5 " >
      < Br > < h1 > KATANA LITE </ h1 >
      </ div >
      < div  class = " col-md-7 col-xs-5 " >
< Br > < br >
<! ---
<form class = "form-horizontal" role = "form">
<div class = "input-group">
<input type = "hidden" name = "view" value = "productos">
<input type = "hidden" name = "act" value = "search">
      <input type = "text" name = "q" placeholder = "Buscar productos ..." class = "form-control">
      <abarcan clase = "input-group-btn">
        <button class = "btn btn-primary" type = "button"> & nbsp; <i class = "fa fa-search"> </i> & nbsp; </button>
      </span>
    </div>
</form>
->
< Br > < br >
      </ div >
      < div  class = " col-md-2 col-xs-2 " >
        <! - botón de carrito ->
< Br > < br >

      </ div >

    </ div >
  </ div >
</ sección >





< nav  class = " navbar navbar-expand-lg navbar-light bg-light " >
  < div  class = " container " >
<! - <a class = "navbar-brand" href = "./"> Navbar </a> ->
  < button  class = " navbar-toggler " type = " button " data-toggle = " collapse " data-target = " #navbarSupportedContent " aria-controls = " navbarSupportedContent " aria- extended = " false " aria-label = " Alternar navegación " >
    < span  class = " navbar-toggler-icon " > </ span >
  </ button >

  < div  class = " collapse navbar-collapse " id = " navbarSupportedContent " >
    < ul  class = " navbar-nav mr-auto " >
      < li  class = " elemento de navegación activo " >
        < Una  clase = " nav-link " href =" ./ " > < i  clase =" fa fa-casa " > </ i > Inicio </ a >
      </ li >
<? php
$ gatos = CategoryData :: getPublics ();
?>
<? php  if ( cuenta ( $ gatos )> 0 ): ?>
      < li  class = " menú desplegable de elemento de navegación activo " >
        < Una  clase = " nav-enlace-desplegable de palanca " href =" # " ID =" navbarDropdown " roles =" botón " de datos de palanca =" desplegable " aria-haspopup =" verdad " aria-expandida =" false " >
          < i  class = " fa fa-th-list " > </ i > Categorías
        </ a >

        < div  class = " menú desplegable " aria-labelledby = " navbarDropdown " >
<? php  foreach ( $ gatos  como  $ gato ): ?>
          < Una  clase = " -elemento desplegable " href =" index.php? View = Productos & cat = <? Php  echo  $ cat -> nombre_corto ; ?> " > <? Php?  Echo  $ cat -> nombre ; ?> </ a >
<? php  endforeach ; ?>
        </ div >
      </ li >
    <? php  endif ; ?>



      < li  class = " menú desplegable de elemento de navegación activo " >
        < Una  clase = " nav-enlace-desplegable de palanca " href =" # " ID =" navbarDropdown " roles =" botón " de datos de palanca =" desplegable " aria-haspopup =" verdad " aria-expandida =" false " >
          < i  class = " fa fa-user " > </ i > Mi cuenta
        </ a >

        < div  class = " menú desplegable " aria-labelledby = " navbarDropdown " >
          <? php  if ( isset ( $ _SESSION [ "client_id" ])): ?>
          < Una  clase = " -elemento desplegable " href =" index.php? View = cliente " > Mi Cuenta </ a >
          < Una  clase = " desplegable ítems " href =" logout.php " > Salir </ a >
            <? php  else : ?>
          < Una  clase = " desplegable ítems " href =" index.php? View = ClientAccess " > Iniciar Sesión </ a >
          < Una  clase = " -elemento desplegable " href =" index.php? View = registro " > Registro </ a >
        <? php  endif ; ?>
        </ div >
      </ li >

    </ ul >
    < form  class = " form-inline my-2 my-lg-0 " >
< input  type = " hidden " name = " view " value = " productos " >
< input  type = " hidden " name = " act " value = " search " >

      < input  class = " form-control mr-sm-2 " name = " q " type = " search " placeholder = " Buscar ... " aria-label = " Buscar ... " >
      < button  class = " btn btn-outline-primary my-2 my-sm-0 " type = " submit " > Buscar </ button >
& nbsp;
< Un  href = " index.php? View = mycart " clase =" btn btn-secundaria mi-mi-2 SM-0 " > < i  clase =" fa fa-shopping-cart " > </ i > 
<? php  if ( isset ( $ _SESSION [ "cart" ])): ?>
< span  class = " badge " > <? php  echo  count ( $ _SESSION [ "cart" ]); ?> </ span >
<? php  endif ; ?>
      </ a >


    </ form >
  </ div >
</ div >
</ nav >



< Br >
<? php  View :: load ( "index" ); ?>
< Br > < br > < br >
< sección >
< div  class = " container " >

<! - - - - ->
< div  class = " row " >
< div  class = " col-md-12 " >
< hr >
< p > < b > Katana Lite </ b > y copia; 2019 </ p >
< ul  class = " list-inline " >
< Li  clase = " lista-inline-elemento " > < p  clase =" text-silenciado " >  < un  href =" http://evilnapsis.com/ " > Evilnapsis </ a > </ p > </ li >
< Li  clase = " lista-inline-elemento " > < p  clase =" text-silenciado " >  < un  href =" http://evilnapsis.com/support/katana-documentation/ " > Documentacion </ a > </ p > </ li >
</ ul >
</ div >
</ div >
</ div >
</ sección >
< Br >
  < script  src = " res / lib / bootstrap / js / bootstrap.min.js " > </ script >
  < guión >
  $ ( ".tip" ) . información sobre herramientas ( ) ;
  </ script >
</ cuerpo >
</ html >
