# 大肥鱼 · Dafeiyu Pet

圆润可爱的蓝色鲸鱼娘宠物，包含九种动作和十六方向注视。本仓库发布的是全部验收通过后的最终优化版本；失败动作采用 v41，其余动作和注视保留最终验收画面。

[下载最新发行版](https://github.com/yang159052/dafeiyu-pet/releases/latest) · [在 ChatGPT 中领养](https://chatgpt.com/s/sharepet_6ac64314feb881918957b50e4f709046)

<img src="preview/all-actions-long-loop.gif" width="192" height="234" alt="大肥鱼九动作完整循环预览">

## 使用方式一：在 ChatGPT 中领养

1. 打开[大肥鱼分享链接](https://chatgpt.com/s/sharepet_6ac64314feb881918957b50e4f709046)，登录自己的 ChatGPT 账户。
2. 按页面提示领养，将它加入自己的宠物库。
3. 在支持 Pets 的 ChatGPT Work 界面选择「大肥鱼」启用。

领养链接直接使用已经创建的宠物；不需要下载或安装本仓库的 ZIP 文件。

## 使用方式二：安装到 Codex 桌面版

适用于支持本地自定义 v2 宠物的 Codex 桌面版。发行包按已验证的本地宠物清单结构制作，不需要 Python、Node.js 或额外插件。

1. 在 [Releases](https://github.com/yang159052/dafeiyu-pet/releases/latest) 下载 `dafeiyu-v1.0.0.zip`。
2. 解压，得到 `dafeiyu` 文件夹。其核心文件是 `pet.json` 和 `spritesheet.webp`。
3. 将整个 `dafeiyu` 文件夹复制到 Codex 的 `pets` 目录。Windows 默认位置是 `%USERPROFILE%\.codex\pets\`。
4. 重新打开 Codex，在宠物选择界面选择「大肥鱼」。

安装后的结构应为：

```text
%USERPROFILE%\.codex\pets\
└── dafeiyu\
    ├── pet.json
    ├── spritesheet.webp
    └── README.md
```

不要额外嵌套一层 `dafeiyu` 文件夹。如果自定义了 `CODEX_HOME`，安装位置改为该目录下的 `pets/dafeiyu`。

也可以克隆本仓库，将根目录的 `pet.json` 和 `spritesheet.webp` 一起复制到 `pets/dafeiyu`，再启用宠物。

## 查看动画

完整循环依次展示：待机 → 等待 → 向左跑 → 向右跑 → 挥手 → 跳跃 → 思考／工作 → 检查 → 失败。

| 动作 | 帧数 | 预览 |
| --- | ---: | --- |
| 待机 | 6 | <img src="preview/idle.gif" width="192" height="234" alt="待机"> |
| 向右跑 | 8 | <img src="preview/running-right.gif" width="192" height="234" alt="向右跑"> |
| 向左跑 | 8 | <img src="preview/running-left.gif" width="192" height="234" alt="向左跑"> |
| 挥手 | 4 | <img src="preview/waving.gif" width="192" height="234" alt="挥手"> |
| 跳跃 | 5 | <img src="preview/jumping.gif" width="192" height="234" alt="跳跃"> |
| 失败 | 8 | <img src="preview/failed.gif" width="192" height="234" alt="失败"> |
| 等待 | 6 | <img src="preview/waiting.gif" width="192" height="234" alt="等待"> |
| 思考／工作 | 6 | <img src="preview/running.gif" width="192" height="234" alt="思考与工作"> |
| 检查 | 6 | <img src="preview/review.gif" width="192" height="234" alt="检查"> |

失败预览按原动作从微笑过渡到低头失落，播放一次后停在末帧；重新加载图片即可重播。其他动作循环播放。

### 十六方向注视

<img src="preview/look-around.gif" width="192" height="234" alt="十六方向注视循环">

[查看全部方向静态帧](preview/look-directions.png)。方向按屏幕坐标顺时针排列：0° 向上、90° 向右、180° 向下、270° 向左，相邻方向相差 22.5°。

需要离线查看时，下载 `dafeiyu-preview-v1.0.0.zip`，解压后用浏览器打开其中的 `index.html`。GitHub 文件页只显示 HTML 源码。

## 资源格式

| 项目 | 值 |
| --- | --- |
| 清单 | `pet.json` |
| 图集 | `spritesheet.webp`，透明 RGBA、无损 WebP |
| 图集版本 | `spriteVersionNumber: 2` |
| 图集大小 | 1536 × 2288 像素 |
| 单帧大小 | 192 × 208 像素 |
| 排列 | 8 列 × 11 行 |
| 使用帧数 | 九动作 57 帧 + 注视 16 帧 = 73 帧 |
| 空白格 | 15 格，完全透明 |

清单与图集须放在同一目录。不要缩放、重新裁切或转换图集，否则可能导致动作错位、尺寸跳动或透明边缘变化。GIF 用于预览，运行时使用 WebP 图集。预览 GIF 上方的文字标签不属于角色画面。

## 分享

可以直接分享本仓库、[最新发行版页面](https://github.com/yang159052/dafeiyu-pet/releases/latest)，或 [ChatGPT 领养链接](https://chatgpt.com/s/sharepet_6ac64314feb881918957b50e4f709046)。

形象参考：[大肥鱼／DeepSeek 鲸鱼娘](https://treapgogo.github.io/deepseek-whale-girl/index.html)。
