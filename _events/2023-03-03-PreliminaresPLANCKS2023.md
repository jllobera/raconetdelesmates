---
layout: event
categories: eventos-internacionales
title:  "Preliminares de PLANCKS 2023"
startingdate: 2023-03-03
endingdate:
place: Toda España
locandina: /img/eventos/2023-PLANCKS/logo.png
cover: /img/eventos/2023-PLANCKS/fondo_web.png
gallery:
site: /PreliminaresPLANCKS2023/
ranking:
exam:
comm:
---

<div class="container">
  <div class="section">

<!-- HEADER -->
    <img class="materialboxed" width="100%" src="/img/eventos/2023-PLANCKS/BANNER.png">
    
<!-- COUNTDOWN -->
    <div class="row">  
      <p style="text-align: justify;">Las inscripciones para las Preliminares de PLANCKS 2023 se abrirán en...</p>
      <h4 style="text-align: center;"><p id="countdown" style="text-align:center"></p></h4>
      
<!-- INTRO -->
      <p style="text-align: justify;">¿Tienes ganas de pasar un rato divertido resolviendo problemas de física? ¡Ya tenemos aquí la sexta edición de las <strong>Preliminares de PLANCKS</strong>! Y este año... como novedad, con <strong>1000€ en PREMIOS</strong> gracias al apoyo de la Fundación Ramón Areces. Así que reúne a un grupo de motivados como tú y sigue explorando la web para saber más. ¡Bienvenid@!</p>
    </div>
      
<!-- BUTTONS -->
    <div class="row center">
      <a href="{{ site.url }}/PreliminaresPLANCKS2023/" id="prelis-button" class="btn-large waves-effect waves-light" style="background-color: #018c45;">Ir a la página de PLANCKS</a>
    </div>
  </div>
</div>      


<!-- TIMER SCRIPT -->
<script>
  // Set the date we're counting down to
  var countDownDate = new Date("Feb 27, 2023 12:30:00").getTime();

  // Update the count down every 1 second
  var x = setInterval(function() {

    // Get today's date and time
    var now = new Date().getTime();

    // Find the distance between now and the count down date
    var distance = countDownDate - now;

    // Time calculations for days, hours, minutes and seconds
    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((distance % (1000 * 60)) / 1000);

    // Output the result in an element with id="countdown"
    document.getElementById("countdown").innerHTML = days + "d " + hours + "h "
    + minutes + "m " + seconds + "s ";

    // If the count down is over, write some text
    if (distance < 0) {
      clearInterval(x);
      document.getElementById("countdown").innerHTML = "INSCRIPCIONES CERRADAS";
    }
  }, 1000);
</script>
