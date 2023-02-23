<template>
<div style>
<H1>AG-Grid Example</H1>
  <ag-grid-vue
   style="width: 1000px; height: 500px"
    class=" container ag-theme-alpine ag-grid"
    :columnDefs="columnDefs"
    :rowData="rowData"
  >
  </ag-grid-vue>
</div>

</template>

<script>

import { AgGridVue } from "ag-grid-vue3";
import "ag-grid-community/styles/ag-grid.css"; // Core grid CSS, always needed
import "ag-grid-community/styles/ag-theme-alpine.css";

export default {
  name: "App",
  components: {
    AgGridVue,
  },
  setup() {
    return {
      columnDefs: [
        { headerName: "Make", field: "make" },
        { headerName: "Model", field: "model" },
        { headerName: "Price", field: "price" },
      ],
      rowData: [
        { make: "Toyota", model: "Celica", price: 35000 },
        { make: "Ford", model: "Mondeo", price: 32000 },
        { make: "Porsche", model: "Boxter", price: 72000 },
      ],
    };
  },
};
</script>
