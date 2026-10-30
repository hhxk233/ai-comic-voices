# 来源与待核实事项

此文件是来源说明，不是法律授权书。本仓库没有给全部文件授予统一的 MIT、Apache 或其他再分发许可。

## 三段原创 Qwen 合成试听

- 模型：[Qwen3-TTS VoiceDesign](https://huggingface.co/Qwen/Qwen3-TTS-12Hz-1.7B-VoiceDesign)，版本 `5ecdb67327fd37bb2e042aab12ff7391903235d3`。
- 成片延续模型：[Qwen3-TTS Base](https://huggingface.co/Qwen/Qwen3-TTS-12Hz-1.7B-Base)，版本 `fd4b254389122332181a7c3db7f27e918eec64e3`。
- 两个模型的官方模型页标注 Apache-2.0；[官方使用说明](https://github.com/QwenLM/Qwen3-TTS) 支持先设计声音，再通过 Base 和合成参考延续声音。
- 本项目记录显示，claude / grok / gemini 是用通用成年角色描述生成的原始合成声音，未使用第三方创作者录音。三段例子均来自已选试听，输入句子仅用于漫画试音。
- 本包没有分发这些模型的权重、模型代码或原始合成参考。模型许可不自动解决所有音频输出、角色或商标使用问题；三段原始合成试听在此展示；本说明不额外授予统一的复用或商业使用许可。

## gpt：Microsoft Edge 晓晓

- 生成方式：Microsoft Edge online speech，经 [edge-tts](https://github.com/rany2/edge-tts) 调用预设 `zh-CN-XiaoxiaoNeural`。
- edge-tts 客户端代码的开源许可不能当作微软声线或音频产出的再分发许可；其他付费服务的条款也不能直接套用到这次 Edge 调用。
- 本仓库只给出来源和参数，不附 gpt 音频、参考音频、声音模型或供应商声音资源。需要先找到适用于实际生成服务的输出使用/再分发依据。

## deepseek：FeiyuVoice-CosyVoice3

- 模型来源：[FeiyuVoice-CosyVoice3](https://huggingface.co/Esmerubphire/FeiyuVoice-CosyVoice3)，本地选用版本 `f37e9d1dda26e8b45b4e9f1b4c347c0a07b797e2`，`cute / F6_0040`。
- 权利核对参考：[v1.0.1 发布说明](https://huggingface.co/Esmerubphire/FeiyuVoice-CosyVoice3/commit/da3b2cb7855e017f477e4986688d104883d8f70d)、[COPYRIGHT.md](https://github.com/Esmerubphire/astrbot_plugin_feiyu_voice/blob/main/COPYRIGHT.md)、[NOTICE.md](https://github.com/Esmerubphire/astrbot_plugin_feiyu_voice/blob/main/NOTICE.md)。
- 基础模型/代码许可不自动覆盖附带角色、参考/训练素材和所有音频输出用途。新训练授权也不能单独证明本次输出可以再分发。
- 这不是本项目原创设计或官方 DeepSeek 声音；也未证明与任何特定创作者视频使用同一声线。
- 本仓库只附公开来源、版本和非秘密设置，不附 deepseek 的试听、附带参考、训练素材或模型权重。剩余事项是明确此次角色及素材链对生成输出再分发的授权。

五个 AI 名称仅用于说明漫画角色，没有官方合作或背书之意。使用相关资料时，请分别核对上游条款、输入/参考素材及具体用途。
