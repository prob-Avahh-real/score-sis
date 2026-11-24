# 谱你妹 (Score Sis)

互动式音乐制作入门教学。零基础学编曲，Web Audio API 实时合成反馈。

## 用途与 Target 判定

| 平台 | 需要? | 方式 |
|------|-------|------|
| 移动端 | 需要 | Capacitor (`android/` + `ios/`) |
| 智能硬件 | 可选 | 互动钢琴卷帘以触屏编曲为主，穿戴输入可选（当前搁置） |

## 课程体系

8 课渐进式：音符→节奏→音阶→和弦→进行→旋律→分层→节奏

## 技术栈

- Web Audio API 合成器
- 互动钢琴卷帘
- 渐进式教程引擎
- Capacitor 原生包装

## Harness / Loop（助手）

- 遵循根 `/Users/skat/AGENTS.md`：**Harness Engineering** + **Loop Engineering**
- Guide = 本文件；Sensor = 下方验证命令；同类失误第二次须沉淀规则或测试（棘轮）
- 开干前写清 **Done**；每切片过验证环；显式停止（成功 / 上限 / 无进展 / 人审）
- 详解：`docs/HARNESS_ENGINEERING.md`、`docs/LOOP_ENGINEERING.md`

## 验证环 / Done

```bash
npm install
npm test          # 若有
npm run build     # 或 build:web
npx cap sync android   # 若有 android/
# 可选：JAVA_HOME=…/openjdk@17 npm run apk:debug
```

**Done 示例**：测试通过（若有）+ web 产物进 `www/`/`dist/` + `cap sync` 无报错。可选穿戴未做可搁置，不纳入强制 Done。
