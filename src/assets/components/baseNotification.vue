<template>
    <div class="notification" :style="notificationStyle">
        <div class="notification-modal-header">
            <div class="notification-title">
                <img :src="icon" alt="notification">
                <p>{{title}}</p>
            </div>
            <button @click="handleDelete" class="cross">
                X
            </button>
        </div>
        <div class="notification-frame">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BaseNotification',
    props: {
        title: String,
        icon: String,
        color: String,
        borderColor: String,
        notificationId: Number,
        required: true
    },
    methods: {
        handleDelete() {
            this.$emit('delete', this.notificationId)
        },
    },
    computed: {
        notificationStyle() {
            return {
                backgroundColor: this.color,
                border: `2px solid ${this.borderColor}`
            };
        }
    }
}
</script>

<style scoped>
.notification {
    width: 527px;
    height: 160px;
    padding: 24px;
    border: 2px solid;
    radius: 16px;
    border-radius: 8px;
    box-shadow: 0px 6px 12px 0px #0000001A;
}

.notification-modal-header {
    display: flex;
    width: 479px;
    height: 32px;
    justify-content: space-between;
    margin-bottom: 8px;
    gap: 16px;
    font-size: 20px;
}

.notification-title {
    display: flex;
    gap: 16px;
}

.cross {
    display: flex;
    border: none;
    cursor: pointer;
    background-color: transparent;
}

.cross:hover {
    font-size: 17px;
}

.notification-frame {
    display: flex;
    width: 479px;
    height: 72px;
    padding: 0px 0px 0px 48px;
    color: grey;
    font-size: 17.4px; /* pas trouvé mieux pour aligner avec la croix, question à poser*/
}
</style>