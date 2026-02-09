<script setup>
import { ref } from 'vue'

// 个人信息
const profile = ref({
  name: '苏格',
  title: '全栈开发者 / 技术创作者 / 开源爱好者',
  bio: '专注于构建优雅高效的解决方案，热爱探索前沿技术。擅长 Vue、React、Node.js 等技术栈。',
  avatar: 'https://api.dicebear.com/7.x/avataaars/svg?seed=Suge'
})

// 社交媒体链接
const socialLinks = ref([
  { name: 'GitHub', icon: 'M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z', url: 'https://github.com/suge' },
  { name: 'Twitter', icon: 'M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z', url: 'https://twitter.com/suge' },
  { name: 'Email', icon: 'M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z', url: 'mailto:contact@suge.dev' },
  { name: 'LinkedIn', icon: 'M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z', url: 'https://linkedin.com/in/suge' }
])

// 个人工具/项目
const projects = ref([
  {
    name: 'DevFlow CLI',
    description: '一个强大的开发者命令行工具，提升开发效率，支持自动化部署和代码生成。',
    tags: ['CLI', 'Node.js', 'TypeScript'],
    icon: '⚡',
    gradient: 'from-yellow-500 to-orange-500',
    url: '#'
  },
  {
    name: 'CodeSnippets',
    description: '在线代码片段管理工具，支持语法高亮、分类管理和快速分享。',
    tags: ['Vue', 'Firebase', 'Tailwind'],
    icon: '💻',
    gradient: 'from-blue-500 to-cyan-500',
    url: '#'
  },
  {
    name: 'TaskMaster',
    description: '轻量级任务管理应用，采用番茄工作法，帮助开发者提升专注力。',
    tags: ['React', 'Redux', 'PWA'],
    icon: '✅',
    gradient: 'from-green-500 to-emerald-500',
    url: '#'
  },
  {
    name: 'API Dashboard',
    description: '优雅的 API 监控仪表板，实时追踪接口性能、错误率和响应时间。',
    tags: ['Vue', 'ECharts', 'WebSocket'],
    icon: '📊',
    gradient: 'from-purple-500 to-pink-500',
    url: '#'
  },
  {
    name: 'GitHelper',
    description: 'Git 工作流辅助工具，自动化处理分支管理、代码审查和发布流程。',
    tags: ['Go', 'Git', 'CI/CD'],
    icon: '🔧',
    gradient: 'from-red-500 to-rose-500',
    url: '#'
  },
  {
    name: 'Markdown Pro',
    description: '增强版 Markdown 编辑器，支持实时预览、导出多格式和云同步。',
    tags: ['Electron', 'Vue', 'Cloud'],
    icon: '📝',
    gradient: 'from-indigo-500 to-violet-500',
    url: '#'
  }
])

// 背景粒子数
const particles = Array.from({ length: 50 }, (_, i) => ({
  id: i,
  size: Math.random() * 3 + 1,
  x: Math.random() * 100,
  y: Math.random() * 100,
  duration: Math.random() * 3 + 2
}))
</script>

