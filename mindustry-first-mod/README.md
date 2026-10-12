# Franky's First Mindustry Mod

一个最小可运行的 Mindustry 模组：加了一面叫 **Hyper Wall** 的自定义墙（2×2，3000 血）。
不用装 JDK、不用编译，丢进游戏就能用。

## 三步上手（比看教程快）

1. **装游戏**：Steam / itch.io / 官网 mindustrygame.github.io 随便下一个（手机端也行）。
2. **放 mod**：把这个 `mindustry-first-mod` 文件夹整个复制到游戏的 mods 目录：
   - macOS：`~/Library/Application Support/Mindustry/mods/`
   - Windows：`%appdata%/Mindustry/mods/`
   - Linux：`~/.local/share/Mindustry/mods/`
   - 一句话命令（macOS）：
     ```
     cp -r mindustry-first-mod ~/Library/Application\ Support/Mindustry/mods/
     ```
3. **启用**：进游戏 → 主菜单 **Mods** → 找到 `Franky's First Mod` → 点启用 → 开一局，在墙分类里就能看到 **Hyper Wall**。

## 怎么改（从这里开始魔改）

- 改数值：编辑 `content/blocks/walls/hyper-wall.hjson`
  - `health` 血量、`size` 占地（1 或 2，改了要相应改贴图尺寸）、`solid` 是否实心。
- 加新方块：在 `content/blocks/` 下照猫画虎新建 `.hjson`，同时在 `sprites/blocks/` 对应位置放同名 PNG。
- 改显示名/描述：编辑 `bundles/bundle.properties`（`block.<名字>.name` / `.description`）。
- 想加资源、炮塔、单位：字段写法看官方 modding wiki →
  https://mindustrygame.github.io/wiki/modding/1-modding

## 贴图说明

`sprites/blocks/walls/hyper-wall.png` 是用仓库根目录的 `gen_sprite.py`
（纯 Python 标准库生成，无第三方依赖）画的占位图。重画它替换即可换外观。

## 许可证

Mindustry 本体是 GPL-3.0。这个 mod 也按 GPL-3.0 发布——
**你自己改着玩完全自由；哪天想发给别人，记得把源码（就是这个文件夹）一起公开就行。**
