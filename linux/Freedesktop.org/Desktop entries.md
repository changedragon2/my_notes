[Category](https://wiki.archlinux.org/title/Category:Freedesktop.org)
	[Desktop entries](https://wiki.archlinux.org/title/Desktop_entries)
桌面项  xxx.desktop
 1. Application entry（程序项）
	目录
		i）系统用户：/usr/share/applications   or  /usr/local/share/applications
		ii）个人用户： ~/.local/share/applications
	模板
		 ````[Esktop Entry]
		# The type available Application, Link, Directory.
		# 桌面项类型（必须有）
		Type=Application
		# The version of the desktop entry specification to which this file complies
		Version=1.0
		# The name of the application
		# 名称（必须有）
		Name=xxx
		# A comment which can/will be used as a tooltip
		Comment=xx xxx xx
		# The path to the folder in which the executable is run
		Path=/opt/xxx
		# The executable of the application, possibly with arguments
		Exec=/path/to/executable
		# The name of the icon that will be used to display this entry
		Icon=/path/to/icon
		# Describes whether this application needs to be run in a terminal or not
		Terminal=false
		# Describes the categories in which this entry should be shown
		Categories=Education;Languages;Game;
```
