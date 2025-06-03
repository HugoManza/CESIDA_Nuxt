<template>
  <section :id="section.id" class="section" :class="{
    'active': isActive,
    'exit-left': exitDirection === 'left' && !isActive,
    'exit-right': exitDirection === 'right' && !isActive
  }">
    <!-- Tipografías -->
    <div v-if="section.id === 'Tipografía'">
      <h2 class="font-heading">Tipogra<span class="script">f</span>ía</h2>
      <p>La tipografía principal es Transforma Sans_Trial, pero algunos caracteres se puede variar con la
        Transforma Script. Esta tipografía se define por formas curvas, que hacen alusión a un lazo, un
        símbolo identificativo del VIH (lazo rojo).
        La combinación de ambas tipos genera un contraste entre una geométrica y una más caligráfica. <br><br>
        Para evitar un uso inadecuado de la tipografía se establecieron unas pautas: La mayoría de
        caracteres deben ser pertenecientes a la tipografía Transforma Sans_Trial, solo puede usarse la
        Transforma Script cada tres caracteres como mínimo y solo se debe usar en una única letra, jamás
        debe aparecer la Transforma Script en dos caracteres seguidos.
        También se establecieron las diferentes letras que pueden variar de tipografía.</p>

      <h3>Fuente Principal: Transforma Mix</h3>
      <div class="font-example">
        <div class="font-heading">Transf<span class="script">or</span>ma Mix</div>
        <div class="font-subheading firstFont">Ti<span class="script">tu</span>lo Pri<span class="script">nc</span>ipal
        </div>
        <div class="font-body">Semibold - 48pt </div>
      </div>

      <h3>Fuente Secundaria: Lexend Deca</h3>
      <div class="font-example secondary-font">
        <div class="font-heading"> Lexend Deca</div>
        <div class="font-subheading secondFont">Subtitulo de Explicación</div>
        <div class="font-body">Light - AllCaps - 20pt</div>
        <div class="font-subheading thirdFont">Sección</div>
        <div class="font-body">Semibold - AllCaps - 20pt</div>
        <div class="font-body"> <span class="textCorr">Texto Corrido</span> <br><br>Cesida es la Coordinadora estatal de
          VIH y sida. Somos la entidad más representativa del
          movimiento ciudadano de VIH y sida del Estado español, con presencia en 17 Comunidades Autónomas. Nos fundamos
          en el año 2002 y en la actualidad somos la organización referente para abordar la realidad del VIH y sida en
          España. <br><br>
          Normal - 10pt

        </div>
      </div>

      <h3>Usos Correctos</h3>
      <ul>
        <li>La tipografía Transforma Mix solo debe ser usada para titulos principales a gran tamaño para mantener su
          legibilidad.</li>
        <li>Mantener una jerarquía correcta y usar las tipografías en el orden establecido.</li>
        <li>En medios digitales, es importante mantener el cuerpo de texto de al menos 14pt.</li>
        <li>Mantener un interlineado de 1.5pt para facilitar la legibilidad.</li>
      </ul>
    </div>

    <!-- Colores -->
    <div v-if="section.id === 'colors'">
      <h2>Colo<span class="script">r</span>es</h2>
      <p>Con inspiración de los antiguos colores, esta nueva paleta mantiene las ideas planteadas por CESIDA dandoles un
        nuevo toque de frescura y aportando valores especificos a nuestros colors. Tambien redujimos minimamente la
        paleta para hacerla mas
        coherente.</p>

      <h3>Colores Principales</h3>
      <div class="color-palette">
        <div class="color-swatch">
          <div class="color-display cesida-blue">
            <h4>Compasión</h4>
            <h4>Estabilidad</h4>
            <h4>Honestidad</h4>
          </div>
          <div class="color-info">
            <div class="color-name">CESIDA Azul</div>
            <div class="color-hex">#54C1DC</div>
            <div class="color-rgb">RGB: 84, 193, 220</div>
          </div>
        </div>

        <div class="color-swatch">
          <div class="color-display cesida-red">
            <h4>Pasión</h4>
            <h4>Fuerza</h4>
            <h4>Dedicación</h4>
          </div>
          <div class="color-info">
            <div class="color-name">CESIDA Rojo</div>
            <div class="color-hex">#E94F1E</div>
            <div class="color-rgb">RGB: 233, 79, 30</div>
          </div>
        </div>

        <div class="color-swatch">
          <div class="color-display cesida-yellow">
            <h4>Energía</h4>
            <h4>Optimismo</h4>
            <h4>Ilusión</h4>
          </div>
          <div class="color-info">
            <div class="color-name">CESIDA Amarillo</div>
            <div class="color-hex">#FDC609</div>
            <div class="color-rgb">RGB: 523, 198, 9</div>
          </div>
        </div>
        <div class="color-swatch">
          <div class="color-display cesida-green">
            <h4>Progreso</h4>
            <h4>Renovación</h4>
            <h4>Esperanza</h4>
          </div>
          <div class="color-info">
            <div class="color-name">CESIDA Verde</div>
            <div class="color-hex">#2EAA53</div>
            <div class="color-rgb">RGB: 46, 170, 83</div>
          </div>
        </div>
        <div class="color-swatch">
          <div class="color-display cesida-pink">
            <h4>Curiosidad</h4>
            <h4>Amabilidad</h4>
            <h4>Cuidado</h4>
          </div>
          <div class="color-info">
            <div class="color-name">CESIDA Rosa</div>
            <div class="color-hex">#F087B5</div>
            <div class="color-rgb">RGB: 240, 135, 181</div>
          </div>
        </div>
      </div>
      <h3>Colores Secundarios</h3>
      <div class="color-palette">
        <div class="color-swatch">
          <div class="color-display cesida-black"></div>
          <div class="color-info">
            <div class="color-name">Negro</div>
            <div class="color-hex">#001100</div>
            <div class="color-rgb">RGB: 0, 17, 0</div>
          </div>
        </div>

        <div class="color-swatch">
          <div class="color-display cesida-dark-gray"></div>
          <div class="color-info">
            <div class="color-name">Gris Oscuro</div>
            <div class="color-hex">#595F59</div>
            <div class="color-rgb">RGB: 89, 95, 89</div>
          </div>
        </div>

        <div class="color-swatch">
          <div class="color-display cesida-light-gray"></div>
          <div class="color-info">
            <div class="color-name">Gris Claro</div>
            <div class="color-hex">#DFE2DF</div>
            <div class="color-rgb">RGB: 223, 226, 223</div>
          </div>
        </div>

        <div class="color-swatch">
          <div class="color-display cesida-white"></div>
          <div class="color-info">
            <div class="color-name">Blanco</div>
            <div class="color-hex">#ffffff</div>
            <div class="color-rgb">RGB: 255, 255, 255</div>
          </div>
        </div>
      </div>

      <h3>Usos de los Colores</h3>
      <ul>
        <li>No tiene por que haber un color predominante en la marca, si no que este se debería seleccionar bsandose en
          los valores del mismo dependiedo del objetivo del diseño.</li>
        <li>Se permite bajar el valor de los colores en margenes de 15 para aclarar los mismos si fueran a ser usados en
          fondos, nunca para iconos o elementos principales.</li>
        <li>Los colores secundarios deberían servir para amplificar los principales, no sustituirlos.</li>
        <li>Mantener suficiente contrase entre los colores (Reglas WCAG)</li>
      </ul>
    </div>

    <!-- Iconos -->
    <div v-if="section.id === 'icons'">
      <h2>Ico<span class="script">n</span>os</h2>
      <p>Los nuevos iconos funcionan como una especie de elementos decorativos que encajan perfectamente con los valores
        de la marca. La idea es tener una gran variedad de elementos geometricos y abstractos para representar una gran
        variedad de ideas.</p>

      <h3>Estilo de Iconos</h3>
      <p>Nuestros iconos utilizan un estilo redondeado y amable, con todas sus esquinas exteriores redondeadas. Ademas,
        aunque aqui se presentnen en negro, deben utilizarse con cualquiera de los colores corporativos disponibles.</p>

      <h3>Librería de Iconos</h3>
      <div class="icon-grid">
        <div class="icon-item">
          <img class="icon" src="../assets/img/icons/BlackIcons/BlackIcons (1).svg"></img>
        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (2).svg" class="icon"></img>
        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (3).svg" class="icon"></img>
        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (4).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (5).svg" class="icon"></img>
        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (6).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (7).svg" class="icon"></img>
        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (8).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (9).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (10).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (11).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (12).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (13).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (14).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (15).svg" class="icon"></img>

        </div>
        <div class="icon-item">
          <img src="../assets/img/icons/BlackIcons/BlackIcons (16).svg" class="icon"></img>

        </div>

      </div>

      <h3>Cuadricula de Creación</h3>
      <div class="create-icon">
        <img src="../assets/img/icons/RetSimb.svg" alt="">
      </div>

      <h3>Uso correcto de los Iconos</h3>
      <ul>
        <li>Los iconos pueden ir acompañando texto o como elementos independientes.</li>
        <li>Una vez se coloque un icono, debe mantenerse ese tamaño constante al añadirse más.</li>
        <li>Cualquier icono nuevo debe estar formado a parrir de la reticula, manteniendo el respeyto por el tamaño de
          el resto.</li>
        <li>Los iconos, al ser de colores deben ser siempre de uno de los colores corporativos.</li>
        <li>Se puede usar la forma de los diferentes iconos para generar mascaras de recorte y usar fotografías como
          relleno.</li>
      </ul>
    </div>

    <!-- Logos  -->
    <div v-if="section.id === 'logos'">
      <h2>Ima<span class="script">g</span>otip<span class="script">os</span></h2>
      <p>Con un Isologo variable, CESIDA busca expandirse y mantener la coerencia de lo que significa ser el cordinador
        estatal. <br><br> Debe recordar que se trata de una marca variable a traves del uso de los iconos realizados
        para
        la misma, de forma que los ejemplos a continuación solo muestran un segmento de las posibilidades y
        combinaciones.</p>

      <h3>Principales</h3>
      <h4>Negros</h4>
      <div class="logo-mains">
        <div class="logo-variants">
          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosMain/LogosMain (3).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosMain/LogosMain (1).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosMain/LogosMain (2).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosMain/LogosMain (4).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosMain/LogosMain (5).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosMain/LogosMain (6).svg" alt=""></div>
          </div>
        </div>
        <h4>Blancos</h4>
        <div class="logo-variants backDark">
          <div class="logo-variant ">
            <div class="logo-img"><img src="../assets/img/logos/logosWhite/LogosWhite (1).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosWhite/LogosWhite (2).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosWhite/LogosWhite (3).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosWhite/LogosWhite (4).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosWhite/LogosWhite (5).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosWhite/LogosWhite (6).svg" alt=""></div>
          </div>
        </div>
        <h4>Positivos</h4>
        <div class="logo-variants">
          <div class="logo-variant ">
            <div class="logo-img"><img src="../assets/img/logos/logosPos/LogoPos (1).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosPos/LogoPos (2).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosPos/LogoPos (3).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosPos/LogoPos (4).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosPos/LogoPos (5).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosPos/LogoPos (6).svg" alt=""></div>
          </div>
        </div>
        <h4>Negativos</h4>
        <div class="logo-variants backDark">
          <div class="logo-variant ">
            <div class="logo-img"><img src="../assets/img/logos/logosNeg/LogoNeg (1).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img "><img src="../assets/img/logos/logosNeg/LogoNeg (2).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosNeg/LogoNeg (3).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosNeg/LogoNeg (4).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosNeg/LogoNeg (5).svg" alt=""></div>
          </div>

          <div class="logo-variant">
            <div class="logo-img"><img src="../assets/img/logos/logosNeg/LogoNeg (6).svg" alt=""></div>
          </div>
        </div>
      </div>
      <h3>Secciones</h3>
      <div class="logo-plus">
        <div class="logo-extras">
          <div class="sect extra"><img src="../assets/img/logos/sections/Frame 29.svg" alt=""></div>
          <div class="sect extra"><img src="../assets/img/logos/sections/Frame 30.svg" alt=""></div>
          <div class="sect extra"><img src="../assets/img/logos/sections/Frame 31.svg" alt=""></div>
          <div class="sect extra"><img src="../assets/img/logos/sections/Frame 32.svg" alt=""></div>
          <div class="sect extra"><img src="../assets/img/logos/sections/Frame 33.svg" alt=""></div>


        </div>
      </div>
      <h3>Area de Respeto</h3>
      <div class="logo-area">
        <p>El espacio de respeto del Imagotipo es medido basandonos en el alto de la "I" del mismo. Este debe ser igaul
          en todos los lados del imagotipo.</p>
        <div class="area-cont">
          <img src="../assets/img/logos/AreaRes.svg" alt="">
        </div>
      </div>
      <h3>Tamaño Mínimo</h3>
      <p>Para asegurrarnos que el imagotipo es legible en todo momento, este no debe ser menor a 50px en terminos
        digitales y por lo menos 2cm en medios impresos.</p>

      <h3>Guías de Uso</h3>
      <ul>
        <li>No alterar proporciones del logo.</li>
        <li>Los iconos pueden ser de los colores deseados siempre que sean alguno de los corporativos. Ademas, el icono
          superior e inferior deben ser del mismo color.</li>
        <li>La elección entre los diferentes iconos que se muestran en esta guía. A su vez, entender la mancha que
          provocan los iconos y mantener el balance entre estos y la tipografía del logo.</li>
        <li>No añadir efectos como sombreados o brillos.</li>
        <li>Buscar el maximo contraste entre las opciones disponibles y el fondo.</li>
        <li>Se permite que el fondo del Imagotipo sea de uno de los colores corporativos.</li>
      </ul>
    </div>








    <!-- Imagenes -->
    <div v-if="section.id === 'images'">
      <div class="audio">
        <div class="audOpen sect">
          <h2>Audio<span class="script">v</span>isu<span class="script">a</span>l</h2>
          <button class="buttonExp" @click="toggleSection('audContent')" aria-label="Toggle audiovisual section">
            {{ sectionStates.audContent ? 'x' : 'v' }}
          </button>
        </div>
        <p>
          Nuestros componentes audiovisuales se basan en generar dinamismo a traves de los diferentes elementos en
          nuestro
          sistema. De esta forma mostramos la variabilidad de la cual es capaz este rediseño.
        </p>

        <div id="audContent" class="imgInfo" :class="{ 'open': sectionStates.audContent }"
          aria-expanded="sectionStates.audContent">

          <h3>Animaciones</h3>

          <h4>Variabilidad de Marca</h4>
          <div class="audSep">
            <div class="vidsShow">
              <div class="image-example">
                <div class="image-container ">
                  <video controls autoplay muted loop src="../assets/vids/CESIDA_Animacion_AlejandraVeloso.mp4"></video>
                </div>



              </div>
              <div class="image-example">
                <div class="image-container ">
                  <video id="hugos" controls autoplay muted loop src="../assets/vids/CESIDA_HugoLogo.mp4"></video>
                </div>


              </div>
              <div class="image-example">
                <div class="image-container ">
                  <video controls autoplay muted loop src="../assets/vids/Copia de LogoANA.mp4"></video>
                </div>


              </div>
            </div>
            <div class="elemCont">
              <h4>Elementos</h4>
              <div class="vidsShow">
                <div class="image-example">
                  <div class="image-container ">
                    Mosca <video controls autoplay muted loop src="../assets/vids/MoscaBlack.mp4"></video>
                  </div>



                </div>
                <div class="image-example">
                  <div class="image-container ">
                    Tipografía <video controls autoplay muted loop src="../assets/vids/TipografiaAnimada.mp4"></video>
                  </div>



                </div>
              </div>
            </div>

            <div class="elemCont">
              <h4>Rótulos</h4>
              <div class="vidsShow">
                <div class="image-example">
                  <div class="image-container ">
                    <video controls autoplay muted loop src="../assets/vids/RotuloAbajo.mp4"></video>
                  </div>
                </div>

                <div class="image-example">
                  <div class="image-container ">
                    <video controls autoplay muted loop src="../assets/vids/RotuloGrandeWhite.mp4"></video>
                  </div>
                </div>

                <div class="image-example">
                  <div class="image-container ">
                    <video controls autoplay muted loop src="../assets/vids/RotuloFrase.mp4"></video>
                  </div>
                </div>

                <div class="image-example">
                  <div class="image-container ">
                    <video controls autoplay muted loop src="../assets/vids/RotuloLargoCentrado.mp4"></video>
                  </div>
                </div>

              </div>
            </div>
          </div>
        </div>


        <!-- Next one, estoy cansado jefe -->


        <div class="apOpen sect">
          <h2>Apli<span class="script">c</span>acio<span class="script">n</span>es</h2>
          <button class="buttonExp" @click="toggleSection('appContent')" aria-label="Toggle applications section">
            {{ sectionStates.appContent ? 'x' : 'v' }}
          </button>
        </div>
        <p> Usamos nuestros elementos y colores para conseguir generar composiciones divertidas y dinamicas. Junto con
          el
          uso de imagenes, generamos una serie que hace un gran uso del sistema.</p>



        <div id="appContent" class="imgInfo" :class="{ 'open': sectionStates.appContent }">
          <h3>Aplicaciones</h3>

          <div class="vidsShow">
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/Subway_Mockup-min.jpg" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/CartelHorizontal_Mockup-min.jpg" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/VerticalCartel_Mockup3-min.jpg" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/VerticalCartel_Mockup2-min.jpg" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/VerticalCartel_Mockup-min.jpg" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/MockupInstagram.png" alt="">
              </div>
            </div>
           
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/01 Free Tote Bag Mockup.png" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/01 Free Tote Bag Mockup4.png" alt="">
              </div>
            </div>
             <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/Cards_mockup9.png" alt="">
              </div>
            </div>
            <div class="image-example">
              <div class="image-container ">
                <img src="../assets/img/examples/Staff_Mockup-min.jpg" alt="">
              </div>
            </div>


          </div>
        </div>
      </div>









    </div>

  </section>
