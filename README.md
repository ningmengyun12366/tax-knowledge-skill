# 柠檬云AI财税专家咨询

本公开源码包只包含 `tax-knowledge` 业务 Skill。公共的 Go 实现、Node.js 打包脚本和依赖代码保留在 `go-script/` 中，便于查看、构建和维护。

## 描述

**名字：** AI财税咨询专家_财税专家_财税实务咨询_税务合规建议_财税政策解读_会计实操_财务咨询_柠檬云财税Skill

**描述：**

柠檬云AI财税开放平台：AI财税咨询专家Skill，依托国家税务总局、财政部、企业会计准则等权威财税知识库打造智能财税专家，为企业、会计人员提供可解释、可追溯的财税实务咨询、政策解读与税务合规建议服务。
本 Skill 依托国家税务总局、财政部、会计准则等权威财税知识库打造 AI 财税专家，可针对企业财务、会计核算、税务与经营过程中的实际问题，提供专业分析、政策依据解读及合规建议，并附带官方文件来源，确保相关结论有据可查。
✅企业财税咨询：支持企业财务、会计实操、税务与经营过程中的实务问题判断与咨询，涵盖账务处理、会计分录、纳税申报、发票管理、涉税风险排查及各类涉税事项处理建议；
✅政策法规智能解读：对复杂财税法规、税收新政、会计准则进行结构化拆解与业务化解读，帮助财务、会计从业者理解政策在实际业务中的落地应用；
✅官方依据溯源：财税解答自动匹配对应官方政策文件，附带政策原文跳转链接，税务、会计相关结论有据可查。

详细的 Skill 规则、使用前准备和安装更新流程见 [`tax-knowledge/README.md`](./tax-knowledge/README.md)、[`tax-knowledge/SKILL.md`](./tax-knowledge/SKILL.md) 和 [`tax-knowledge/tax-knowledge-install.md`](./tax-knowledge/tax-knowledge-install.md)。

## 目录结构

- `tax-knowledge/`：当前 Skill 的说明、安装文档、引用资料和资源。
- `go-script/`：Go 命令行实现、公共库和生产打包脚本。

## 生产构建

构建要求 Node.js 20+ 和 Go 1.24+。请在仓库根目录执行：

```powershell
npm ci
node go-script/build.js --env prod tax-knowledge
```

生产发布物生成在 `dist/Skills/tax-knowledge/`。运行时 ZIP 包不包含 `bin/**` 二进制文件，安装时按安装文档下载当前平台对应的二进制。

## 配置与数据安全

- API 凭据由使用者在本地工作区配置，不应写入源码、文档或日志。
- 生产接口通过 `go-script/config/prod.json` 注入发布包。
- 安全问题请按照 [SECURITY.md](SECURITY.md) 私下报告。

## 许可证

本项目自有代码、文档和资源文件采用 [MIT License](LICENSE)；第三方组件与字体许可见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
