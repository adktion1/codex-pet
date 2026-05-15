# Yunou Codex 宠物

[English README](README.md)

Yunou 是一个原创 Codex 动画宠物，设计灵感来自云端偶戏、风筝挂饰、柔软云形、飘带流苏和雅致的戏曲妆面。

它是一个紧凑的贴纸风格小宠物，使用青绿、珊瑚橙、金色、象牙白和炭黑配色。角色为原创设计，不隶属于、也不复制任何现有游戏、角色、皮肤、标志或官方素材。

## 内容

- `pets/yunou/pet.json` - Codex 宠物配置文件
- `pets/yunou/spritesheet.webp` - 最终 9 状态动画图集
- `qa/contact-sheet.png` - 视觉 QA 总览图
- `qa/previews/*.gif` - 每个状态的动画预览
- `qa/validation.json` - 图集校验结果
- `qa/review.json` - 帧检查结果

## 安装

把 `pets/yunou` 文件夹复制到你的 Codex 宠物目录：

```powershell
Copy-Item -Recurse -Force .\pets\yunou "$env:USERPROFILE\.codex\pets\yunou"
```

然后在 Codex 中选择或重新加载该宠物。

## 图集规格

- 尺寸：`1536x1872`
- 单元格：`192x208`
- 行数：9
- 格式：带透明通道的 WebP

状态列表：

1. `idle` - 待机
2. `running-right` - 向右拖动
3. `running-left` - 向左拖动
4. `waving` - 挥手
5. `jumping` - 跳跃
6. `failed` - 失败/受阻
7. `waiting` - 等待输入或确认
8. `running` - 任务处理中
9. `review` - 审阅/检查完成结果

## QA

图集已通过 hatch-pet 校验脚本检查。

- `validation.json`：无错误，无警告
- `review.json`：无错误，无警告
- 透明像素 RGB 残留：`0`

![Yunou contact sheet](qa/contact-sheet.png)

## 许可

本仓库使用 CC BY 4.0 许可。详情见 `LICENSE`。