</template>

<script setup>
import { defineProps, ref } from 'vue';

const props = defineProps({
  section: {
    type: Object,
    required: true
  },
  isActive: {
    type: Boolean,
    default: false
  },
  exitDirection: {
    type: String,
    default: null
  }
});

// Estado para controlar la visibilidad de cada sección
// Inicializamos audContent como true para que comience abierta
const sectionStates = ref({
  audContent: true,
  appContent: false
});

// Función para alternar la visibilidad de una sección
const toggleSection = (sectionId) => {
  sectionStates.value[sectionId] = !sectionStates.value[sectionId];
};
</script>

<style scoped>
.section {
  display: none;
  padding: 2rem;
  margin-bottom: 2rem;
  opacity: 0;
  transform: translateX(30px);
  transition: opacity 0.4s ease, transform 0.4s ease;
}

.section.active {
  display: block;
  width: 100%;
  opacity: 1;
  transform: translateX(0);
  padding-top: 12rem;

}

.section.exit-left {
  opacity: 0;
  transform: translateX(-30px);
}

.section.exit-right {
  opacity: 0;
  transform: translateX(30px);
}

/* Font Example Styles */
.font-example {
  margin: 2rem 0;
  padding: 1.5rem;
  border: 1px solid #eee;
  border-radius: 4px;
  transition: border-color 0.4s ease;
}

