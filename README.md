# youtube_to_mp3
youtube link to mp3 converter 

1. DOWNLOAD YT-DLP
[<YT_DLP>](<https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe>)
3. PASTE THE BELOW CODE INTO NOTEPAD AND SAVE AS A ".bat" FILE AND SAVE TO DESKTOP
4. ENSURE THAT DESTINATION FILE IS REPLACED IN THE CODE BELOW

@echo off

:START
set /p URL=Paste YouTube URL (or type exit): 

if /i "%URL%"=="exit" goto END

C:\yt-dlp.exe ^
-P "C:\DESTINATION FILE (replace with your own)" ^
-x ^
--audio-format mp3 ^
-o "%%(title)s.%%(ext)s" ^
"%URL%"

echo.
goto START

:END
echo Exiting...
pause
