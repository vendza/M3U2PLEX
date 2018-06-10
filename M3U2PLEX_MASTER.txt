@echo off
title M3U2PLEX
echo Welcome To M3U2PLEX Startup Guide
pause
echo Please Enter Your M3U Below:
set /p -playlist=""
echo your -playlist= is %-playlist%
if '%-playlist=%'=='' mkdir %USERPROFILE%\AppData\Local\Temp\Telly
pause
cd %USERPROFILE%\Downloads
telly-windows-amd64.exe -playlist="%-playlist%"  -streams=5 -friendlyname=M3U2PLEX -listen=localhost:7575 -deviceid=12345678 -logrequests -temp=%USERPROFILE%\AppData\Local\Temp\Telly\file