.firstFont {
  font-size: larger;
}

.font-example.secondary-font {
  font-family: "Lexend Deca", sans-serif;
}

.font-example .font-heading {
  font-size: 2rem;
  margin-bottom: 1rem;
  font-family: "Transforma", Tahoma, Geneva, Verdana, sans-serif;
  transition: color 0.4s ease;
}

.font-example .font-subheading {
  font-family: "Lexend Deca", sans-serif;
  font-size: 3.5rem;
  margin-bottom: 1rem;
}

.font-example .secondFont {
  font-family: "Lexend Deca", sans-serif;
  font-size: 1.25rem;
  margin-bottom: 1rem;
  font-weight: 250;
  text-transform: uppercase;
}

.font-example .thirdFont {
  font-family: "Lexend Deca", sans-serif;
  font-size: 1.25rem;
  margin-bottom: 1rem;
  font-weight: 600;
  text-transform: uppercase;
}

.font-example .font-body {
  font-size: 1rem;
  margin-bottom: 2.5rem;
}

.font-example .font-body .textCorr {
  text-decoration: underline;
}

/* Color Palette Styles */
.color-palette {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  margin: 2rem 0;
  justify-content: space-between;
}

.color-swatch {
  width: 11rem;
  overflow: hidden;

}

.color-swatch .color-display {
  height: 10rem;
  border-radius: 16px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

}

