<script setup>

</script>

<template>
    <div class="container">
      <div class="north">
        <slot name="north">
          <img :src="Img" />
        </slot>
      </div>
      <div class="east">
        <slot name="east">
          <img :src="Img" />
        </slot>
      </div>
      <div class="west">
        <slot name="west">
          <img :src="Img" />
        </slot>
      </div>
      <div class="south">
        <slot name="south">
          <img :src="Img" />
        </slot>
      </div>
    </div>
  </template>
  
  
  <style>
  .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 10px;
  }
  
  .north {
    grid-column: 1 / span 2;
    height: 100px;
  }
  
  .south {
    grid-column: 1 / span 2;
    height: 100px;
  }
  
  .east {
    width: 100px;
    height: 100px;
  }
  
  .west {
    width: 100px;
    height: 100px;
  }
  </style>
  