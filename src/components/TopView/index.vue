<template>
  <div>
    <el-row :gutter="20">
      <el-col :span="6">
        <el-card shadow="hover">
          <total-sales />
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card shadow="hover">
          <total-orders />
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card shadow="hover">
          <today-user />
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card shadow="hover">
          <total-users />
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import TotalSales from '@/components/TotalSales'
import TotalOrders from '@/components/TotalOrders'
import TodayUser from '@/components/TodayUser'
import TotalUsers from '@/components/TotalUsers'
export default {
  components: {
    TotalSales,
    TotalOrders,
    TodayUser,
    TotalUsers
  }
}
</script>

<style></style>