.color-swatch .color-display h4 {
  color: white;
  font-size: 1rem;
}

.color-swatch .color-display.cesida-blue {
  background-color: #54c1dc;

}

.color-swatch .color-display.cesida-red {
  background-color: #e94f1e;
}

.color-swatch .color-display.cesida-green {
  background-color: #2eaa53;
}

.color-swatch .color-display.cesida-pink {
  background-color: #f087b5;
}

.color-swatch .color-display.cesida-yellow {
  background-color: #fdc609;
}

.color-swatch .color-display.cesida-black {
  background-color: #001100;
}

.color-swatch .color-display.cesida-dark-gray {
  background-color: #595F59;
}

.color-swatch .color-display.cesida-light-gray {
  background-color: #DFE2DF;
}

.color-swatch .color-display.cesida-white {
  background-color: #ffffff;

}

.color-swatch .color-info {
  padding: 1rem;

  font-size: 1rem;
}

.color-swatch .color-info .color-name {
  font-weight: bold;
  margin-bottom: 0.5rem;
}

/* Logo Variants Styles */
.logo-variants {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 1rem;
  margin: 2rem 0;
  justify-content: center;
  align-items: center;
}

.backDark {
  background-color: #181818;
  border-radius: 16px;


}

.logo-variant {


  max-width: 10rem;
  padding: 1.5rem;
}

