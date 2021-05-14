<template>
  <div class="cuote-option">
    <header class="option-header">
      <template v-if="value.Precio === 0">
        <h2 class="free">GRATIS!</h2>
      </template>
      <template v-else> 
        ${{ value.Precio }}
         </template>
    </header>
    <body class="option-body">
      {{ value.descripcion }}
    </body>
    <footer class="option-footer">
      {{ value.PlazoEntrega }}
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
  border-left: 3px solid #ff0000;
  border-top: 3px solid #008cff;
  border-right: 3px solid #33cc33;
  border-bottom: 3px solid #ffcc00;
  margin-top: 20px;
  display: grid;
  grid-template-rows: repeat(3, 60px);
  padding: 1px;
  min-width: 200px;
  max-width: 200px;
  border-style: solid;
  border-radius: 15px;

  .option-header {
    font-size: 2rem;
    color: white;
    grid-row: 1;
    background-color: dodgerblue;
    border-top-right-radius: 15px;
    border-top-left-radius: 15px;
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
  .option-body,
  .option-footer {
    background-color: #e6f2ff;
  }
  .option-footer {
    color: black;
    border-bottom-left-radius: 15px;
    border-bottom-right-radius: 15px;
  }

  .free {
    margin: 0;
    line-height: 48px;
    margin-block-end: 0;
    animation-name: bounce;
    animation-duration: 1.5s;
    animation-iteration-count: infinite;
    font-size: 2rem;
    font-weight: bold;
  }

  @keyframes bounce {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.1);
    }

    100% {
      transform: scale(1);
    }
  }
}
</style>
