<template>
  <div class="notification-container">
    <base-notification title="Danger" icon="/src/assets/icons/Danger.svg" color="#F7E4E4" borderColor="#D29393" alt="Danger"/>
    <base-notification title="CheckCircle" icon="/src/assets/icons/CheckCircle.svg" color="#E4F7E8" borderColor="#89B291" alt="Info"/>
    <base-notification title="Warning" icon="/src/assets/icons/Warning.svg" color="#F7F2E4" borderColor="#D4C296" alt="Info"/>
    <base-notification title="Info" icon="/src/assets/icons/Info.svg" color="#E4E9F7" borderColor="#96A8D8" alt="Info"/>
  </div>
</template>

<script>
import BaseNotification from '/src/assets/components/BaseNotification.vue';

export default {
  components: {BaseNotification},
}
</script>

<style scoped>
.notification-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100vh;
  gap: 20px;
  align-items: center;
}
</style>