.logo-variant .logo-img {
  max-width: 100%;
  height: auto;
  align-items: center;


}

.logo-variant .logo-img img {
  width: 100%;
  height: 100%;

}

.logo-area .area-cont {
  display: flex;
  justify-content: center;
  width: 20vw;
  min-width: 10rem;
  justify-self: center;
}

.logo-area .area-cont img {
  width: 100%;
  height: 100%;
}

.logo-plus {
  display: flex;
  flex-direction: column;
}

.logo-plus .logo-extras {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;

}

.logo-plus .logo-extras .extra {
  display: flex;
  padding: 1em 2rem;
  max-height: 6rem;
  box-sizing: content-box;
}

.logo-plus .logo-extras .sect {
  display: flex;
  padding: 1em 1rem;
  max-height: 4rem;
  box-sizing: content-box;
}

.logo-plus .logo-extras .extra img {
  width: 100%;
  height: 100%;
  box-sizing: content-box;
}

/* Icon Grid Styles */
.icon-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.icon-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;

}

.icon-item img {
  width: 100%;
  height: 100%;
}


.create-icon {
  display: flex;
  width: 30%;
  justify-self: center;
  min-width: 200px;
}

.create-icon img {
  width: 100%;
  height: 100%;
}



.vidsShow {
  display: flex;
  gap: 3rem;
  justify-content: center;
  flex-wrap: wrap;
  padding: 2rem;
}

