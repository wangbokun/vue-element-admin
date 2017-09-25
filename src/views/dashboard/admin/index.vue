<template>
	<div class="dashboard-editor-container">
     <el-row>
        <el-col :span="8"><div class="grid-content bg-purple"> <bar-chart></bar-chart> </div></el-col>
        <el-col :span="8"><div class="grid-content bg-purple-light"><bar-chart></bar-chart></div></el-col>
        <el-col :span="8"><div class="grid-content bg-purple"><bar-chart></bar-chart></div></el-col>
      </el-row>
	</div>
</template>

<script>
import { mapGetters } from 'vuex'
import countTo from 'vue-count-to'
import panThumb from '@/components/PanThumb'
import pieChart from './pieChart'
import barChart from './barChart'
import lineChart from './lineChart'

export default {
  name: 'dashboard-admin',
  components: { countTo, panThumb, pieChart, lineChart, barChart },
  data() {
    return {
      statisticsData: {
        article_count: 1024,
        pageviews_count: 1024
      }
    }
  },
  computed: {
    ...mapGetters([
      'name',
      'avatar',
      'roles'
    ])
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.dashboard-editor-container {
    margin: 30px;
    .btn-group {
        margin-bottom: 60px;
    }
    .box-card-header {
        position: relative;
        height: 160px;
    }
    .panThumb {
        z-index: 100;
        height: 150px;
        width: 150px;
        position: absolute;
        left: 0px;
        right: 0px;
        margin: auto;
    }
    .display_name{
        font-size: 30px;
        display: block;
    }
    .info-item{
        display: inline-block;
        margin-top: 10px;
        font-size: 14px;
        &:last-of-type{
            margin-left: 15px;
        }
    }
}
</style>
