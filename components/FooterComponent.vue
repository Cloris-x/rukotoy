<template>
  <div class="footer">
    <el-row class="footer-logo">
      <img src="~/static/images/icon/footer-logo.png" alt="footer-logo" />
    </el-row>
    <el-row :gutter="10" class="footer-detail" style="margin: auto">
      <el-col :span="6">
        <p class="footer-title">联系我们</p>
        <p class="footer-content">
          深圳市龙岗区坂田街道马安堂社区布龙路573号儒峰大厦1701
        </p>
        <p class="footer-content">联系方式: 0755-83126255</p>
        <p class="footer-content">工作时间：9:00-18:30</p>
      </el-col>
      <el-col :span="3">
        <p class="footer-title">探索精彩</p>
        <p class="footer-content">
          <a href="https://share.rukotoy.com/" target="_blank">乐于分享</a>
        </p>
        <p class="footer-content">Ruko社区</p>
        <p class="footer-content">公司介绍</p>
      </el-col>
      <el-col :span="6">
        <p class="footer-title">服务支持</p>
        <p class="footer-content">
          中文官网：<a href="https://www.ruko.cn" target="_blank"
            >https://www.ruko.cn</a
          >
        </p>
        <p class="footer-content">
          全球官网：<a href="https://www.rukotoy.com" target="_blank"
            >https://www.rukotoy.com</a
          >
        </p>
        <p class="footer-content">
          海外购买：
          <a href="https://www.ruko.net" target="_blank"
            >https://www.ruko.net</a
          >
        </p>
      </el-col>
      <el-col :span="9">
        <p class="footer-title">与我们联系第一时间获得瑞可的最新动态</p>
        <el-form
          :model="emailForm"
          ref="emailValidateForm"
          label-width="100px"
          class="demo-dynamic"
        >
          <el-form-item
            prop="email"
            label-width="0"
            :rules="[
              { required: true, message: '请输入邮箱地址', trigger: 'blur' },
              {
                type: 'email',
                message: '请输入正确的邮箱地址',
                trigger: ['blur', 'change'],
              },
            ]"
          >
            <el-input
              type="email"
              placeholder="邮箱"
              v-model="emailForm.email"
            ></el-input>
          </el-form-item>
          <el-form-item prop="info" label-width="0">
            <el-input
              type="textarea"
              :rows="4"
              v-model="emailForm.info"
            ></el-input>
          </el-form-item>
          <el-form-item>
            <el-button
              type="primary"
              @click="submitForm('emailValidateForm')"
              class="submit"
              >提交</el-button
            >
          </el-form-item>
        </el-form>
      </el-col>
    </el-row>
    <el-row class="footer-detail footer-bottom">
      <p class="footer-content">
        Copy Right&nbsp;©&nbsp;2024&nbsp;瑞可创新&nbsp;版权所有
      </p>
    </el-row>
  </div>
</template>

<script>
import { Col, Row, Form, FormItem, Input, Button } from "element-ui";

export default {
  name: "FooterComponent.vue",
  data() {
    return {
      emailForm: {
        email: "",
        info: "",
      },
      rules: {
        info: [{ required: true, message: "请填写邮箱内容", trigger: "blur" }],
      },
    };
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate((valid) => {
        if (valid) {
          alert("submit!");
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
  },
};
</script>

<style scoped>
.footer {
  background: linear-gradient(to right, #104d8b, #028eed);
  color: #fff;
}

.footer-logo {
  padding: 30px 0;
  text-align: center;
}

.footer-detail {
  width: 66.67%;
  margin: 0 auto;
}

.footer-title {
  font-size: 0.9rem;
}

.footer-content {
  font-size: 0.75rem;
  margin-bottom: 40px;
}

.footer-bottom {
  border-top: #ebebeb 1px solid;
  margin-top: 10px;
}

.submit {
  float: right;
  color: #000;
  background-color: #fff9f9;
  width: 4.25rem;
  font-size: 0.75rem;
  border-radius: 5px;
  border: none;
}

a:link {
  color: #fff;
  padding: 0;
}

a:visited {
  color: #fff;
  padding: 0;
}

a:hover {
  color: #fff;
  padding: 0;
}

a:active {
  color: #fff;
  padding: 0;
}
</style>
