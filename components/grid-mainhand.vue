<template>
  <div class="grid-mainhand">
    <svg-icon class="plus" name="plus" />
  </div>
</template>

<style>
  .grid-mainhand {
    align-items: center;
    background: #F4E5CE;
    border: 1px solid rgba(0, 0, 0, 0);
    border-radius: 8px;
    display: flex;
    height: 333px;
    justify-content: center;
    margin-right: 24px;
    transition: all 0.18s ease-in-out;
    width: 159px;
  }

  .grid-mainhand:hover {
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: rgba(0, 0, 0, 0.14) 0px 0px 14px;
    cursor: pointer;
    transform: scale(1.05, 1.05);
  }
</style>
