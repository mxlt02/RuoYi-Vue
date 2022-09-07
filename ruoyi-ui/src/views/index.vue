<template>
  <div class="app-container home">
    <el-row :gutter="20">
      <el-col :sm="24" :lg="24">
        <blockquote class="text-warning" style="font-size: 14px">
          欢迎使用[mxlt]
        </blockquote>

        <hr />
      </el-col>
    </el-row>
    <el-row :gutter="20">
      <el-col :sm="24" :lg="12" style="padding-left: 20px">
        <h2>[mxlt]</h2>
        <p>
          [mxlt]是一款先进的智能平台.
        </p>
        <p>
          <b>当前版本:</b> <span>v{{ version }}</span>
        </p>
        <p>
          <el-tag type="danger">&yen;定制</el-tag>
        </p>
        <p>
          <el-button
            type="primary"
            size="mini"
            icon="el-icon-cloudy"
            plain
            @click="goTarget('https://github.com/mxlt02')"
            >访问Github</el-button
          >
          <el-button
            size="mini"
            icon="el-icon-s-home"
            plain
            @click="goTarget('http://mxlt.top')"
            >访问主页</el-button
          >
        </p>
      </el-col>

      <el-col :sm="24" :lg="12" style="padding-left: 50px">
        <el-row>
          <el-col :span="12">
            <h2>技术选型</h2>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="6">
            <h4>后端技术</h4>
            <ul>
              <li>SpringBoot</li>
              <li>Spring Security</li>
              <li>JWT</li>
              <li>MyBatisPlus</li>
              <li>Druid</li>
              <li>Fastjson</li>
              <li>...</li>
            </ul>
          </el-col>
          <el-col :span="6">
            <h4>前端技术</h4>
            <ul>
              <li>Vue</li>
              <li>Vuex</li>
              <li>Element-ui</li>
              <li>Axios</li>
              <li>Sass</li>
              <li>Quill</li>
              <li>...</li>
            </ul>
          </el-col>
        </el-row>
      </el-col>
    </el-row>
    <el-divider />
    <el-row :gutter="20">
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>联系信息</span>
          </div>
          <div class="body">
            <p>
              <i class="el-icon-s-promotion"></i> 官网：<el-link
                href="http://mxlt.top"
                target="_blank"
                >mxlt.top</el-link
              >
            </p>
            <p>
              <i class="el-icon-chat-dot-round"></i> 微信：<a
                href="javascript:;"
                >mxlt02</a
              >
            </p>
          </div>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="24" :md="12" :lg="8">
        <el-card class="update-log">
          <div slot="header" class="clearfix">
            <span>更新日志</span>
          </div>
          <el-collapse accordion>
            <el-collapse-item title="v3.8.3 - 2022-06-27">
              <ol>
                <li>新增缓存列表菜单功能</li>
                <li>代码生成树表新增(展开/折叠)</li>
                <li>Excel注解支持color字体颜色</li>
                <li>新增Anonymous匿名访问不鉴权注解</li>
                <li>用户头像上传限制只能为图片格式</li>
                <li>接口使用泛型使其看到响应属性字段</li>
                <li>检查定时任务bean所在包名是否为白名单配置</li>
                <li>添加页签openPage支持传递参数</li>
                <li>用户缓存信息添加部门ancestors祖级列表</li>
                <li>升级element-ui到最新版本2.15.8</li>
                <li>升级oshi到最新版本6.1.6</li>
                <li>升级druid到最新版本1.2.11</li>
                <li>升级fastjson到最新版2.0.8</li>
                <li>升级spring-boot到最新版本2.5.14</li>
                <li>降级jsencrypt版本兼容IE浏览器</li>
                <li>删除多余的salt字段</li>
                <li>新增获取不带后缀文件名称方法</li>
                <li>新增获取配置文件中的属性值方法</li>
                <li>新增内容编码/解码方便插件集成使用</li>
                <li>字典类型必须以字母开头，且只能为（小写字母，数字，下滑线）</li>
                <li>优化设置分页参数默认值</li>
                <li>优化对空字符串参数处理的过滤</li>
                <li>优化显示顺序orderNum类型为整型</li>
                <li>优化表单构建按钮不显示正则校验</li>
                <li>优化字典数据回显样式下拉框显示值</li>
                <li>优化R响应成功状态码与全局保持一致</li>
                <li>优化druid开启wall过滤器出现的异常问题</li>
                <li>优化用户管理左侧树型组件增加选中高亮保持</li>
                <li>优化新增用户与角色信息&用户与岗位信息逻辑</li>
                <li>优化默认不启用压缩文件缓存防止node_modules过大</li>
                <li>修复字典数据显示不全问题</li>
                <li>修复操作日志查询类型条件为0时会查到所有数据</li>
                <li>修复Excel注解prompt/combo同时使用不生效问题</li>
                <li>其他细节优化</li>
              </ol>
            </el-collapse-item>
          </el-collapse>
        </el-card>
      </el-col>
<!--      <el-col :xs="24" :sm="24" :md="12" :lg="8">-->
<!--        <el-card class="update-log">-->
<!--          <div slot="header" class="clearfix">-->
<!--            <span>捐赠支持</span>-->
<!--          </div>-->
<!--          <div class="body">-->
<!--            <img-->
<!--              src="https://oscimg.oschina.net/oscnet/up-d6695f82666e5018f715c41cb7ee60d3b73.png"-->
<!--              alt="donate"-->
<!--              width="100%"-->
<!--            />-->
<!--            <span style="display: inline-block; height: 30px; line-height: 30px"-->
<!--              >你可以请作者喝杯咖啡表示鼓励</span-->
<!--            >-->
<!--          </div>-->
<!--        </el-card>-->
<!--      </el-col>-->
    </el-row>
  </div>
</template>

<script>
export default {
  name: "Index",
  data() {
    return {
      // 版本号
      version: "3.8.3",
    };
  },
  methods: {
    goTarget(href) {
      window.open(href, "_blank");
    },
  },
};
</script>

<style scoped lang="scss">
.home {
  blockquote {
    padding: 10px 20px;
    margin: 0 0 20px;
    font-size: 17.5px;
    border-left: 5px solid #eee;
  }
  hr {
    margin-top: 20px;
    margin-bottom: 20px;
    border: 0;
    border-top: 1px solid #eee;
  }
  .col-item {
    margin-bottom: 20px;
  }

  ul {
    padding: 0;
    margin: 0;
  }

  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;

    b {
      font-weight: 700;
    }
  }

  .update-log {
    ol {
      display: block;
      list-style-type: decimal;
      margin-block-start: 1em;
      margin-block-end: 1em;
      margin-inline-start: 0;
      margin-inline-end: 0;
      padding-inline-start: 40px;
    }
  }
}
</style>

