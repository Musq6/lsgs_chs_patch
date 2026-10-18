# 第三方组件 / Third-Party Components

本补丁以二进制形式分发以下第三方组件。它们**未被修改**，按原样分发，
其版权归各自作者所有，协议全文见 `licenses/` 目录。

---

## BepInEx 5.4.23.4

- **协议**：GNU Lesser General Public License v2.1（LGPL-2.1）
- **版权**：Copyright (c) BepInEx contributors
- **源码**：https://github.com/BepInEx/BepInEx
- **许可证全文**：`licenses/LGPL-2.1.txt`
- **位置**：`BepInEx/core/`
- **修改**：无

## UnityDoorstop 4.4.1

- **协议**：GNU Lesser General Public License v2.1（LGPL-2.1）
- **版权**：Copyright (c) NeighTools and contributors
- **源码**：https://github.com/NeighTools/UnityDoorstop
- **许可证全文**：`licenses/LGPL-2.1.txt`
- **位置**：`winhttp.dll`
- **修改**：无

## HarmonyX 2.10.2

- **协议**：MIT
- **版权**：Copyright (c) 2020 BepInEx
- **源码**：https://github.com/BepInEx/HarmonyX
- **许可证全文**：`licenses/MIT-HarmonyX.txt`
- **位置**：`BepInEx/core/0Harmony.dll` 等（随 BepInEx 内置）
- **修改**：无

## MonoMod / Mono.Cecil

随 BepInEx 内置的间接依赖，协议分别为 MIT 与 MIT，未作修改。

---

## LGPL-2.1 合规说明

1. 上述 LGPL 组件的完整许可证全文已随本仓库提供（`licenses/LGPL-2.1.txt`）。
2. 组件源码可从上方链接获取；本项目**未修改**这些组件，因此无需另行公开修改。
3. 这些组件以独立程序集 / 独立可执行文件的形式分发，使用者可以自行替换，
   本项目未对其加壳、混淆或做任何阻碍替换的处理。
4. 本补丁自身的代码与译文使用 MIT 协议（见 `LICENSE`），与上述组件相互独立。