.audSep {
  gap: 3rem;
  display: flex;
  flex-direction: column;
}

.image-example {

  display: flex;
  width: 40%;
  overflow: hidden;
  transition: border-color 0.4s ease;
  flex-direction: column;
}

.image-example .image-container {

  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: .5rem;
  border-radius: 1rem;
  overflow: hidden;
}

.image-example .image-container video {

  width: 100%;
  height: 100%;
  overflow: hidden;
  display: flex;

}

.image-example .image-container img {

  width: 100%;
  height: 100%;
  overflow: hidden;
  display: flex;

}



.image-example .image-caption {
  padding: 1rem;

  font-size: 0.9rem;
}


.audio {
  display: flex;
  flex-direction: column;
  max-width: 100vw;
}

.sect {
  display: flex;
  gap: 1rem;
  align-items: baseline;
}

.sect p {
  max-width: 100vw;
}

.sect button {
  background-color: transparent;
  border: 0px;
  font-size: medium;
  font-family: 'Lexend Deca';
  font-weight: 500;
  color: #DFE2DF;
  padding: 0;
  margin: 0;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.sect button:hover {
  color: #54c1dc;
}

.sect button:active {
  transform: scale(0.95);
}

.sect h2 {
  margin-bottom: 0;
  margin-top: 3rem;
}

/* Estilos para la animación del acordeón */
.imgInfo {
  max-height: 0;
  overflow: hidden;
  opacity: 0;
  transform: translateY(-10px);
  transition: max-height 0.5s ease-in-out, opacity 0.3s ease, transform 0.3s ease, padding 0.3s ease;
  padding-top: 0;
  padding-bottom: 0;
  flex-direction: column;
}

.imgInfo.open {
  max-height: 2000px;
  /* Valor alto para asegurar que todo el contenido sea visible */
  opacity: 1;
  transform: translateY(0);
  padding-top: 1rem;
  padding-bottom: 4rem;
}

@media (max-width: 768px) {
  .vidsShow {
 width: 100%;
  flex-direction: column;
  align-items: center;
}



.image-example {
  width: 100%;
}


}
</style>