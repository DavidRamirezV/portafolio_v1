<template>
  <div class="fab-container">
    <div class="fab shadow">
      <div class="fab-content">
        <span class="material-icons">menu</span>
      </div>
    </div>

    <div class="sub-button shadow">
      <a v-on:click="displayHandlerChild(5)">
        <span class="material-icons">alternate_email</span>
      </a>
    </div>

    <div class="sub-button shadow">
      <a v-on:click="displayHandlerChild(4)">
        <span class="material-icons">folder_open</span>
      </a>
    </div>

    <div class="sub-button shadow">
      <a v-on:click="displayHandlerChild(3)">
        <span class="material-icons">trending_up</span>
      </a>
    </div>

    <div class="sub-button shadow">
      <a v-on:click="displayHandlerChild(2)">
        <span class="material-icons">school</span>
      </a>
    </div>

    <div class="sub-button shadow">
      <a v-on:click="displayHandlerChild(1)">
        <span class="material-icons">person</span>
      </a>
    </div>
  </div>
</template>
  
<script>
export default {
  name: 'FloatingActionButton',
  data: () => ({
    fab: false,
  }),
  methods: {
    displayHandlerChild: function (pressed) {
      this.$emit('handlerData', pressed);
    }
  }
};
</script>

<style lang="scss">
$primary: rgb(75, 162, 255);

.fab-container {
  flex-grow: 1;
  display: none;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  user-select: none;
  position: absolute;
  bottom: 30px;
  right: 30px;
  cursor: pointer;

  &:hover {
    height: 100%;

    .sub-button:nth-child(2) {
      transform: translateY(-80px);
    }

    .sub-button:nth-child(3) {
      transform: translateY(-140px);
    }

    .sub-button:nth-child(4) {
      transform: translateY(-200px);
    }

    .sub-button:nth-child(5) {
      transform: translateY(-260px);
    }

    .sub-button:nth-child(6) {
      transform: translateY(-320px);
    }
  }

  .fab {
    position: relative;
    height: 70px;
    width: 70px;
    background-color: $primary;
    border-radius: 50%;
    z-index: 2;

    .fab-content {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100%;
      width: 100%;
      border-radius: 50%;

      .material-icons {
        color: white;
        font-size: 48px;
      }
    }
  }

  .sub-button {
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    bottom: 10px;
    right: 10px;
    height: 50px;
    width: 50px;
    background-color: $primary;
    border-radius: 50%;
    transition: all .3s ease;

    &:hover {
      cursor: pointer;
    }

    .material-icons {
      color: white;
      padding-top: 6px;
    }
  }
}</style>