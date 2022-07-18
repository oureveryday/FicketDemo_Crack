# Ficket: 追剧引擎 Demo 破解 
原工具网址: https://store.steampowered.com/app/1634680/ 

## 破解方法 
1. 下载并安装 [Node.js](https://nodejs.org/) 
2. 在命令提示符下运行 :`npm -g install --engine-strict asar`
3. 使用 asar 解压 resources/app.asar :`asar e resources/app.asar resources/app.asar.unpacked`
4. 在 `resources\app.asar.unpacked\dist\renderer.prod.js` 中搜索并替换:
    * 搜索：`":"FicketDemo"`
    * 替换为：`":"Ficket"`

    * 搜索：`"FicketDemo"===Bk.u2||LR.get("version")!==Bk.i8`
    * 替换为：`"FicketDemo"===Bk.u2`
5. 使用 asar 打包 resources/app.asar :`asar p --unpack="resources/app.asar.unpacked/node_modules/greenworks/**" resources/app.asar.unpacked resources/app.asar`
6. 使用任意Steam模拟器替换 
`resources\app.asar.unpacked\node_modules\greenworks\deps\steamworks_sdk\redistributable_bin\steam_api.dll` 和
`resources\app.asar.unpacked\node_modules\greenworks\deps\steamworks_sdk\redistributable_bin\win64\steam_api64.dll` 并配置模拟器

## 下载
[Ficket_Crack.7z](https://raw.githubusercontent.com/oureveryday/FicketDemo_Crack/main/Ficket_Crack.7z)
(Steam Appid: 1634720/Build:14723591)