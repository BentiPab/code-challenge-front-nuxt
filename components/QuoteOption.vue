<template>
  <div class="cuote-option">
    <header class="option-header">${{ value.Precio }}</header>
    <body>
      <p class="option-body">
        {{ value.descripcion }}
      </p>
    </body>
    <footer>
      <p class="option-footer">{{ value.PlazoEntrega }}</p>
    </footer>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.cuote-option {
  width: 100%;
  text-align: center;
  border-left: 2px solid #ff0000;
  border-top: 2px solid #008cff;
  border-right: 2px solid #33cc33;
  border-bottom: 2px solid #ffcc00;
  border-radius: 15px;
  margin-top: 20px;

  display: grid;
  grid-template-rows: repeat(3, 60px);
  padding: 0;
  min-width: 200px;

  .option-header {
    font-size: 2rem;
    color: dodgerblue;
    grid-row: 1;
    background-color: lightgrey;
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;
  }
  .option-body,
  .option-header,
  .option-footer {
    text-align: center;
  }
  .option-body,
  .option-header {
    font-weight: bold;
  }

  .option-footer {
    opacity: 0.5;
  }
}
</style>
