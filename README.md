# 环境
|库|版本|
|--|--|
|node.js|16.20.2|

# 安装依赖
```
npm_config_arch=x64 npm install
```
## 报错
建议更换源:
```
npm config set electron_mirror https://npmmirror.com/mirrors/electron/
```
然后再执行上述命令

# 运行
```
npm start
```


# 说明
fork from [mac-roco-client](https://github.com/wlz196/mac-roco-client)

# 洛克王国微端 for macOS

---

## 功能特性
- 一键启动洛克王国网页版
- 自动适配 Flash 插件路径（开发/打包环境）
- 支持打包为 macOS 应用（.app/.dmg）
- 禁止网页滚动，体验更接近原生客户端

---

## 环境要求
- macOS 系统（Intel 或 Apple Silicon 芯片均可，作者实测 M4 芯片可用）
- Node.js 与 npm（仅开发或源码运行时需要，直接安装应用无需）

---

## 安装与运行

### 方式一：直接下载安装包
1. **下载项目中的 `.dmg` 安装包**  
   - 在 [Releases](#) 或项目发布页面下载最新的 `.dmg` 文件。
2. **安装应用**  
   - 双击 `.dmg` 文件，按提示将应用拖入"应用程序"文件夹。
3. **运行应用**  
   - 在“应用程序”中找到“洛克王国微端”，双击即可运行。
   - 如为 M 系列芯片，首次运行会提示安装 Rosetta，按提示安装即可。
   - 若出现“无法验证开发者”提示，请在“系统设置-隐私与安全性”中最下方选择“仍要打开”或“允许”。

---

### 方式二：源码运行（开发者模式）
1. **克隆项目**
   ```bash
   git clone <本项目地址>
   cd mac-roco-client
   ```
2. **安装依赖**
   ```bash
   npm_config_arch=x64 npm install
   ```
3. **开发模式运行**
   ```bash
   npm start
   ```

---

## 打包发布

1. **配置 package.json**
   - 已内置 electron-builder 配置，无需额外修改。
2. **打包为 macOS 安装包（仅 Intel 架构）**
   ```bash
   npm run dist -- --mac --x64
   ```
3. **打包结果**
   - 在 `dist/` 目录下生成 `.dmg` 安装包和 `.app` 文件。

---

## 常见问题

### 1. 运行提示“无法验证开发者”？
- 在“系统设置-隐私与安全性”中最下方选择“仍要打开”或“允许”。

### 2. M 系列芯片提示需要 Rosetta？
- 按提示安装 Rosetta 即可，安装后可正常运行。

