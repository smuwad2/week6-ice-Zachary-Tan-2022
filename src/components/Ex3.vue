<script>
export default {

    // add code here
    data() {
        return {
            selection: "username"
        }
    }

}
</script>

<template>
    <h1>Please select your login option</h1>
    <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
    <select v-model="selection">
        <option selected value="username">Username login</option>
        <option value="email address">Email login</option>
    </select>

    <div>
        <label v-if="selection == 'username'">Username</label>
        <label v-else>Email</label>
        <input :placeholder="`Enter your ${selection}`">
    </div>
</template>
