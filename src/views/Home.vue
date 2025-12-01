<template>
  <div class="home-container">
    <el-container>
      <el-header class="header">
        <div class="header-content">
          <h1 class="logo">Metaprise</h1>
          <el-menu
            mode="horizontal"
            :default-active="activeIndex"
            class="header-menu"
          >
            <el-menu-item index="1">首页</el-menu-item>
            <el-menu-item index="2">产品</el-menu-item>
            <el-menu-item index="3">服务</el-menu-item>
            <el-menu-item index="4">关于我们</el-menu-item>
          </el-menu>
        </div>
      </el-header>
      <el-main class="main-content">
        <div class="welcome-section">
          <el-card class="welcome-card">
            <template #header>
              <div class="card-header">
                <span>欢迎使用 White Label 产品</span>
              </div>
            </template>
            <div class="card-content">
              <p>这是一个基于 Vue3 + Element Plus 构建的白标产品平台</p>
              <el-divider />
              <div class="feature-grid">
                <el-card shadow="hover" class="feature-card">
                  <el-icon :size="40" class="feature-icon"><Setting /></el-icon>
                  <h3>易于配置</h3>
                  <p>灵活的配置选项，快速定制您的品牌</p>
                </el-card>
                <el-card shadow="hover" class="feature-card">
                  <el-icon :size="40" class="feature-icon"><DataAnalysis /></el-icon>
                  <h3>数据分析</h3>
                  <p>强大的数据分析功能，洞察业务趋势</p>
                </el-card>
                <el-card shadow="hover" class="feature-card">
                  <el-icon :size="40" class="feature-icon"><User /></el-icon>
                  <h3>用户管理</h3>
                  <p>完善的用户管理系统，保障数据安全</p>
                </el-card>
                <el-card shadow="hover" class="feature-card">
                  <el-icon :size="40" class="feature-icon"><Document /></el-icon>
                  <h3>文档中心</h3>
                  <p>详细的文档说明，快速上手使用</p>
                </el-card>
              </div>
            </div>
          </el-card>
        </div>
      </el-main>
      <el-footer class="footer">
        <div class="footer-content">
          <p>&copy; 2024 Metaprise. All rights reserved.</p>
        </div>
      </el-footer>
    </el-container>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { Setting, DataAnalysis, User, Document } from '@element-plus/icons-vue'

const activeIndex = ref('1')
</script>

<style scoped>
.home-container {
  width: 100%;
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.header {
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
  padding: 0;
  height: 70px;
  display: flex;
  align-items: center;
}

.header-content {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
}

.logo {
  font-size: 24px;
  font-weight: bold;
  color: #667eea;
  margin: 0;
}

.header-menu {
  border-bottom: none;
}

.main-content {
  padding: 40px 20px;
  min-height: calc(100vh - 140px);
}

.welcome-section {
  max-width: 1200px;
  margin: 0 auto;
}

.welcome-card {
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.card-header {
  font-size: 20px;
  font-weight: 600;
  color: #333;
}

.card-content {
  padding: 20px 0;
}

.card-content p {
  font-size: 16px;
  color: #666;
  margin-bottom: 20px;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.feature-card {
  text-align: center;
  padding: 30px 20px;
  transition: transform 0.3s ease;
  border-radius: 8px;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-icon {
  color: #667eea;
  margin-bottom: 15px;
}

.feature-card h3 {
  font-size: 18px;
  margin: 15px 0 10px;
  color: #333;
}

.feature-card p {
  font-size: 14px;
  color: #666;
  line-height: 1.6;
}

.footer {
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.footer-content {
  text-align: center;
}

.footer-content p {
  color: #666;
  font-size: 14px;
}
</style>
