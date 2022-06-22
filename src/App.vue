<template>
    <div>
        <user-data
            @add-user="addUser"
        ></user-data>
        <active-user
            v-for="users in user"
            :key="users.id"
            :id-user="users.id"
            :name="users.name"
            :age="users.age"
        ></active-user>
    </div>
</template>

<script>
export default {
    data() {
        return {
            user: [
                {
                    id: '1',
                    name: 'Rizki',
                    age: '20'
                },
                {
                    id: '2',
                    name: 'Dita',
                    age: '19'
                }, 
                {
                    id: '3',
                    name: 'Raisa',
                    age: '7'
                }
            ]
        }
    },
    methods: {
        addUser(valueName, valueAge) {
            const userAdd =
                {
                    id: new Date().toISOString(),
                    name: valueName,
                    age: valueAge
                };
            this.user.push(userAdd);
        }
    }
}
</script>