<template>
  <div class="min-h-screen relative overflow-hidden">
    <!-- 背景网格 -->
    <div class="absolute inset-0 bg-grid-pattern opacity-20"></div>

    <!-- 背景粒子 -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div
        v-for="particle in particles"
        :key="particle.id"
        class="absolute rounded-full bg-primary/20 animate-float"
        :style="{
          width: `${particle.size}px`,
          height: `${particle.size}px`,
          left: `${particle.x}%`,
          top: `${particle.y}%`,
          animationDuration: `${particle.duration}s`,
          animationDelay: `${particle.id * 0.1}s`
        }"
      ></div>
    </div>

    <!-- 主内容 -->
    <div class="relative z-10">
      <!-- 导航栏 -->
      <nav class="fixed top-0 left-0 right-0 z-50 backdrop-blur-md bg-darker/50 border-b border-white/5">
        <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
          <div class="text-xl font-bold text-gradient">SU.DEV</div>
          <div class="flex gap-6 text-sm">
            <a href="#about" class="text-gray-400 hover:text-primary transition-colors">关于</a>
            <a href="#projects" class="text-gray-400 hover:text-primary transition-colors">项目</a>
            <a href="#contact" class="text-gray-400 hover:text-primary transition-colors">联系</a>
          </div>
        </div>
      </nav>

      <!-- Hero Section -->
      <section id="about" class="min-h-screen flex items-center justify-center px-6 pt-20">
        <div class="max-w-4xl mx-auto text-center">
          <!-- 头像 -->
          <div class="relative inline-block mb-8">
            <div class="w-32 h-32 rounded-full bg-gradient-to-br from-primary to-secondary p-1 animate-glow">
              <img
                :src="profile.avatar"
                :alt="profile.name"
                class="w-full h-full rounded-full bg-darker object-cover"
              />
            </div>
            <div class="absolute -bottom-2 -right-2 bg-darker rounded-full px-3 py-1 text-xs border border-primary/50">
              Available for hire
            </div>
          </div>

          <!-- 名字和标题 -->
          <h1 class="text-5xl md:text-7xl font-bold mb-4">
            <span class="text-gradient">Hi, I'm {{ profile.name }}</span>
          </h1>
          <p class="text-xl md:text-2xl text-gray-400 mb-6">{{ profile.title }}</p>

          <!-- 简介 -->
          <p class="text-gray-300 max-w-2xl mx-auto mb-12 leading-relaxed">
            {{ profile.bio }}
          </p>

          <!-- 社交链接 -->
          <div class="flex justify-center gap-4">
            <a
              v-for="social in socialLinks"
              :key="social.name"
              :href="social.url"
              target="_blank"
              class="group relative p-4 bg-dark/50 backdrop-blur-sm rounded-xl tech-border card-glow hover:scale-110 transition-all duration-300"
            >
              <svg class="w-6 h-6 text-gray-400 group-hover:text-primary transition-colors" viewBox="0 0 24 24" fill="currentColor">
                <path :d="social.icon" />
              </svg>
              <span class="absolute -bottom-10 left-1/2 -translate-x-1/2 text-sm text-gray-400 opacity-0 group-hover:opacity-100 transition-opacity whitespace-nowrap">
                {{ social.name }}
              </span>
            </a>
          </div>
        </div>
      </section>

      <!-- 项目展示区 -->
      <section id="projects" class="py-32 px-6">
        <div class="max-w-6xl mx-auto">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold mb-4">
              <span class="text-gradient">My Projects</span>
            </h2>
            <p class="text-gray-400 text-lg">我精心打造的工具和应用</p>
          </div>

          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div
              v-for="project in projects"
              :key="project.name"
              class="group bg-dark/30 backdrop-blur-sm rounded-2xl p-6 tech-border card-glow hover:bg-dark/50 transition-all duration-300 cursor-pointer"
              @click="window.location.href = project.url"
            >
              <!-- 图标 -->
              <div class="text-4xl mb-4">{{ project.icon }}</div>

              <!-- 标题 -->
              <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">
                {{ project.name }}
              </h3>

              <!-- 描述 -->
              <p class="text-gray-400 text-sm mb-4 leading-relaxed">
                {{ project.description }}
              </p>

              <!-- 标签 -->
              <div class="flex flex-wrap gap-2">
                <span
                  v-for="tag in project.tags"
                  :key="tag"
                  class="px-3 py-1 text-xs rounded-full bg-gradient-to-r from-white/10 to-white/5 border border-white/10"
                >
                  {{ tag }}
                </span>
              </div>

              <!-- 装饰光效 -->
              <div class="absolute top-0 right-0 w-20 h-20 bg-gradient-to-br opacity-0 group-hover:opacity-10 transition-opacity duration-300 rounded-bl-full" :class="project.gradient"></div>
            </div>
          </div>
        </div>
      </section>

      <!-- 联系区域 -->
      <section id="contact" class="py-32 px-6">
        <div class="max-w-4xl mx-auto text-center">
          <h2 class="text-4xl md:text-5xl font-bold mb-4">
            <span class="text-gradient">Let's Connect</span>
          </h2>
          <p class="text-gray-400 text-lg mb-12">
            对我的项目感兴趣？欢迎与我交流合作
          </p>
          <a
            href="mailto:contact@suge.dev"
            class="inline-flex items-center gap-2 px-8 py-4 bg-gradient-to-r from-primary to-secondary rounded-full font-semibold hover:scale-105 transition-transform duration-300 hover:shadow-lg hover:shadow-primary/25"
          >
            <svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor">
              <path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
            </svg>
            Get in Touch
          </a>
        </div>
      </section>

      <!-- 页脚 -->
      <footer class="py-8 px-6 border-t border-white/5">
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
          <div class="text-gray-500 text-sm">
            © 2024 {{ profile.name }}. All rights reserved.
          </div>
          <div class="flex gap-6 text-sm text-gray-500">
            <span>Built with Vue + Tailwind</span>
            <span>Hosted on Cloudflare Pages</span>
          </div>
        </div>
      </footer>
    </div>

    <!-- 滚动指示器 -->
    <div class="fixed bottom-8 left-1/2 -translate-x-1/2 animate-bounce">
      <svg class="w-6 h-6 text-gray-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <path d="M12 5v14M19 12l-7 7-7-7"/>
      </svg>
    </div>
  </div>
</template>

<style scoped>
.bg-grid-pattern {
  background-image:
    linear-gradient(to right, rgba(255,255,255,0.03) 1px, transparent 1px),
    linear-gradient(to bottom, rgba(255,255,255,0.03) 1px, transparent 1px);
  background-size: 50px 50px;
}

/* 自定义滚动条 */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #050508;
}

::-webkit-scrollbar-thumb {
  background: #00f0ff30;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #00f0ff50;
}
</style>
