# LOG_GIGANTIC_TROJAN

<h1>Описание:</h1>
<h2>Релиз нового нативного резидентного вируса, написанного на C, C++ и питоне (питон чисто для отправки логов с кейлоггера и скриншотов) с использованием winapi 32 👨‍💻</h2>
вирус не детектится абсолютно никакими антивирусами, копируется в svchost.exe, создает кучу новых процессов и заражает все активные .exe файлы на компьютере.
реализован инжект в виде библиотеки динамической компоновки (dll) в абсолютно любые удобные для пользователя процессы. 
к примеру, я выбрал MicrosoftSoundController, который склеен с инъекцией вируса и мусорными dll файлами Microsoft. 

<h2>программа управляет буфером обмена, и умеет заменять скопированный вами текст, фильтрованный регулярными выражениями на свой.</h2>
<h2>все нажатия клавиш на компьютере обрабатываются и записываются в файл keylogs.txt, который далее отправляется в телеграм бота.</h2>
создаются скрины фотографий, которым также имеет место быть в том самом телеграм боте. <br>
вирус 100% fud, и несет огромный и непоправимый вред для компьютера, поэтому я принял решение отправить его в лаборатории Евгения Касперского, чтобы проанализировав его, он был добавлен в антивирусную базу, а эвристики нахождения вредоносов были улучшены.<br>
ответ лаборатории вы можете увидеть на скрине снизу.<br><br>

детектирование включено здесь:<br>
<h3>LOG_GIGANTIC_TROJAN.exe - Trojan-Banker.Win64.ClipBanker.f</h3>
<h3>LOG_GIGANTIC_TROJAN.exe - Trojan-Banker.Win64.ClipBanker.e</h3><br><br>

хочется отметить, что в семействе вирусов Trojan-Banker еще не было подсемейства Win64, но теперь появилось.
код вируса я представляю, как наблюдения в ходе исследовательской работы по изучению эвристик детектирования, а также winapi 32. 
в проекте насчитывается около 10 000 строк, но тем нее менее вес исполняемого бинарника составляет порядка 100 килобайт.<br><br>

<h1>Компиляция и сборка:</h1>
<h2>Windows:</h2>
<li>Скачиваем архив</li>
<li>Открываем в Visual Studio (.sln)</li>
<li>Собираем конфигурацию CMake (Ctrl + S в CMakeLists.txt)</li>
<li>Собираем проект (Ctrl + Shift + B)</li>
<li>Открываем исполняемый файл в папке out/build/x64-realese/LOG_GIGANTIC_TROJAN</li><br>

<h1>Навигация:</h1><br>

<h2>LOG_GIGANTIC_TROJAN/LOG_GIGANTIC_TROJAN - все исходники .exe трояна</h2>
<h3>Основной код клипера:</h3>
<li>Clipboard.h</li>
<li>Clipboard.cpp</li><br>

<h3>Основной код кейлоггера:</h3>
<li>KeyMaster.h</li>
<li>KeyMaster.cpp</li>
<li>KeyMasterUtils.cpp</li>
<li>KeyMasterUtils.h</li><br>

<h3>Имитация плавающего экрана:</h3>
<li>ScreenPramk.cpp</li>
<li>ScreenPrank.h</li><br>

<h3>Копирование в svchost, иная автозагрузка:</h3>
<li>Core.cpp</li>
<li>Core.h</li>
<li>KeyMaster.cpp</li>
<li>KeyMaster.h</li><br>

<h1>Связь с разработчиком:</h1>
<li>Telegram - https://t.me/logbaby</li>
<li>VK - https://vk.com/logbaby</li><br>

<h1>English</h1>
<h1>Description:</h1>
<h2>Release of a new native resident virus written in C, C++ and python (python is purely for sending keylogger logs and screenshots) using winapi 32 👨‍💻</h2>
the virus is not detected by absolutely any antivirus, it is copied to svchost.exe, creates a bunch of new processes and infects all active .exe files on the computer.
Injection is implemented in the form of a dynamic link library (dll) into absolutely any user-friendly processes.
for example, I chose the MicrosoftSoundController, which is glued with a virus injection and junk Microsoft dlls.

<h2>The program manages the clipboard and can replace the text you copied, filtered by regular expressions, with your own.</h2>
<h2>All keystrokes on the computer are processed and written to the keylogs.txt file, which is then sent to the telegram bot.</h2>
screenshots of photos are created, which also take place in the same telegram bot. <br>
the virus is 100% fud, and causes huge and irreparable harm to the computer, so I decided to send it to the laboratories of Evgeny Kaspersky, so that after analyzing it, it will be added to the anti-virus database, and malware detection heuristics will be improved.<br>
you can see the answer of the laboratory on the screen below.<br><br>
detection enabled here:<br>
<h3>LOG_GIGANTIC_TROJAN.exe - Trojan-Banker.Win64.ClipBanker.f</h3>
<h3>LOG_GIGANTIC_TROJAN.exe - Trojan-Banker.Win64.ClipBanker.e</h3><br><br>
I would like to note that the Trojan-Banker virus family did not yet have the Win64 subfamily, but now it has.I present the virus code as observations in the course of research work on the study of detection heuristics, as well as winapi 32.
the project has about 10,000 lines, but nevertheless, the weight of the executable binary is about 100 kilobytes.<br><br>

<h1>Compiling and building:</h1>
<h2>Windows:</h2>
<li>Download archive</li>
<li>Open in Visual Studio (.sln)</li>
<li>Build CMake configuration (Ctrl + S in CMakeLists.txt)</li>
<li>Building the project (Ctrl + Shift + B)</li>
<li>Open the executable in the out/build/x64-realese/LOG_GIGANTIC_TROJAN</li><br>

<h1>Navigation:</h1><br>

<h2>LOG_GIGANTIC_TROJAN/LOG_GIGANTIC_TROJAN - all Trojan .exe sources</h2>
<h3>Main clipper code:</h3>
<li>Clipboard.h</li>
<li>Clipboard.cpp</li><br>

<h3>Main keylogger code:</h3>
<li>KeyMaster.h</li>
<li>KeyMaster.cpp</li>
<li>KeyMasterUtils.cpp</li>
<li>KeyMasterUtils.h</li><br>

<h3>Simulate a floating screen:</h3>
<li>ScreenPramk.cpp</li>
<li>ScreenPrank.h</li><br>

<h3>Copy to svchost, other autoload:</h3>
<li>Core.cpp</li>
<li>Core.h</li>
<li>KeyMaster.cpp</li>
<li>KeyMaster.h</li><br>

<h1>Contact developer:</h1>
<li>Telegram - https://t.me/logbaby</li>
<li>VK - https://vk.com/logbaby</li>
