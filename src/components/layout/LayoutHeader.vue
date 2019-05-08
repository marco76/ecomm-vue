<template>
        <el-container>
            <img alt="Vue logo" src="../../assets/logo_cropped-15_10_logo_dsf.png" style=" height: 50px">
            <Header></Header>
        </el-container>
</template>

<script>

    import Header from "../Header";
    export default {
        name: "LayoutHeader",
        components: {Header}
    }
</script>

<style scoped>
    .el-header {
        background-color: #FFFFFF;
        color: #333;
        line-height: 60px;
    }
</style>