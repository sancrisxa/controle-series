<script>

    export default {

        props: ['users'],

        data () {

            return {

                list: []
            }

        },

        ready() {

            this.list = JSON.parse(this.users)
        }

    }
</script>
<template>
    <div>
        <table class="table table-bordered table-striped table-hover">
            <thead>
                <tr>
                    <th>Nome</th>
                    <th>E-mail</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="user in list">
                    <td>{{ user.name }}</td>
                    <td>{{ user.email }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<style scoped="">

</style>

