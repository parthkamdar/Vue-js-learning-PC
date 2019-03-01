<template>
  <div class="col-6">
    <div class="panel">
      <div class="panel-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>
<script>

</script>
<style>
  .panel-body{
    background: #ddd;
    width: 200px;
    height: 100px;
    padding: 10px;
    margin: 10px;
    text-align: center;
  }
  .quote{
    cursor: pointer;
  }
</style>
