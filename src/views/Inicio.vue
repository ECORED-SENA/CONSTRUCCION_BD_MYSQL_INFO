<template lang="pug">
section
  BannerPrincipal.mb-5


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p Bienvenido al programa de formación Construcción de bases de datos con MYSQL. 
      br
      br
      | En este curso el aprendiz desarrolla una serie de conocimientos que van desde el proceso de selección de las herramientas necesarias para la construcción de la base de datos en el lenguaje estructurado de consulta SQL para la manipulación y programación y, las pruebas que le permiten determinar si el modelo de datos presentado corresponde a los requerimientos previamente establecidos.
      br
      br
      | Es de referir que programar en este lenguaje lleva inherente la necesidad de conocer como mínimo el funcionamiento de MYSQL y, que la utilización de cualquier otra base de datos o método de conexión no conlleva cambios significativos en el script que se trabaja a lo largo del curso.


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa

    p.mb-4 El sector TIC juega un papel importante en el país, puesto que aporta a la productividad de la economía, atrayendo cada vez más inversionistas y fomentando la generación de empresas y puestos de trabajo en esta área. Para el año 2019 este sector registró una participación de 3,6% respecto al valor agregado nacional y, según Fedesoft se están generando 120.000 empleos y se vende 16,5 billones de pesos, representando 1,7% del PIB. [1]
      br
      br
      | En la actualidad un gran porcentaje de software y aplicativos que se encuentran en el mercado hacen uso de bases de datos con MySQL. Además, es de vital importancia contar con una gestión eficiente de la gran cantidad de información que se genera diariamente a través de múltiples dispositivos. Las bases de datos bien gestionadas marcan una ventaja competitiva entre las diferentes empresas.
      br
      br
      | En consecuencia, los diferentes sectores productivos de la economía colombiana se encuentran en la búsqueda de personal con las mejores capacidades laborales y profesionales, que cuenten con el dominio en la administración y manipulación de bases de datos, para así contribuir al desarrollo económico, social y tecnológico de su entorno y del país.
      br
      br
      |El SENA ofrece el programa de formación Construcción de bases de datos con MySQL, con todos los elementos de formación profesional, social, tecnológico y cultural, aportando como elementos diferenciadores metodologías y plataformas para el desarrollo de software de calidad, con acceso a tecnologías de última generación y una estructuración sobre métodos más que sobre contenidos, lo que potencia la formación de ciudadanos librepensadores, con capacidad crítica, solidaria y emprendedora, factores que lo acreditan y lo hacen pertinente y coherente con su misión, innovando permanentemente de acuerdo con las tendencias y cambios tecnológicos y las necesidades del sector empresarial y de los trabajadores, impactando positivamente la productividad, la competitividad, la equidad y el desarrollo del país.

    .reference
      p [1] Portafolio (2020). Fedesoft pide cuota nacional en equipo de gurús tecnológicos.  https://www.portafolio.co/economia/fedesoft-pide-cuota-nacional-en-equipo-de-gurus-tecnologicos- 540800

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Población<br>objetivo

    p La formación está dirigida a personas interesadas en afianzar sus conocimientos en la construcción de bases de datos relacionales con MySQL, en formación complementaria virtual SENA.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4. Estrategia<br>metodológica

    p.mb-4 Centrada en la construcción de la autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportada en la utilización de las Tecnologías de la Información y la Comunicación (TIC), integradas en ambientes virtuales de aprendizaje, que en todo caso recrean el contexto productivo, vinculan al aprendiz con la realidad cotidiana y con el desarrollo de las competencias. 
      br
      br
      | Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el quehacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:      

    ul.fa-ul
      li.mb-2 #[span.li--clr.fa-li #[i.fas.fa-angle-right ]] El instructor - tutor
      li.mb-2 #[span.li--clr.fa-li #[i.fas.fa-angle-right ]] El entorno
      li.mb-2 #[span.li--clr.fa-li #[i.fas.fa-angle-right ]] Las TIC
      li.mb-2 #[span.li--clr.fa-li #[i.fas.fa-angle-right ]] El trabajo colaborativo

    
    



  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>

<style lang="sass" scoped>
.resultados-aprendizaje
  &__item
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0

.desarrollo-contenidos
  &__item
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 25px
    padding: 5px
    border-radius: $base-border-radius

    &__texto
      display: flex
      align-items: center

    &__icono
      display: block
      background-color: $color-sistema-g
      font-size: 20px
      font-weight: $base-black-font-weight
      text-align: center
      padding: 10px
      line-height: 1em
      width: 40px
      margin-right: 15px

    &:last-child
      margin-bottom: 0

    &:hover
      background-color: $color-sistema-g
      font-weight: $base-black-font-weight
      color: $color-sistema-a
</style>
