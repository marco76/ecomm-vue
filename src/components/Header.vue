<template>
    <span>
    <el-menu class="el-menu-demo" mode="horizontal">
        <el-submenu v-for="item of appmenu" :index="item.index">
            <template slot="title">{{item.title}}</template>
            <el-menu-item v-for="subitem of item.subitems" :index="subitem.index">
                {{subitem.title}}
            </el-menu-item>

        </el-submenu>

    </el-menu>
    <div class="line"></div>
    </span>
</template>

<script>
    export default {
        name: "Header",
        data() {
            return {appmenu : [
                {"title": "Obermaterial", "index" : "1",
                 "subitems": [
                     {"title": "Leder", "index" : "1-1"},
                     {"title": "Synthetik", "index" : "1-2"},
                     {"title": "Socken", "index" : "1-3"},
                     {"title": "Texil & Stoffe", "index" : "1-4"},
                 ]},
                    {"title": "Futtermaterial", "index" : "2",
                        "subitems": [
                            {"title": "Leder", "index" : "2-1"},
                            {"title": "Synthetik", "index" : "2-2"},
                            {"title": "Socken", "index" : "2-3"}
                        ]},
                    {
                        "title": "Technische Materialen", "index" : "3",
                        "subitems": [
                            {"title": "Verstaerkungmaterialen", "index" : "3-1"},
                            {"title": "Buegelstoffe", "index" : "3-2"}
                        ]},
                    {
                        "title": "Kleinmaterialen", "index" : "4",
                        "subitems": [
                            {"title": "Brandsohlen", "index" : "4-1"},
                            {"title": "Kappen", "index" : "4-2"},
                            {"title": "Senkel", "index" : "4-3"}
                        ]},
                    {
                        "title": "Accessories", "index" : "5",
                        "subitems": [
                            {"title": "Schmuck", "index" : "5-1"},
                            {"title": "Schnallen", "index" : "5-2"},
                            {"title": "Reiseverschluss", "index" : "5-3"}
                        ]},
                    {
                        "title": "Sohlen", "index" : "6",
                        "subitems": [
                            {"title": "Sohlen", "index" : "6-1"},
                            {"title": "Gummi", "index" : "6-2"},
                            {"title": "TR", "index" : "6-3"},
                            {"title": "EVA", "index" : "6-4"}
                        ]},
                    {
                        "title": "Rohstoffe", "index" : "7",
                        "subitems": [

                        ]},
                    {
                        "title": "Verpackung", "index" : "8",
                        "subitems": [

                        ]},
        ]        }

        }
    }
</script>

<style scoped>

</style>