<template>
    <div v-if="response" class="content">
        <p>User ID: {{ response.userId }}</p>
        <p>Title: {{ response.title }}</p>
        <p>ID: {{ response.body }}</p>

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
            response: null
        }),
        created() {

            let post = {
                title: 'foo',
                body: 'bar',
                userId: 1
            };
            axios.put("https://jsonplaceholder.typicode.com/posts/1", post).then((response) => {
                console.log(response);
            });
            axios.get("https://jsonplaceholder.typicode.com/posts/1").then((response) => {
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