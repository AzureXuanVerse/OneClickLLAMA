## OneClickLLAMA
- 一键运行 [Qwen2.5](https://github.com/QwenLM/Qwen2.5) [SakuraLLM](https://github.com/SakuraLLM/SakuraLLM)  等本地 LLM 模型
- 可与众多支持 OpenAI 格式的翻译器、分析器应用搭配使用，包括但是不限于：
  - [LinguaGacha](https://github.com/neavo/LinguaGacha) `使用 AI 能力一键翻译小说、游戏、字幕的次世代翻译器` `推荐` 👈👈
  - [KeywordGacha](https://github.com/neavo/KeywordGacha) `使用 AI 能力一键生成术语表的次世代翻译辅助工具` `推荐` 👈👈
  - [AiNiee](https://github.com/NEKOparapa/AiNiee)
  - [GalTransl](https://github.com/xd2333/GalTransl)
  - [绿站（轻小说翻译机器人）](https://books.fishhawk.top/workspace/sakura)
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
  
| 显存大小         | 模型规模    | 启动脚本        | 下载链接                                                   |
|:---------------:|:-----------:|:--------------:|:---------------------------------------------------------:|
| 8G/10G          | 7B          | 01_2K_NP8.bat  | [sakura-7b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-7B-Qwen2.5-v1.0-GGUF/blob/main/sakura-7b-qwen2.5-v1.0-iq4xs.gguf) |
| 11G             | 14B         | 01_2K_NP3.bat  | [sakura-14b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-iq4xs.gguf) |
| 12G             | 14B         | 01_2K_NP6.bat  | [sakura-14b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-iq4xs.gguf) |
| 16G             | 14B         | 01_2K_NP16.bat | [sakura-14b-qwen2.5-v1.0-iq4xs.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-iq4xs.gguf) |
| 24G             | 14B         | 01_2K_NP16.bat | [sakura-14b-qwen2.5-v1.0-q6k.gguf](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2.5-v1.0-GGUF/blob/main/sakura-14b-qwen2.5-v1.0-q6k.gguf) |

- 其他语言之间的互译（8B 效果很差，14B 勉勉强强，最好使用在线API）
- 搭配 KeywordGacha 抓取实体词语表

| 显存大小         | 模型规模    | 启动脚本        | 下载链接                                                   |
|:---------------:|:-----------:|:--------------:|:---------------------------------------------------------:|
| 8G/10G          | 7B          | 01_2K_NP8.bat  | [Qwen3-8B-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen_Qwen3-8B-GGUF/blob/main/Qwen_Qwen3-8B-IQ4_XS.gguf) |
| 11G             | 14B         | 01_2K_NP3.bat  | [Qwen3-14B-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen_Qwen3-14B-GGUF/blob/main/Qwen_Qwen3-14B-IQ4_XS.gguf) |
| 12G             | 14B         | 01_2K_NP6.bat  | [Qwen3-14B-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen_Qwen3-14B-GGUF/blob/main/Qwen_Qwen3-14B-IQ4_XS.gguf) |
| 16G             | 14B         | 01_2K_NP16.bat | [Qwen3-14B-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen_Qwen3-14B-GGUF/blob/main/Qwen_Qwen3-14B-IQ4_XS.gguf) |
| 24G             | 14B         | 01_2K_NP16.bat | [Qwen3-14B-IQ4_XS.gguf](https://huggingface.co/bartowski/Qwen_Qwen3-14B-GGUF/blob/main/Qwen_Qwen3-14B-IQ4_XS.gguf) |

## 启动
- 现在你的文件结构应该类似于：
```
  OneClickLLAMA\llama\...
                    \00_Core.bat
                    \01_2K_NP16.bat
                    \sakura-14b-qwen2.5-v1.0-iq4xs.gguf
                    \...
```
- 根据 `你的显存和模型的搭配组合` 选择对应的启动脚本，双击启动即可
  
## 应用设置
- 根据你的需求和使用的应用查看对应设置教程
  - 搭配 [LinguaGacha](https://github.com/neavo/LinguaGacha) 进行日中翻译 [Wiki - LinguaGacha_Sakura](https://github.com/neavo/OneClickLLAMA/wiki/LinguaGacha_Sakura)  `推荐` 👈👈
  - 搭配 [LinguaGacha](https://github.com/neavo/LinguaGacha) 进行其他语言翻译 [Wiki - LinguaGacha](https://github.com/neavo/OneClickLLAMA/wiki/LinguaGacha)  `推荐` 👈👈
  - 搭配 [KeywordGacha](https://github.com/neavo/KeywordGacha) 进行文本分析 [Wiki - KeywordGacha](https://github.com/neavo/OneClickLLAMA/wiki/KeywordGacha)  `推荐` 👈👈
  - 搭配 [AiNiee](https://github.com/NEKOparapa/AiNiee) 进行日中翻译 [Wiki - AiNiee_Sakura](https://github.com/neavo/OneClickLLAMA/wiki/AiNiee_Sakura)
  - 搭配 [轻小说翻译机器人（绿站）](https://books.fishhawk.top/) 进行日中翻译 [Wiki - AutoNovel_Sakura](https://github.com/neavo/OneClickLLAMA/wiki/AutoNovel_Sakura)

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
