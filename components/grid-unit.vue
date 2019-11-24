<template>
  <div class="grid-unit">
    <svg-icon class="plus" name="plus" />
  </div>
</template>

<style>
  .grid-unit {
    align-items: center;
    background: #F4E5CE;
    border: 1px solid rgba(0, 0, 0, 0);
    border-radius: 8px;
    display: flex;
    height: 63px;
    justify-content: center;
    transition: all 0.18s ease-in-out;
    width: 110px;
  }

  .grid-unit:hover {
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: rgba(0, 0, 0, 0.14) 0px 0px 14px;
    cursor: pointer;
    transform: scale(1.1, 1.1);
  }
</style>
