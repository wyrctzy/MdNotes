## Windows Register Etc

### 增加主题（颜色）模式
```vbs
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\DesktopBackground\Shell\AppMode]
"Icon"="imageres.dll,237"
"MUIVerb"="主题模式(&Z)"
"Position"="Bottom"
"SubCommands"=""

[HKEY_CLASSES_ROOT\DesktopBackground\Shell\AppMode\Shell]

[HKEY_CLASSES_ROOT\DesktopBackground\Shell\AppMode\Shell\lbflyout]
"Icon"="imageres.dll,-5412"
"MUIVerb"="深色模式(&Z)"

[HKEY_CLASSES_ROOT\DesktopBackground\Shell\AppMode\Shell\lbflyout\command]
@="cmd /c Reg Add HKCU\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Themes\\Personalize /v AppsUseLightTheme /t REG_DWORD /d 0 /f &&Reg Add HKCU\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Themes\\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 0 /f"

[HKEY_CLASSES_ROOT\DesktopBackground\Shell\AppMode\Shell\liflyout]
"MUIVerb"="浅色模式(&X)"
"Icon"="imageres.dll,-5411"

[HKEY_CLASSES_ROOT\DesktopBackground\Shell\AppMode\Shell\liflyout\command]
@="cmd /c Reg Add HKCU\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Themes\\Personalize /v AppsUseLightTheme /t REG_DWORD /d 1 /f &&Reg Add HKCU\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Themes\\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 1 /f"
```
