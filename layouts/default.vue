<template>
  <div>
    <nuxt />
    <modal-portal />
  </div>
</template>

<style>
html {
  background: #FFF4E3;
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

h1 {
  color: #345237;
  font-size: 21px;
  font-weight: 400;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

/*
    Based on the original styles from vue-thin-modal:
    node_modules/vue-thin-modal/dist/vue-thin-modal.css
  */
  .modal-open {
    overflow: hidden;
  }
  .modal-open .modal-wrapper {
    display: block;
  }
  .modal-wrapper {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
  }
  /*  Backdrop
  ----------------------------------------*/
  .modal-backdrop {
    opacity: 1;
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 1000;
  }
  .modal-backdrop-enter-active,
  .modal-backdrop-leave-active {
    transition: opacity 300ms ease-out;
  }
  .modal-backdrop-enter,
  .modal-backdrop-leave-active {
    opacity: 0;
  }
  /*  Content
  ----------------------------------------*/
  .modal-content-wrapper {
    overflow: auto;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 100%;
    z-index: 1001;
  }
  .modal-content {
    position: absolute;
    left: 0;
    right: 0;
    margin-left: auto;
    margin-right: auto;
    transform: translateY(0);
  }
  .modal-content-enter-active,
  .modal-content-leave-active {
    transition: 300ms cubic-bezier(0.51, 0.21, 0.38, 0.98);
    transition-property: opacity, transform;
  }
  .modal-content-enter,
  .modal-content-leave-active {
    opacity: 0;
    transform: translateY(-50px);
  }
  .mainContentIndex {
    font-size: 28px;
    color: var(--c-blue);
    font-weight: 500;
  }
  .centeredContent {
    max-width: 816px;
    margin: 0 auto;
    & .paneLeft {
      flex: 1;
    }
    & .paneRight {
      width: 18.5rem;
      margin-left: 1.5rem;
    }
  }
</style>
