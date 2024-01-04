<script setup>
import WelcomeItem from './WelcomeItem.vue'
// import DocumentationIcon from './icons/IconDocumentation.vue'
// import ToolingIcon from './icons/IconTooling.vue'
// import EcosystemIcon from './icons/IconEcosystem.vue'
// import RecursoItem from './icons/IconoRecurso.vue'
import Activeit from './icons/IconActiveit.vue'
import Blokey from './icons/IconBlokey.vue'
import CastilloGrafico from './icons/IconCastillo.vue'
// import CommunityIcon from './icons/IconCommunity.vue'
// import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <h1>Experiencia</h1>
  <WelcomeItem>
    <template #icon>
      <Activeit class="a" />
    </template>
    <template #heading>[Sept 2022] ActiveIt Consultores</template>

    Cargo:Desarrollador trainee.<br />
    ➢ Principalmente utilice el Framework de Vue.js en Frontend y use la metodología de Scrum.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <Blokey />
    </template>
    <template #heading>[Ene 2022-May 2022] Blokey Limitada.</template>
    Cargo: Diseño estrategia Comercial.<br />
    Principales Funciones:<br />
    ➢ Desarrollé plan comercial y gestioné contactos con clientes potenciales.<br />
    Logros: Coordiné con los plazos indicados por CORFO.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CastilloGrafico />
    </template>
    <template #heading>[Jun 2016-May 2020] Castillo Gráfico Limitada.</template>
    Principales Funciones:<br />
    ➢ Organicé el funcionamiento de la empresa en ámbitos de venta, recursos humanos, finanzas.<br />
    ➢ Desarrollé constantemente estrategias orientadas a las ventajas competitivas y propuesta de
    valor que permitieron resultados potentes.<br />
    ➢ Desarrollé, diseñé e implementé Plan Comercial.<br />
    Logros:<br />
    ➢ Desarrollé estrategias de fidelización que aumentaron la frecuencia de compra en un 90% en el
    segundo año 2018.<br />
    ➢ Evalué un 32% en el aumento de las ventas en el año 2018 con la implementación de un plan de
    marketing.<br />
    ➢ Dirigí el plan de marketing para un nicho de mercado con resultado en aumento de ventas 25% en
    el año 2019.
  </WelcomeItem>

  <!-- <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Got stuck? Ask your question on
    <a href="https://chat.vuejs.org" target="_blank" rel="noopener">Vue Land</a>, our official
    Discord server, or
    <a href="https://stackoverflow.com/questions/tagged/vue.js" target="_blank" rel="noopener"
      >StackOverflow</a
    >. You should also subscribe to
    <a href="https://news.vuejs.org" target="_blank" rel="noopener">our mailing list</a> and follow
    the official
    <a href="https://twitter.com/vuejs" target="_blank" rel="noopener">@vuejs</a>
    twitter account for latest news in the Vue world.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its sustainability. You can help
    us by
    <a href="https://vuejs.org/sponsor/" target="_blank" rel="noopener">becoming a sponsor</a>.
  </WelcomeItem> -->
</template>
<style>
/* .a {
  width: 20px;
  height: 20px;
} */
</style>
