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
      <button class="btn btn-primary" @click="descargarPDF">
        Haz click Aquí
        <!-- <img src="../assets/flecha-animada.gif" alt="" width="150" height="150" /> -->
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

.btn {
  margin: 20px;
}
</style>
