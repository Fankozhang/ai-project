# ai-project
## 创建nuxt项目 （pnpm）

```
pnpm create nuxt@latest ai-echarts
```

## NuxtPage 组件（渲染页面）

app.vue组件使用

```
<template>
  <div>
    <NuxtPage />
  </div>
</template>
```

NuxtPage 是 Nuxt 的核心组件，用于渲染基于文件系统的路由。让我简洁地解释它的工作原理。
<NuxtPage /> 是 Nuxt 的路由出口组件。
核心作用：根据当前 URL 渲染 pages/ 目录下对应的 .vue 文件。
pages/
├── index.vue      → /
├── dashboard.vue  → /dashboard
├── about.vue      → /about
└── users/
    └── [id].vue   → /users/123
访问 /dashboard 时，<NuxtPage /> 会把 pages/dashboard.vue 的内容渲染到自己的位置。
本质：它等价于 Vue Router 的 <RouterView />，只是 Nuxt 把路由配置自动化了（基于文件系统约定）。
没有它：pages/ 目录下的文件就是普通文件，路由系统不会生效。

## UI (shadcn-vue) MCP 安装

### vue+shadcn-vue安装：

 [Nuxt - shadcn/vue 组件库](https://vue.shadcn.org.cn/docs/installation/nuxt)

**opencode安装**：查看 E:\ai\ai-project\ai-echarts，我要一个nuxt+shadcn-vue的项目，现在我需要你按照[Nuxt - shadcn/vue 组件库](https://vue.shadcn.org.cn/docs/installation/nuxt)网页文档的内容，按照步骤完成nuxt应用创建安装shadcn-vue和 项目的初始配置

### MCP安装：

[MCP Server - shadcn/vue 组件库](https://vue.shadcn.org.cn/docs/mcp)

cc-switch  加如下配置：

```
{
  "args": [
    "shadcn-vue@latest",
    "mcp"
  ],
  "command": "npx",
  "type": "stdio"
}
```

