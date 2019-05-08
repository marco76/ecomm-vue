<template>
<el-container style="height: 500px; border: 1px solid #eee">
  <el-header>
    <LayoutHeader></LayoutHeader>
  </el-header>
  <el-container>
    <LayoutLeftMenu></LayoutLeftMenu>
    <el-main>
      aaa
      <ProductCard></ProductCard>
      <!--
      <el-table :data="tableData">
        <el-table-column prop="date" label="Date" width="140">
        </el-table-column>
        <el-table-column prop="name" label="Name" width="120">
        </el-table-column>
        <el-table-column prop="address" label="Address">
        </el-table-column>
      </el-table>-->
    </el-main>
  </el-container>
  </el-container>

</template>

<style>

</style>

<script>
  import ProductCard from "./product/ProductCard";
  import LayoutLeftMenu from "./layout/LayoutLeftMenu";
  import LayoutHeader from "./layout/LayoutHeader";
  export default {
    components: {LayoutHeader, LayoutLeftMenu, ProductCard},
    data() {
      const item = {
        date: '2016-05-02',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles'
      };
      return {
        tableData: Array(20).fill(item)
      }
    }
  };
</script>