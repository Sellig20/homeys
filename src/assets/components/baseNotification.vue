<template>
  <div class="notification">
    <div class="notification-modal-header">
        <img src="/src/assets/icons/Danger.svg" alt="Danger">
        <p>Modal Window</p>
        <p class="cross">X</p>
    </div>
    <div class="notification-frame">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor</p>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped> 
.notification {
    width: 527px;
    height: 160px;
    radius: 16px;
    border: 2px solid #D29393;
    padding: 24px;
    background: #F7E4E4;
    border-radius: 8px;
    box-shadow: 0px 6px 12px 0px #0000001A;
}

.cross {
    padding: 0px 0px 0px 256px;
}

.notification-modal-header {
    display: flex;
    gap: 16px;
    font-size: 20px;
    margin-bottom: 8px;
}

.notification-frame {
    display: flex;
    padding: 0px 0px 0px 48px;
    color: grey;
    font-size: 16px;
}
</style>