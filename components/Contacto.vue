<template>
  <div class="bg-gray-50">
    <div class="relative">
      <div style="width: 100%">
        <iframe
          width="100%"
          height="600"
          frameborder="0"
          scrolling="no"
          marginheight="0"
          marginwidth="0"
          src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=es&amp;q=Refiner%C3%ADa%20Web,%20house,%20Palma%20de%20Mallorca,%20Spain+(Refineria%20Web)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
          ><a href="https://www.mapsdirections.info/marcar-radio-circulo-mapa/"
            >Dibuja un circulo Google Maps</a
          ></iframe
        >
      </div>
      <div
        class="
            
          container
          xl:max-w-sm
          xl:mx-auto
          flex-1 flex flex-col
          items-center
          justify-center
          px-2
          xl:absolute
          xl:top-2
          left-3/4
        "
      >
        <div class="bg-white px-6 py-8 rounded shadow-md text-black w-full">
          <h1 class="mb-8 text-3xl text-center">Contacto</h1>
          <form action="" @submit.prevent="validateForm">
            <label for="">Nombre</label>
            <input
              type="text"
              class="block border border-grey-light w-full p-3 rounded mb-4"
              name="fullname"
              placeholder="Nombre completo"
              v-model.trim="contacto.nombre"
            />
            <label for="">Email</label>
            <input
              type=" email"
              class="block border border-grey-light w-full p-3 rounded mb-4"
              name="email"
              placeholder="Email"
              v-model.trim="contacto.email"
            />
            <label for="">Teléfono</label>
            <input
              type="tel"
              class="block border border-grey-light w-full p-3 rounded mb-4"
              name="telefono"
              placeholder="Teléfono"
              v-model.number="contacto.tel"
            />
            <label for="cehckbox" class="mb-4 block">
                <input
              type="checkbox"
              class=" border border-grey-light p-3 rounded"
              name="cehckbox"
              v-model="contacto.condiciones"
            />
                He leído y acepto los términos y condiciones de uso
            </label>
            <div class="flex justify-center">
                <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded w-40 ">
                Button
            </button>
            </div>
            
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            contacto: {
                nombre : "",
                email: "",
                tel: "",
                condiciones: false
            }
        }
    },
    methods: {
        validateForm() {
            // Aquí validariamos los datos de nuestro contacto antes de enviar los datos a la BBDD
        }
    },
};
</script>

<style scoped>
</style>