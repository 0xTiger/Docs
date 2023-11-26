{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg 文件",
"cfg mugen 配置文件",
"什么是 cfg 文件",
"如何打开cfg文件",
"文件",
"cfg 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "CFG 文件格式 - MUGEN 配置文件",
  "description":"了解 CFG MUGEN 配置文件格式以及可以创建和打开 CFG 文件的 API。",
"linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen",
"parent": "game"
}
},
"lastmod": "2023-09-27"
}

## 什么是一 .cfg 文件？

MUGEN 上下文中的 CFG 文件指的是"MUGEN 配置文件"。 **MUGEN** 是由 Elecbyte 开发的可定制 2D 格斗游戏引擎。用户可以通过编辑包括CFG文件在内的各种配置文件来创建自己的角色,阶段,甚至修改游戏的行为和规则。

以下是您在 MUGEN `.cfg` 文件中可能找到的内容的基本概述：

1. **系统配置**：CFG 文件通常包含与游戏引擎的一般行为相关的设置。这包括屏幕分辨率,声音设置和输入配置（键盘,操纵杆或控制器映射）等。
    








2. **角色和场景默认设置**：您可以定义角色和场景的默认设置。例如,您可以指定游戏开始时加载哪些角色和阶段。
    








3. **游戏选项**：MUGEN `.cfg` 文件还可以控制各种游戏选项,例如回合时间限制,伤害缩放等。
    








4. **调试和开发**：高级用户可以使用".cfg"文件进行调试和开发。这些设置可以控制调试信息在屏幕上的显示方式或定义其他与开发相关的行为。
    








5. **屏幕包配置**：屏幕包是改变游戏外观和感觉的视觉主题。 `.cfg` 文件可以指定使用哪个屏幕包并配置其各种元素。
    








6. **AI 行为**：MUGEN 允许您定义计算机控制的角色 (AI) 在战斗中的行为方式。 `.cfg` 文件可以包含与 AI 难度和行为相关的设置。

## MUGEN 配置文件

MUGEN CFG（配置）文件对于自定义格斗游戏世界的创作者来说是至关重要的组件。它使他们能够制定游戏的基本规则。这包括每轮持续多长时间,计算机控制的对手提出的挑战级别,游戏节奏,连击影响伤害的程度等因素。

此外,CFG 文件允许创建者确定游戏的显示设置,例如屏幕分辨率,并决定 MUGEN 是否应在游戏过程中播放音效和音乐。对于那些熟悉 MUGEN 复杂性的人来说,此文件提供了调整一系列其他游戏相关设置以打造独特游戏体验的潜力。

默认情况下,MUGEN 的主 CFG 文件（称为"mugen.cfg"）位于程序的数据文件夹中。虽然可以在此文件中直接编辑游戏设置,但通常建议首先创建备份副本。此预防措施可确保您可以在需要时轻松将 MUGEN 恢复为其原始设置,防止任何意外更改破坏您的游戏体验。

## MUGEN - 游戏引擎

MUGEN 是 Elecbyte 开发的多功能且高度可定制的 2D 格斗游戏引擎。 "MUGEN"这个名字代表"Mugen 终极游戏引擎"。它最初于 1999 年发布,自此赢得了由用户和创作者组成的专门社区,他们使用引擎来设计和开发自己的 2D 格斗游戏。

以下是 MUGEN 的一些主要功能和方面：

1. **可自定义角色：** MUGEN 允许用户创建并导入自己的角色（称为"战士"或"精灵"）到游戏中。创作者可以为这些角色设计独特的动作,动画和特殊攻击,从而可以包含来自各种系列或原创作品的几乎任何角色。
    








2. **关卡：** 除了角色之外,用户还可以创建和自定义发生战斗的关卡。这些阶段可以有互动元素和独特的背景。
      









3. **屏幕包：** 屏幕包是改变游戏整体外观的视觉主题,包括菜单,角色选择屏幕和生命栏。用户可以创建和共享自己的屏幕包,为他们的游戏提供独特的外观和感觉。
    








4. **声音和音乐：** 创作者可以为他们的游戏添加音效和背景音乐,增强整体游戏体验。
    








5. **脚本：**高级用户可以使用内置的脚本语言来创建复杂的角色行为,独特的游戏机制和特效。

## 如何打开 CFG 文件？

MUGEN CFG 文件是纯文本文档,可以使用各种文本编辑器进行访问。在 Windows 上,您可以使用 Microsoft 记事本或写字板,而 macOS 用户可以使用 Apple TextEdit 来实现此目的。这些编辑器允许用户轻松查看和修改 CFG 文件中的配置设置。

打开或引用 CFG 文件的程序

- Elecbyte MUGEN
- 记事本
- 文本编辑

## 其他 CFG 文件

以下是使用 **.cfg** 文件扩展名的其他文件类型。

**设置**
- [CFG - Celestia 配置文件](/zh/settings/cfg-celestia/)
- [CFG - Citrix 服务器连接文件](/zh/settings/cfg-citrix/)
- [CFG - MAME 配置文件](/zh/settings/cfg-mame/)
- [CFG - LightWave 配置文件](/zh/settings/cfg-lightwave/)

**游戏**
- [CFG - 韦诺标记语言文件](/zh/game/cfg-wesnoth/)
- [CFG - MUGEN 配置文件](/zh/game/cfg-mugen/)
- [CFG - 源引擎配置文件](/zh/game/cfg-sourceengine/)

**系统及杂项**
- [CFG - CFG 文件](/zh/system/cfg/)
- [CFG - Cal3D 模型配置文件](/zh/misc/cfg-cal3d/)

## 参考
* [Mugen（游戏引擎）](https://en.wikipedia.org/wiki/Mugen_(game_engine))
