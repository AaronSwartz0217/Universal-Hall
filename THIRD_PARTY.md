# 第三方来源与参考声明

本项目在开发过程中参考了以下开源项目与教学资源。所有参考内容仅用于学习算法思路与接口约定，本项目核心代码均为独立实现。

> 注：commit hash 一栏将在实际查阅对应版本时补充，边做边记。

---

## 1. Microsoft DirectX-Graphics-Samples

- **仓库地址**：https://github.com/microsoft/DirectX-Graphics-Samples
- **参考 commit**：`TODO: 查阅时记录`
- **协议**：MSPL（Microsoft Sample Public License）
- **参考内容**：
  - `Samples/Desktop/D3D12HelloTriangle` — 设备初始化、交换链、命令列表、Present 的最小骨架
  - `Samples/Desktop/D3D12HelloTexture` — 上传堆、资源复制、SRV 描述符
  - `Samples/Desktop/D3D12HelloConstBuffers` — CBV、根参数、帧循环 buffer 轮换
  - `Samples/Desktop/D3D12HDR` — HDR 交换链格式、后处理链、tonemap
  - `Samples/Desktop/D3D12Fullscreen` — 全屏四边形后处理 pass
- **使用方式**：仅参考 API 调用顺序与资源布局，代码为自行重写。原始版权声明归 Microsoft Corporation 所有。

---

## 2. NVIDIA Streamline

- **仓库地址**：https://github.com/NVIDIAGameWorks/Streamline
- **参考 commit**：`TODO: 查阅时记录`
- **协议**：框架层开源（详见仓库 LICENSE）；DLSS 二进制（`nvngx_dlss.dll`、`dlssg.dll`）不随仓库分发，需从 NVIDIA 官方渠道获取
- **参考内容**：
  - 官方文档 / programming guide — `sl::init`、`sl::beginFrame/endFrame`、`sl::evaluateFeature` 调用顺序
  - `samples/` 下 D3D12 示例 — 深度、运动向量、无 HUD 色彩缓冲的 tag 绑定、帧索引与 swapchain 配合、缓冲区 unique ID 约定
- **使用方式**：参考接口约定与调用流程，接入代码为自行编写。

---

## 3. LearnOpenGL

- **网站地址**：https://learnopengl.com
- **参考章节**：
  - Advanced OpenGL → Framebuffers
  - Advanced Lighting → Deferred Shading
  - Advanced Lighting → Shadows
  - Advanced Lighting → Cascade Shadow Maps
  - PBR / Lighting Theory
- **协议**：教学内容，CC BY 4.0（详见网站）
- **使用方式**：参考算法思路，HLSL 着色器为自行编写，未直接复制其 GLSL 代码。论文正文中需注明"GBuffer 布局与延迟光照实现参考 LearnOpenGL Deferred Shading 教程（算法移植，着色器为自行编写）"。

---

## 4. 闭源二进制声明

本仓库**不包含**任何 NVIDIA 闭源二进制文件（`nvngx_dlss.dll`、`dlssg.dll` 等）。如需启用 DLSS 功能，请从 NVIDIA 官方开发者渠道或显卡驱动目录获取对应版本的二进制文件，并放置于可执行文件同目录下。
