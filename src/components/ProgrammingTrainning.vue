<script setup>
import WelcomeItem from './WelcomeItem.vue'
// import DocumentationIcon from './icons/IconDocumentation.vue'
// import ToolingIcon from './icons/IconTooling.vue'
// import EcosystemIcon from './icons/IconEcosystem.vue'
// import RecursoItem from './icons/IconoRecurso.vue'
import Edutecno from './icons/IconEdutecno.vue'
import Aiep from './icons/IconAiep.vue'
import Alura from './icons/IconAlura.vue'
import Duoc from './icons/IconDuoc.vue'
import SanSebastian from './icons/IconSansebastian.vue'
import Umayor from './icons/IconUmayor.vue'
import EscuelaComercio from './icons/IconEscuelaComercio.vue'
import IPChile from './icons/IconChile.vue'
// import Activeit from './icons/IconActiveit.vue'
// import CommunityIcon from './icons/IconCommunity.vue'
// import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <h1>Formación</h1>
  <WelcomeItem>
    <template #icon>
      <IPChile />
    </template>
    <template #heading>[mar 2024] IPChile</template>
    Técnico de nivel superior analista programador computacional.<br />
    alumno regular.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <Edutecno />
    </template>
    <template #heading>[mar 2023 - ago 2023] Otec Edutecno</template>
    Bootcamp desarrollo de aplicaciones full-stack javascript trainee.<br />
    duración 472 horas.
  </WelcomeItem>
  <WelcomeItem>
    <template #icon>
      <Aiep />
    </template>
    <template #heading>[ago 2022-nov 2022] Instituto Profesional AIEP.</template>
    Diplomado marketing digital y gestión estratégica.<br />
    duración 90 horas.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <Aiep />
    </template>
    <template #heading>[ene 2022-jun 2022] Instituto Profesional AIEP.</template>
    Bootcamp desarrollo de aplicaciones full stack java trainee.<br />
    duración 480 horas.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <Alura />
    </template>
    <template #heading>[dic 2021- jun 2022] Alura Latam.</template>
    Bootcamp full stack frontend.<br />
    duración 522 horas.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <Duoc />
    </template>
    <template #heading>[ene 2022-may 2021] Duoc UC.</template>
    Bootcamp desarrollo de aplicaciones móviles android trainee.<br />
    duración 480 horas.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SanSebastian />
    </template>
    <template #heading>[may 2020-nov 2020] Universidad San Sebastián.</template>
    Diplomado de dirección comercial y ventas.<br />
    duración 112 horas.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <Umayor />
    </template>
    <template #heading>[mar 2013 - 2017] Universidad Mayor.</template>
    Ingeniería en administración mención marketing y gestión comercial.<br />
    titulado.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EscuelaComercio />
    </template>
    <template #heading>[mar 2010 - 2012] Escuela de comercio de santiago.</template>
    Técnico nivel superior en administración recursos humanos.<br />
    titulado.
  </WelcomeItem>
</template>
