<template>
    <div v-if="response" class="content">
        <p>User ID: {{ response.userId }}</p>
        <p>Title: {{ response.title }}</p>
    </div>
</template>

<script>
    import axios from "axios";
    export default {
        name: 'firstAxios',
        props: {
            msg: String,
            msg2: String,
        },
        data: () => ({
            result: null
        }),
        created() {
            axios.get("https://jsonplaceholder.typicode.com/todos/1").then((response) => {
                    console.log(response.data);
                    this.response = response.data;
                })

                .catch(e => {
                    // Capturamos los errores
                    console.log(e);
                })
        }
    };
</script>

<style scoped lang="scss">
</style>