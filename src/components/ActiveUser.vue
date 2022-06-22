<template>
    <div class="form">
        <h2>{{ name }}</h2>
        <ul>
            <li>Age : {{ age }}</li>
            <li>ID : {{idUser}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    props: {
        idUser: String,
        name: String,
        age: String
    },
    data() {
        return {
            
        }
    }
}
</script>