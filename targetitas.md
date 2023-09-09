---
layout: default
title: Targetitas
permalink: /testtargetitas/
---

<div class="no-pad-top" id="index-page">
  <div class="container">
    <div class="section">
      


    <!-- PONENTES -->

    <div class="section">
      <h3 id="Ponentes">Ponentes</h3>
      <h2>Elegimos que nos enseñen los mejores</h2>
        <p style="text-align: justify;">
          Algun@s ponentes que ya nos han confirmado:
        </p>
     </div>

     <div class="section">
       <div class="col s12 m6">
         <div class="row center">
         {% for person in site.persons %}
         {% if person.evento contains "JornadasVerano2021" %}
         {% if person.destacado contains "YES" %}
           <ul class="collection waves-effect waves-light" style="width: 33%">
             <a href="#{{ person.id | remove: "/" }}-modal" class="collection-item modal-trigger waves-effect waves-light" style="color: rgba(0, 0, 0, 0.87); padding: 2px">
               <li class="collection-item avatar2">
                 <img src="{{ person.img }}" alt="" class="circle">
                 {% if person.nombredes %}
                 <span class="title" style="padding-left: 10px">{{ person.nombredes }}</span>
                 {% else %}
                 <span class="title" style="padding-left: 10px">{{ person.nombre }}</span>
                 {% endif %}
                 {% if person.roldes %}
                 <p style="padding-top: 10px">
                   {{ person.roldes }}
                 </p>
                 {% else %}
                 <p style="padding-top: 10px">
                   {{ person.rol }}
                 </p>
                 {% endif %}
               </li>
             </a>
           </ul>
         {% endif %}
         {% endif %}
         {% endfor %}    
         </div>
       </div>
     </div>


     <!-- Modal PONENTES -->

     {% for person in site.persons %}
     {% if person.evento contains "JornadasVerano2021" %}

     <div id="{{ person.id | remove: "/" }}-modal" class="modal">
       <div class="modal-content">
         <div class="section" style="padding-left: 30px; padding-right: 30px;">

           <div class="row">
             <div class="col s12 m6 l6">
               <div class="row center">
               <img src="{{ person.img }}" alt="" class="circle" width="70%">
               </div>
             </div>
             <div class="col s12 m6 l6">        
               <div class="row center" style="padding-left: 30px; padding-top: 70px;">
                 <h3 class="justify">{{ person.nombre }}</h3>
                 <h5 class="justify">Biografía y Contenido Recomendado</h5>
               </div>
             </div>
           </div>

           <!-- Biografía -->

           <div class="row">
             <h2 class="justify">Biografía</h2>
             {% if person.bio1 %}
             <p style="text-align: justify;">
             {{ person.bio1 }}
             </p>
             {% endif %}
             {%- if person.bio2 -%}<p style="text-align: justify;">
             {{ person.bio2 }}
             </p>{%- endif -%}
             {%- if person.bio3 -%}<p style="text-align: justify;">
             {{ person.bio3 }}
             </p>{%- endif -%}
             {%- if person.bio4 -%}<p style="text-align: justify;">
             {{ person.bio4 }}
             </p>{%- endif -%}
           </div>

           <!-- Recomendaciones -->

             <div class="row">
               <h2 class="justify" style="padding-bottom: 12px;">Contenido Recomendado</h2>
               {%- if person.book1title -%}
                {%- if person.book2title -%}<div class="col s12 m6 l6">{%- endif -%}     
                  <div class="row center">
         		        <a href="{{ person.book1link }}" target="_blank"><img class="responsive-img" style="width:50%; align: center;" src="{{ person.book1img }}"></a>
                     <p style="text-align: center; padding-right: 2px; padding-left: 2px;">
                       <a href="{{ person.book1link }}" target="_blank">{{ person.book1title }}</a>
                     </p>
                  </div>
                {%- if person.book2title -%}</div>{%- endif -%}      
               {%- endif -%}
               {%- if person.book2title -%}
               <div class="col s12 m6 l6">
                 <div class="row center">
                   <a href="{{ person.book2link }}" target="_blank"><img class="responsive-img" style="width:50%" src="{{ person.book2img }}"></a>
                   <p style="text-align: center; padding-right: 2px; padding-left: 2px;">
                     <a href="{{ person.book2link }}" target="_blank">{{ person.book2title }}</a>
                   </p>
                 </div>
               </div>
               {%- endif -%}
             </div>

             {%- if person.videotitle -%}
             <div class="row">
               <center><iframe width="642" height="361" src="{{- person.videolink -}}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>
             </div>
             {%- endif -%}

             {%- if person.otherinfo1link -%}
             <div class="row">
               <div class="col s12 m6 l6">
                 <div class="row center">
                  <a href="{{ person.otherinfo1link }}" target="_blank">{{ person.otherinfo1text }}</a>
                </div>
              </div>
              {%- if person.otherinfo2link -%}
              <div class="col s12 m6 l6">
                <div class="row center">
                    <a href="{{ person.otherinfo2link }}" target="_blank">{{ person.otherinfo2text }}</a>
                </div>
              </div>
              {%- endif -%}
             </div>
            {%- endif -%}

             {%- if person.otherinfo3link -%}
             <div class="row">
               <div class="col s12 m6 l6">
                 <div class="row center">
                  <a href="{{ person.otherinfo3link }}" target="_blank">{{ person.otherinfo3text }}</a>
                </div>
              </div>
              {%- if person.otherinfo4link -%}
              <div class="col s12 m6 l6">
                <div class="row center">
                    <a href="{{ person.otherinfo4link }}" target="_blank">{{ person.otherinfo4text }}</a>
                </div>
              </div>
              {%- endif -%}
             </div>
             {%- endif -%}

         </div>
       </div>
       <div class="modal-footer">
         <a href="#!" class="modal-close waves-effect waves-green btn-flat">CERRAR</a>
       </div>
     </div>

     {% endif %}
     {% endfor %}


    </div>
  </div>
</div>
