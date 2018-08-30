<template>
  <div class="hello">
    <el-container>
  <el-header>
     <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="1">
          <img src="../assets/element.png" alt="tupian"/>
      </el-menu-item>
      <el-menu-item index="1">
        <el-input v-model="input" placeholder="请输入内容"></el-input>
      </el-menu-item>
      <el-menu-item index="2">
        <el-tabs v-model="activeName" @tab-click="handleClick">
        <el-tab-pane label="指南" name="first"></el-tab-pane>
        <el-tab-pane label="组件" name="second"></el-tab-pane>
        <el-tab-pane label="资源" name="third"></el-tab-pane>
      </el-tabs>
      </el-menu-item>
      <el-submenu index="3">
        <template slot="title">2.4.5</template>
        <el-menu-item index="2-1">1.4.13</el-menu-item>
        <el-menu-item index="2-2">2.0.11</el-menu-item>
        <el-menu-item index="2-3">2.1.0</el-menu-item>
        <el-menu-item index="2-1">2.2.2</el-menu-item>
        <el-menu-item index="2-2">2.3.9</el-menu-item>
        <el-menu-item index="2-3">2.4.5</el-menu-item>
      </el-submenu>
      <el-submenu index="4">
        <template slot="title">中文</template>
        <el-menu-item index="2-1">中文</el-menu-item>
        <el-menu-item index="2-2">English</el-menu-item>
        <el-menu-item index="2-3">Español</el-menu-item>
      </el-submenu>
      <el-menu-item index="5"> <el-color-picker v-model="color1"></el-color-picker></el-menu-item>
    </el-menu>
  </el-header>
  <el-container>
    <el-aside width="200px">
      <ul class="list">
        <li>
           <img src="../assets/logo.png" alt="tupian"/>
        </li>
        <li>
          <h4>更新日志</h4>
        </li>
        <li>Element React</li>
        <li>Element Angular</li>
        <li>
          <h4>开发指南</h4>
        </li>
        <li>安装</li>
        <li>快速上手</li>
        <li>国际化</li>
        <li>自定义主题</li>
        <li>内置过渡动画</li>
        <li>
          <h4>组件</h4>
        </li>
        <li>Basic</li>
        <li>Form表单</li>
        <li>Data数据</li>
        <li>Notice通知</li>
        <li>Navigation导航</li>
        <li>Others其他</li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </el-aside>
    <el-main>
      <el-row>
        <el-col :span="24">
            <h1 class="main-title">更新日志</h1>
          <el-button>GitHub Releases</el-button>
          </el-col>
      </el-row>
            <el-form ref="form" :model="form" label-width="80px">
        <el-form-item label="活动名称">
          <el-input v-model="form.name"></el-input>
        </el-form-item>
        <el-form-item label="活动区域">
          <el-select v-model="form.region" placeholder="请选择活动区域">
            <el-option label="区域一" value="shanghai"></el-option>
            <el-option label="区域二" value="beijing"></el-option>
          </el-select>
        </el-form-item>
        <el-form-item label="活动时间">
          <el-col :span="11">
            <el-date-picker type="date" placeholder="选择日期" v-model="form.date1" style="width: 100%;"></el-date-picker>
          </el-col>
          <el-col class="line" :span="2">-</el-col>
          <el-col :span="11">
            <el-time-picker type="fixed-time" placeholder="选择时间" v-model="form.date2" style="width: 100%;"></el-time-picker>
          </el-col>
        </el-form-item>
        <el-form-item label="即时配送">
          <el-switch v-model="form.delivery"></el-switch>
        </el-form-item>
        <el-form-item label="活动性质">
          <el-checkbox-group v-model="form.type">
            <el-checkbox label="美食/餐厅线上活动" name="type"></el-checkbox>
            <el-checkbox label="地推活动" name="type"></el-checkbox>
            <el-checkbox label="线下主题活动" name="type"></el-checkbox>
            <el-checkbox label="单纯品牌曝光" name="type"></el-checkbox>
          </el-checkbox-group>
        </el-form-item>
        <el-form-item label="特殊资源">
          <el-radio-group v-model="form.resource">
            <el-radio label="线上品牌商赞助"></el-radio>
            <el-radio label="线下场地免费"></el-radio>
          </el-radio-group>
        </el-form-item>
        <el-form-item label="活动形式">
          <el-input type="textarea" v-model="form.desc"></el-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="onSubmit">立即创建</el-button>
          <el-button>取消</el-button>
        </el-form-item>
      </el-form>
</el-main>
  </el-container>
</el-container>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
        input:'',
        color1: '#409EFF',
        activeIndex: '1',
        activeName: 'second',
        form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
      }
    }
  },
  methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      },
       handleClick(tab, event) {
        console.log(tab, event);
      },   
      onSubmit() {
        console.log('submit!');
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#app.el-menu--horizontal {
    border-right: none;
}
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
}
li {
  display: block;
  margin:0;
}
a {
  color: #42b983;
}
.hello{
  overflow-y: hidden;
}
.list li{
  text-align: left;
}
 .main-title{
   display: inline-block;
   float: left;
   } 
</style>
