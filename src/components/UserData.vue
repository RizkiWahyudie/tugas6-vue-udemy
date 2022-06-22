<template>
    <div class="form">
        <form @submit.prevent="submitUser()">
            <div>
                <label>Name</label>
                <input type="text" v-model="valueName">
            </div>
            <div>
                <label>Age</label>
                <input type="text" v-model="valueAge">
            </div>
            <button>Add User</button>
        </form>
    </div>
</template>

<script>
export default {
    emits: ['add-user'],
    data() {
        return {
            valueName: '',
            valueAge: ''
        }
    },
    methods: {
        submitUser() {
            this.$emit('add-user', this.valueName, this.valueAge);
        }
    }
}
</script>