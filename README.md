# 五个 AI 漫画角色的配音资料

给漫画里的 gpt、claude、grok、gemini、deepseek 选了五个固定声音，把来源、提示词、设置和短试听整理在这里，方便交流。

这些是漫画里的角色配音，不是各家产品的官方声音，也不代表社区统一音源。gpt 和 codex 共用一个声音；小白团不说话，不计入这五个角色。

| 角色 | 当前选择 | 实际来源 | 试听 |
| --- | --- | --- | --- |
| gpt / codex | GPT-A | Microsoft Edge 晓晓预设音色 | 只有制作说明，音频输出的再分发依据尚未明确 |
| claude | CLAUDE-C | 原创 Qwen3-TTS VoiceDesign，后续用 Base 延续声线 | [claude.mp3](examples/claude.mp3) · 6.24 秒 |
| grok | GROK-D | 原创 Qwen3-TTS VoiceDesign，后续用 Base 延续声线 | [grok.mp3](examples/grok.mp3) · 3.52 秒 |
| gemini | GEMINI-D | 原创 Qwen3-TTS VoiceDesign，后续用 Base 延续声线 | [gemini.mp3](examples/gemini.mp3) · 5.04 秒 |
| deepseek | DEEPSEEK-C | FeiyuVoice-CosyVoice3 大肥鱼可爱版角色模型 | 只有制作说明，角色及附带素材的权利范围尚未明确 |

三段试听来自已选中的中性试音句，没有使用成片里的私人对白。文件是原有试听导出副本，没有重新合成；均为单声道、24 kHz MP3，可下载到本地播放器试听。

## 制作方法

- **gpt**：通过 edge-tts 调用 `zh-CN-XiaoxiaoNeural`，语速 `-6%`，音高 `+0Hz`。这是供应商预设声线，没有声线设计提示词。
- **claude / grok / gemini**：用通用的成年角色描述，在 Qwen3-TTS VoiceDesign 中设计声音，没有输入第三方创作者录音。选中合成 WAV 后，成片用 Qwen3-TTS Base，以同一段合成参考和对应文本延续声音。这里的 MP3 是最初设计试听，不是 Base 成片对白。设计提示词、种子、模型版本及延续设置见 [manifest.json](manifest.json) 和 [prompts](prompts/)。
- **deepseek**：使用 FeiyuVoice-CosyVoice3 1.0.1 的 `cute / F6_0040` 检查点与其附带参考，CosyVoice3 zero-shot，种子 `42`，速度 `1.0`，FP32。不是本项目原创设计的声库；这里只记录来源和设置。

本仓库不带模型权重、第三方参考录音、原始合成参考 WAV、原始请求或日志。只凭种子不保证在不同环境复现完全相同的声音；要精确延续已选声线，需要对应的原始合成参考。

## 来源与使用范围

- [Qwen3-TTS VoiceDesign](https://huggingface.co/Qwen/Qwen3-TTS-12Hz-1.7B-VoiceDesign) 和 [Base](https://huggingface.co/Qwen/Qwen3-TTS-12Hz-1.7B-Base)：三段原创合成试听的模型来源。
- [edge-tts](https://github.com/rany2/edge-tts)：调用工具。代码许可证不等于微软声线或生成音频的再分发授权，因此这里不附 gpt 音频。
- [FeiyuVoice-CosyVoice3](https://huggingface.co/Esmerubphire/FeiyuVoice-CosyVoice3) 及其 [素材来源说明](https://github.com/Esmerubphire/astrbot_plugin_feiyu_voice/blob/main/COPYRIGHT.md)：基础模型或代码的许可不自动覆盖角色、训练/参考素材和所有生成用途，因此这里不附 deepseek 音频。

模型许可、音频产出和角色使用范围分别说明，本仓库没有给全部资料统一套用 MIT、Apache 或商业复用许可。详细来源及尚未明确的范围见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)，文件校验信息见 [checksums.json](checksums.json)。

## 想听听大家的意见

哪个声音最贴角色？哪里还能更自然？普通话、英文名字发音，以及同一角色在不同句子里的声音一致性，都欢迎交流。
