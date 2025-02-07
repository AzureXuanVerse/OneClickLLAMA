## OneClickLLAMA_20250207
- 一键运行 [Qwen2.5](https://github.com/QwenLM/Qwen2.5) [SakuraLLM](https://github.com/SakuraLLM/SakuraLLM)  等本地 LLM 模型
- 可与众多支持 OpenAI 格式的翻译器、分析器应用搭配使用，包括但是不限于：
  - [AiNiee](https://github.com/NEKOparapa/AiNiee)
  - [GalTransl](https://github.com/xd2333/GalTransl)
  - [LinguaGacha](https://github.com/neavo/LinguaGacha)
  - [KeywordGacha](https://github.com/neavo/KeywordGacha)
  - [绿站（轻小说翻译机器人）](https://books.fishhawk.top/workspace/sakura) 等翻译器的服务器端使用
- 配合本页中的各应用的设置指南，可以得到最优化的性能，相较于默认设置可提升 3-5 倍

## 要求
- 至少 8G 显存的独立显卡，NVIDIA 显卡最佳，其他显卡很慢
- 确保安装了 `最新版本` 的显卡驱动程序

## 步骤
- 从 [发布页](https://github.com/neavo/OneClickLLAMA/releases) 下载最新版本的 `OneClickLLAMA` 并解压缩
  - `OneClickLLAMA_NV` 是 NVIDIA 专用的版本
  - `OneClickLLAMA_VULKAN` 是 所有显卡 通用的版本
- 根据用途和显存大小下载适合的模型并放入 `OneClickLLAMA` 文件夹

- 日文翻译到中文
  
| 显存大小         | 模型规模    | 启动脚本          | 下载链接                                                   |
|:---------------:|:-----------:|:----------------:|:---------------------------------------------------------:|
| 8G/10G          | 7B          | 01_1280_NP16.bat | [sakura-7b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-7B-Qwen2.5-v1.0-GGUF/blob/main/sakura-7b-qwen2.5-v1.0-iq4xs.gguf) |
| 11G             | 14B         | 01_1280_NP4.bat  | [sakura-14b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-iq4xs.gguf) |
| 12G             | 14B         | 01_1280_NP6.bat  | [sakura-14b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-iq4xs.gguf) |
| 16G             | 14B         | 01_1280_NP16.bat | [sakura-14b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-iq4xs.gguf) |
| 24G             | 14B         | 01_1280_NP16.bat | [sakura-14b-qwen2.5-v1.0-q6k.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-q6k.gguf) |

- 其他语言翻译到中文

| 显存大小         | 模型规模    | 启动脚本          | 下载链接                                                   |
|:---------------:|:-----------:|:----------------:|:---------------------------------------------------------:|
| 8G/10G          | 7B          | 01_1280_NP16.bat | [Qwen2.5-7B-Instruct-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen2.5-7B-Instruct-GGUF/blob/main/Qwen2.5-7B-Instruct-IQ4_XS.gguf) |
| 11G             | 14B         | 01_1280_NP4.bat  | [Qwen2.5-14B-Instruct-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-GGUF/blob/main/Qwen2.5-14B-Instruct-IQ4_XS.gguf) |
| 12G             | 14B         | 01_1280_NP6.bat  | [Qwen2.5-14B-Instruct-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-GGUF/blob/main/Qwen2.5-14B-Instruct-IQ4_XS.gguf) |
| 16G             | 14B         | 01_1280_NP16.bat | [Qwen2.5-14B-Instruct-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-GGUF/blob/main/Qwen2.5-14B-Instruct-IQ4_XS.gguf) |
| 24G             | 14B         | 01_1280_NP16.bat | [Qwen2.5-14B-Instruct-Q6_K.gguf](https://huggingface.co/bartowski/Qwen2.5-14B-Instruct-GGUF/blob/main/Qwen2.5-14B-Instruct-Q6_K.gguf) |

- 搭配 KeywordGacha 抓取实体词语表

| 显存大小                         | 模型规模    | 启动脚本        | 下载链接                                                   |
|:-------------------------------:|:-----------:|:--------------:|:---------------------------------------------------------:|
| 8G/10G/11G/12G/16G/24G          | 7B          | 01_2k_NP16.bat | [Qwen2.5-7B-Instruct-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen2.5-7B-Instruct-GGUF/blob/main/Qwen2.5-7B-Instruct-IQ4_XS.gguf) |

## 启动
- 现在你的文件结构应该类似于：
```
  OneClickLLAMA\llama\...
                    \00_Core.bat
                    \01_1280_NP16.bat
                    \sakura-14b-qwen2.5-v1.0-iq4xs.gguf
                    \...
```
- 根据 `你的显存和模型的搭配组合` 选择对应的启动脚本，双击启动即可
  
## 设置 AiNiee 
- 确保安装了 `最新版本（版本号 >= 5.2）` 的 [AiNiee](https://github.com/NEKOparapa/AiNiee) 应用
- 启动应用，设置以下选项，其余设置保持默认即可：：
  
| 选项 | 设置 |
|------|:----:|
| 接口管理 - SakuraLLM - 编辑接口 - 接口地址 | http://127.0.0.1:8080 |
| 接口管理 - SakuraLLM - 编辑接口 - 模型名称 | Sakura-v1.0 |
| 项目设置 - 接口名称 | SakuraLLM |
| 基础设置 - 翻译任务切分模式 | Token 模式 |
| 基础设置 - 翻译任务的最大 Tokens 数 | 384 |
| 基础设置 - 每个翻译任务携带的参考上文行数 | 0 |
| 基础设置 - 同时执行的翻译任务数量 | 启动脚本名称中 NP 后的数字 |
| 基础设置 - 翻译流程的最大轮次 | 20 |
| 高级设置 - 保留句内换行符 | 启用 |
| 高级设置 - 保留首尾代码段 | 启用 |

## 设置 GalTransl（TODO）

## 设置 轻小说翻译机器人（绿站）
- 本地翻译
  - 打开 [Sakura 工作区](https://books.fishhawk.top/workspace/sakura) 页面
  - 在左侧 `翻译器` 区域
    - 点击 `添加翻译器`，添加若干个翻译器
    - 翻译器的数量一般应等于 `脚本名称中 NP 后的数字`
    - 翻译器名字随意，链接为 [http://127.0.0.1:8080](http://127.0.0.1:8080)，其他保持默认
  - 在右侧 `本地翻译设置` 区域，将任务均分数设置为翻译器的数量
  - 在右侧 `本地小说` 区域，添加要翻译的日文文本文件
  - 依次点击所有 `翻译器` 后的启动按钮即可开始 `多线程翻译`
  - 翻译完毕后，在右侧 `本地小说` 区域点击 `阅读` 按钮开始阅读
- 在线翻译（8G/10G 配置暂时无法使用在线翻译上传作品）
  - 打开 [Sakura 工作区](https://books.fishhawk.top/workspace/sakura) 页面
    - 在左侧 `翻译器` 区域
    - 点击 `添加翻译器`，添加若干个翻译器
    - 翻译器的数量一般应等于 `脚本名称中 NP 后的数字`
    - 翻译器名字随意，链接为 [http://127.0.0.1:8080](http://127.0.0.1:8080)，其他保持默认
  - 打开你想要翻译的小说页面
    - 在页面中部的 `范围` 区域，将任务均分数设置为翻译器的数量，点击 `排队 Sakura` 按钮
  - 打开 [Sakura 工作区](https://books.fishhawk.top/workspace/sakura) 页面，依次点击所有 `翻译器` 后的启动按钮即可开始 `多线程翻译`

## 常见问题
- 什么是 `爆显存`，会导致什么问题？
  - 系统需求的显存超过了显卡实际的物理显存大小，称之为 `爆显存`
  - `爆显存` 时，翻译的速度和结果都会出现异常，基本丧失可用性，所以要避免这种情况
    
- 如何判断是否 `爆显存`
  - 如果爆的比较厉害，程序会直接报错或者退出
  - 爆了一点又没有完全爆比较难判断
  - 一个可参考的方式是通过第三方软件监测显卡功耗
  - 满载执行任务时，显卡实际功耗应为最大功耗的 `70%-80%` 或者更高
  - 如果显存接近用完，但是显卡实际功耗很低，则大概率是爆显存了

- 如何避免 `爆显存`
  - 在模型启动后，模型占用的显存大小是固定的，不会变化，但是系统中的其他应用也会占用显存
  - 本项目中的脚本都预留了一定的冗余空间，但如果开启过多应用，依然可能导致显存消耗完
  - 所以在使用时，应尽量减少开启其他消耗显存的应用
  - 比如 `浏览器`、`动态壁纸`、`视频播放器` 或 `QQNT`、`VSCODE` 等基于浏览器内核的应用
