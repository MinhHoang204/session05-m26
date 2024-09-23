<template>
    <div>
        <h1>List rendering</h1>
        <ul v-for="user in listUser" :key="user.id">
            <li>
                <span>Id: {{ user.id }}</span>
                <span>Name: {{ user.name }}</span>
            </li>
        </ul>
    </div>
</template>

<script>
    const listUser = [
        {
            id:1,
            name: "Nguyen Van A",
        },
        {
            id:2,
            name: "Nguyen Van B",
        },
        {
            id:3,
            name: "Nguyen Van C",
        }
    ]
</script>