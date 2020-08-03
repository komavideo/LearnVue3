<template>
<div>
    <h1>Vue Tempalte</h1>
</div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
// helo vue 3.
export default {
name: "my-header",
components: {
    // HelloWorld
},
data: function() {
    return {};
},
props: {},
computed: {
    displayYMD() {
        return new Date().getFullYear().toString();
    }
},
methods: {},
beforeCreate: function() {},
created: function() {},
beforeMount: function() {},
mounted: function() {},
beforeUpdate: function() {},
updated: function() {},
activated: function() {},
deactivated: function() {},
beforeDestroy: function() {},
destroyed: function() {},
errorCaptured: function() {}
};
</script>

<style scoped>
</style>