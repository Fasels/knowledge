# 快速开始

1.创建项目命令

```
npm create electron-vite@latest
```

2.设置下载源

```
# 更换淘宝镜像
npm config set registry https://registry.npmmirror.com
# 临时设置electron的二进制下载镜像
$env:ELECTRON_MIRROR = "https://npmmirror.com/mirrors/electron/"
npm install
```

3.项目开始

```
npm run dev
```

# 项目简介

```
my-app/
├─ dist-electron/ # 进行npm run dev后，编译后的electron文件
|  ├─ main.js
│  ├─ preload.js	
|
├─ electron/           # 👈 Electron 主进程（Main Process）代码
│  ├─ main.ts
│  ├─ preload.ts
│  ├─ index.html
│  └─ vite.config.ts   # 针对主进程和预加载脚本的Vite配置
│
├─ public/             # 存放资源的地方
|
├─ src/                # 👈 React 前端（Renderer Process）代码
│  ├─ App.tsx
│  ├─ main.tsx
│  ├─ assets/
│  └─ vite-env.d.ts
│
├─ out/                # 打包产物目录（运行打包命令后出现）
│
├─ electron-builder.json5 # 打包配置文件
├─ package.json
├─ electron.vite.config.ts  # Electron 主体构建配置文件（关键）
├─ tsconfig.json
└─ README.md
```

