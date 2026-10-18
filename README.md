# 对标视频 → 可复用生成提示词

> 作者：胡峻  
> Copyright © 2026 胡峻。保留所有权利。

包内 `reference-video-template/` 是完整 Skill，入口为 `SKILL.md`。所有方法引用均在该文件夹中；不依赖作者本机的 Skill、路径、账号或飞书资料。

## 怎么用

在支持本地 Agent Skills 的宿主中，将整个 `reference-video-template` 文件夹放进该宿主识别的 skills 目录，并按宿主方式重新加载技能。不要只复制 SKILL.md，也不要多嵌套一层同名目录。不同宿主的安装位置不同，以宿主的实际设置为准。

如果暂时不安装，可把整个文件夹放进 AI 能读取的项目，直接告诉它：

> 请读取 reference-video-template/SKILL.md，按照其中方法拆解我提供的视频，再写新的生成提示词。

若宿主只能接收文件附件，请提供 SKILL.md 及 references 中的四份 Markdown；这些文件共同构成完整方法。宿主仍需能查看视频/图片；本包不能为纯文本模型增加视听能力。

已识别该 Skill 后可说：

> 用 $reference-video-template 拆解这个视频。我想保留它的动作和转场，把人物换成我提供的照片、场景换成海边。先给我可复用母版和本次完整提示词，暂时不生成。

或：

> 用 $reference-video-template 打一个生成模板。先分析，再判断是否需要垫图。如果我已经配置的视频工具支持，就生成一版给我看；不要自行剪辑或上传。

## 包含什么

- 原片查看、事件表、动作/镜头/空间/转场/声音的拆解方法。
- T2V、I2V、多参考的选择与垫图判断。
- 参数化母版、本次完整实例、素材和声音交付方法。
- 结果对照和返修方法，以及一个明确标为虚构的完整示例。
- 可选 FFmpeg/FFprobe 命令；不使用命令也能按宿主能力完成分析。

## 使用边界

方法和提示词编写无需 API 密钥。真实视频生成需使用者自己的可用工具、账号和授权；本包不附付费服务或自动安装程序。链接打不开时可直接提供本地原片。声音不可听、片段不可见或结果未生成时，Skill 会要求如实标注。

仅打包通用方法，不含原作者的视频、配乐、照片、个人路径、账号标识或私有 API。不要把解压成功理解为任何宿主都已自动安装；将 Skill 放到宿主可发现的位置，或让代理显式读取入口即可开始。

版本：1.0.2（2026-10-18）。

## 文件入口

- [Skill 入口](reference-video-template/SKILL.md)
- [视频拆解方法](reference-video-template/references/analyze-reference.md)
- [提示词写作方法](reference-video-template/references/write-prompts.md)
- [返修与教学示例](reference-video-template/references/review-and-example.md)
- [版权声明](COPYRIGHT.txt)
