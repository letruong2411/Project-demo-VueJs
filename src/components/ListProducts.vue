<template>
    <div>
        <div class="container">
        <h1>List Students</h1>
        <button type="button" class="btn btn-primary">ADD Students</button>           
        <table class="table table-striped">
            <thead>
            <tr>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Email</th>
                <th> Edit</th>
                <th>Delete</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td vfor="Students in  st"> {{FName}} </td>
                <td> {{LName}} </td>
                <td> {{Email}} </td>
                <td> <button type="button" class="btn btn-danger">Edit</button> </td>
                <td> <button type="button" class="btn btn-danger">Delete</button> </td>
            </tr>
            <tr>
                <td>Mary</td>
                <td>Moe</td>
                <td>mary@example.com</td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>July</td>
                <td>Dooley</td>
                <td>july@example.com</td>
                <td></td>
                <td></td>
            </tr>
            </tbody>
        </table>
        </div>
    </div>
</template>

<script>
    export default {
        name:'ListProducts',
        data() {
            return {
                FName:'Le',
                LName: 'Truong',
                Email: 'truong.le2241199@gmail.com'
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>