<template>
  <div class="container">
    <h1>Custom theme example (on demand)</h1>

    <el-row>
      <el-button @click="onClick">Default</el-button>
      <el-button @click="onClick" type="primary">Primary</el-button>
      <el-button @click="onClick" type="success">Success</el-button>
      <el-button @click="onClick" type="info">Info</el-button>
      <el-button @click="onClick" type="warning">Warning</el-button>
      <el-button @click="onClick" type="danger">Danger</el-button>
    </el-row>

    <el-radio-group v-model="radioVal">
      <el-radio-button label="New York"></el-radio-button>
      <el-radio-button label="Washington"></el-radio-button>
      <el-radio-button label="Los Angeles"></el-radio-button>
      <el-radio-button label="Chicago"></el-radio-button>
    </el-radio-group>

    <div>
      <el-switch v-model="switchVal"></el-switch>&nbsp;
      <el-switch
        v-model="switchVal"
        active-color="#13ce66"
        inactive-color="#ff4949"
      />
    </div>

    <div>
      <el-select>
        <el-option>test</el-option>
      </el-select>
      &nbsp;
      <el-date-picker></el-date-picker>
    </div>

    <el-slider v-model="sliderVal"></el-slider>

    <p>
      It is a example built by vite.&nbsp; More info see
      <a
        href="https://github.com/element-plus/unplugin-element-plus"
        target="_blank"
        >unplugin-element-plus</a
      >.
    </p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import {
  ElButton,
  ElSwitch,
  ElNotification,
  ElSelect,
  ElRadioGroup,
  ElRadioButton,
  ElSlider,
  ElDatePicker
} from 'element-plus'

const radioVal = ref('New York')
const switchVal = ref(true)
const sliderVal = ref(50)

function onClick() {
  ElNotification({
    type: 'success',
    title: '已成功发送邮件',
    message: '验证码区分大小写，有效期5分钟',
    duration: 3000
  })
}
</script>
