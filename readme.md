# 列宁街小卖部 Demo 汉化包

《Lenin Street Geek Shop》Demo 的简体中文补丁。

- **适用版本**：Lenin Street Geek Shop Demo（Unity 6000.0.58f2，Mono 后端）
- **汉化范围**：界面 3,055 条 + 对话 17,897 条，覆盖率 100%
- **补丁体积**：约 3.2 MB，不修改任何游戏本体文件

## 使用的框架

| 框架 | 版本 | 用途 |
|---|---|---|
| **BepInEx** | 5.4.23.4（x64） | Unity 插件加载框架，补丁宿主 |
| **Doorstop** | 4.4.1 | 通过 `winhttp.dll` 劫持进程启动，拉起 BepInEx 预加载器 |
| **HarmonyX** | 随 BepInEx 5.4 内置 | 运行时方法拦截，用于文本替换与字体处理 |
| **TextMeshPro** | 游戏自带 | 通过运行时挂载中文字体资产实现中文显示 |

补丁本体是自行编写的 C# 插件（netstandard2.1），未使用词典替换、资源包覆写等第三方汉化工具。

## 安装

把本目录**全部内容**复制到游戏根目录（与 `Lenin Street Geek Shop.exe` 同级），启动即为中文。

```
Lenin Street Geek Shop\
  ├─ Lenin Street Geek Shop.exe
  ├─ winhttp.dll
  ├─ doorstop_config.ini
  ├─ .doorstop_version
  └─ BepInEx\
```

详细说明（配置、改词库、自检、已知问题）见 **`安装说明.txt`**。

## 卸载

删除以下四项即可，游戏恢复原样：

```
winhttp.dll
doorstop_config.ini
.doorstop_version
BepInEx\
```

## 注意

- **首次启动会卡约 20 秒**（窗口显示未响应），是补丁在生成 3,073 个汉字的字形图集，属正常现象。
- `BepInEx\config\lsgs.zh.patch.cfg` 里的 `FontRegister` **必须保持 `none`**，改成 `all` 会导致卡死。
- 修改配置文件前请先**完全关闭游戏**，否则退出时会被回写覆盖。

## 许可证

本补丁的插件代码与译文以 **MIT** 协议发布，见 [`LICENSE`](LICENSE)。

打包内附带的第三方组件协议不同，均为原样分发、未作修改：

| 组件 | 协议 | 全文 |
|---|---|---|
| BepInEx 5.4.23.4 | LGPL-2.1 | [`licenses/LGPL-2.1.txt`](licenses/LGPL-2.1.txt) |
| UnityDoorstop 4.4.1 | LGPL-2.1 | [`licenses/LGPL-2.1.txt`](licenses/LGPL-2.1.txt) |
| HarmonyX 2.10.2 | MIT | [`licenses/MIT-HarmonyX.txt`](licenses/MIT-HarmonyX.txt) |

版权归属与合规说明详见 [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md)。

## 免责声明

- 本补丁不含游戏本体文件，也不含任何字体文件（中文显示使用系统自带字体），
  使用前请先自行获得游戏本体。
- 游戏内文本及其译文版权归原权利所有，译文仅供学习交流使用，请勿用于商业用途。
- 补丁仅修改运行时的显示文本，不触碰存档与游戏文件，但使用修改类工具的风险请自行评估，
  因使用本补丁造成的任何问题由使用者自行承担。

