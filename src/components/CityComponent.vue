<script>
export default {
  name: "CityComponent",
  props: [
    "key",
    "name",
    "country_name",
    'country_code',
    'state_name',
    'state_code',
    'latitude',
    'longitude'
    //TODO: crear una propiedad para determinar si al componente se le puede hacer click
  ],
};
</script>

<template>
  <!--TODO: Utilizar la propiedad creada para controlar el click. Cuando el componente es "clickeable", redirigir a la pagina del pais.
  Mira las rutas para ver como redirigir al usuario.-->
  <div class = "country">
  <!--TODO: Poblar el HTML con las propiedades. Usar https://countryflagsapi.com/png/${code}-->
  <img
      width="200"
      height="200"
      src ="../assets/city.jpg"
    />
  <h1>Pais: {{country_name}} {{country_code}}</h1><br>
  <p>Estado : {{state_name}} {{state_code}}</p><br>
  <p>Latitude : {{latitude}}</p><br>
  <p>Longitude : {{longitude}}</p><br>
  </div>
</template>

<style scoped>
.country {
  padding: 2px;
  white-space: nowrap;
  width: 350px;
  height: 350px;
  border-style: solid;
  border-radius: 5px;
  border-color: grey;
}

.country-hover:hover {
  background-color: rgb(49, 49, 49);
  cursor: pointer;
}

h1 {
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
