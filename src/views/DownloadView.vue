<template>
  <div class="descarga">
    <h1>Descargas</h1>

    <div class="d-flex justify-content-center">
      <a class="flecha" href="https://www.gifsanimados.org/cat-flechas-111.htm"></a>
      <img
        src="https://www.gifsanimados.org/data/media/111/flecha-imagen-animada-0025.gif"
        border="0"
        alt="Descarga Aquí Cv"
        height="50"
      />
      <button @click="descargarPDF">
        <IMG src="http://gifs.gratis.es/informatica/download/02.gif" width="200" height="70"></IMG>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    descargarPDF() {
      // Import the PDF file
      import('@/assets/RodolfoParada.pdf').then((pdfUrl) => {
        const link = document.createElement('a')
        link.href = pdfUrl.default // Access the default export
        link.target = '_blank'
        link.download = 'curriculum-RodolfoParada.pdf'
        link.type = 'application/pdf'

        document.body.appendChild(link)

        link.click()

        document.body.removeChild(link)
      })
    }
  }
}
</script>

<style scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
