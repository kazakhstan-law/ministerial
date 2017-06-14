↑ [Вся редакция](../rus.md)

> *Приложение 8*  
> *к Правилам метеорологического*  
> *обеспечения гражданской авиации*  
> *Республики Казахстан*

## Образец для составления сообщений SIGMET и AIRMET

<table>
<tr>
<td rowspan="2">Элемент кода</td>
<td rowspan="2">Подробное содержание</td>
<td colspan="2">Формат</td>
<td rowspan="2">Примеры сообщений SIGMET</td>
<td colspan="3" rowspan="2">Примеры сообщений AIRMET</td>
</tr>
<tr>
<td>SIGMET</td>
<td>AIRMET</td>
</tr>
<tr>
<td>Указатель местоположения РПИ/СТА</td>
<td>Указатель Местоположения органа ОВД, обслужива-ющего РПИ или СТА, которого касается сообщение SIGMET/AIRMET</td>
<td>nnnn</td>
<td></td>
<td colspan="4">
UAAA
UATT
UACC
</td>
</tr>
<tr>
<td>Идентификация</td>
<td>Идентификация и порядковый номер сообщения</td>
<td>SIGMET [n][n]n</td>
<td>
AIRMET
[n][n]n
</td>
<td>
SIGMET 1
SIGMET 01
SIGMET A01
</td>
<td colspan="3">
AIRMET 9
AIRMET 19
AIRMET B19
</td>
</tr>
<tr>
<td>Период действия</td>
<td>Группа «день – время», указываю-щая период действия в UTC</td>
<td colspan="2">VALID nnnnnn/nnnnnn</td>
<td colspan="4">
VALID 101520/ 101800
VALID 251600/ 252200
VALID 152000/ 160000
</td>
</tr>
<tr>
<td>Указатель местоположе-ния</td>
<td>Указатель местоположения отправителя сообщения с разделяю-щим дефисом</td>
<td colspan="2">nnnn–</td>
<td colspan="4">
UAAA–
UATT–
UACC–
</td>
</tr>
<tr>
<td>Название РПИ/СТА</td>
<td>
Указатель местоположения и название РПИ/СТА, которому направлено сообщение SIGMET/
AIRMET
</td>
<td>
nnnn nnnnnnnnnn
FIR
или
nnnn nnnnnnnnnn
СТА
</td>
<td>
nnnn
nnnnnnnnnn
FIR[/n]
</td>
<td colspan="4">
UAAA ALMATY FIR
UATT AKTOBE СТА
UACC ASTANA FIR
</td>
</tr>
<tr>
<td>Явление</td>
<td>
Описание явления, служащего причиной выпуска SIGMET/
AIRMET
</td>
<td>
OBSC TS [GR],
EMBD TS[GR],
FRQ TS [GR],
SQL TS [GR]
TC nnnnnnnnnn PSN
Nnn [nn] или Snn[nn]
Wnnn[nn]илиEnnn[nn]
SEV TURB,
SEV ICE,
SEV ICE (FZRA)
SEV MTW
HVY DS,
HVY SS,
VA ERUPTION]
[MT] [nnnnnnnnnn]
[PSN
Nnn[nn], или Snn[nn]
Ennn[nn], или Wnnn[nn]]
VA CLD
RDOACT CLD
</td>
<td>
SFC WIND
nnn/nn[n]MPS
(или SFC WIND nnn/nn[n]KT)
SFC VIS
nnnnM(nn)
ISOL TS [GR]
OCNL TS [GR]
MT OBSC
BKN CLD
nnn/[ABV] nnnnM
(или BKN CLD nnn/[ABV](n)nnnnFT) или BKN CLD
SFC/[ABV]nnnnM
или BKN CLD
SFC[ABV] [n]nnnnFT
OVC CLD
nnn/[ABV]nnnnM
(или OVC CLD nnn/[ABV][n]nnnnFT) или OVC CLD SFC/[ABV]nnnnM (или OVC CLD SFC/[ABV][n]nnnnFT)
ISOL CB
OCNL CB
FRQ CB
ISOL TCU
OCNL TCU
FRQ TCU
MOD TURB
MOD ICE
MOD MTW
</td>
<td>
OBSC TS
OBSC TSGR
EMBD TS
EMBD TSGR
FRQ TS
FRQ TSGR
SQL TS
SQL TSGR
TC GLORIA PSN N10
W060 CB
TC NN PSN S2030
E06030 CB
SEV TURB
SEV ICE
SEV ICE (FZRA)
SEV MTW
HVY DS
HVY SS
VA ERUPTION MT ASHVAL2 PSN S15 E073
VA CLD
RDOACT CLD
</td>
<td colspan="3">
SFC WIND 040/40MPS
SFC WIND 310/20KT
SFC VIS 1500M(BR)
ISOL TS
ISOL TSGR
OCNL TS
OCNL TSGR
MT OBSC
BKN CLD 120/900M
(BKN CLD 400/3000FT)
BKN CLD SFC/3000M
BKN CLD
SFC/ABV10000FT
OVC CLD
270/ABV3000M
(OVC CLD
900/ABV10000FT)
OVC CLD SFC/3000M
OVC CLD
SFC/ABV10000FT
ISOL CB
OCNL CB
FRQ CB
ISOL TCU
OCNL TCU
FRQ TCU
MOD TURB
MOD ICE
MOD MTW
</td>
</tr>
<tr>
<td>Наблюдаемое или прогнозиру-емое явление</td>
<td>Указание о том, является ли информация данными наблюдения, и предполагается ли ее обновление или она является прогнозом</td>
<td colspan="2">
OBS [AT nnnnZ]
или
FCST [AT nnnnZ]
</td>
<td colspan="4">
OBS
OBS AT 1210Z
FCST
FCST AT 1815Z
</td>
</tr>
<tr>
<td>Местоположение</td>
<td>Местополо-жение (с указанием широты и долготы (в градусах и минутах))</td>
<td colspan="2">
Nnn[nn] Wnnn[nn] или
Nnn[nn) Ennn(nn] или
Snn[nn) Wnnn[nn] или
Snn[nn) Ennn[nn]
или
N OF Nnn[nn] или
S OF Nnn[nn] или
N OF Snn[nn] или
S OF Snn[nn];
[AND]
W OF Wnnn[nn] или
E OF Wnnn[nn] или
W OF Ennn[nn] или
E OF Ennn[nn]
или
N OF Nnn[nn] или N OF Snn[nn] AND
S OF Nnn[nn]
или
S OF Snn[nn]
или
W OF Wnnn[nn] или W OF Ennn[nn] AND E OF Wnnn[nn] или E OF Ennn[nn]
Или
N OF LINE или NE OF LINE или E OF LINE или SE OF LINE или S OF LINE или SW OF LINE или W OF LINE или NW OF LINE
Nnn[nn] или Snn[nn]Wnnn[nn] или Ennn[nn] –
Nnn[nn] или Snn[nn] Wnnn[nn], или Enn[nn] –
Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]] [–Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]]
[AND N OF LINE или NE OF LINE или E OF LINE или SE OF LINE или S OF LINE или SW OF LINE или W OF LINE или NW OF LINE
Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn] –
Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn] [–
Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]] [–
Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]]]
или
WI Nnn[nn], или Snn[nn] Wnn[nn], или Enn[nn] –
Nnn[nn], или Snn[nn] Wnn[nn], или Enn[nn]] – Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn] – [Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn] –Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]]
или
APRX nnKM WID LINE BTN (или nnNM WID LINE BTN) Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]
– Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]
[ – Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]]
[– Nnn[nn] или Snn[nn] Wnnn[nn] или Ennn[nn]
или ENTIRE FIR
или ENTIRE CTA
или
WI nnnKM (или nnnNM) OF TC CENTRE
(только для сообщений SIGMET касающихся тропических циклонов)
(N OF – севернее, NE OF–северо-восточнее, E OF – восточнее, SE OF – юго-восточнее, S OF – южнее, SW OF – юго-западнее, W OF – западнее, NW OF – северо-западнее)
</td>
<td colspan="4">
N4320 W07005
N48 E071
S54 W060
S5330 E06530
N OF N50
S OF N5430
N OF S10
S OF S4530
W OF W155
W OF E15540
E OF W45
E OF E09015
N OF N42 W OF E070
N OF N1515 AND W OF E13530
S OF N45 AND N OF N40
E OF LINE N4255 E07030-N4500 E07800
N OF LINE S2520 W11510 – S2520 W12010
SW OF LINE N50 W005 – N60 W020
SW OF LINE N50 W020 – N45 E010 AND NE OF LINE
N45 W020 – N40 E010
WI N6030 E02550 – N6055 E02500 – N6050 E02630 – N6030 E02550
APRX 50KM WID LINE BTN N64 W017 – N60 W010 –
N57 E010
ENTIRE FIR
ENTIRE CTA
WI 400KM OF TC CENTRE
WI 250NM OF TC CENTRE
</td>
</tr>
<tr>
<td>Уровень</td>
<td>Эшелон полета или абсолютная высота</td>
<td colspan="2">
[SFC/]FLnnn или
[SFC/]nnnnM(или [SFC/][n]nnnnFT) или
FLnnn/nnn или
TOP FLnnn, или
[TOP] ABV FLnnn или
[nnnn/]nnnnM (или [[n]nnnn/][n]nnnnFT) или
[nnnnM/]FLnnn (или
[[n]nnnnFT/]FLnnn)
или
TOP [ABV или BLW]FLnnn
(только для сообщений SIGMET касающихся тропических циклонов)
</td>
<td colspan="4">
FL180
SFC/FL070
SFC/3000M
SFC/10000FT
FL050/080
TOP FL390
ABV FL250
TOP ABV FL100
3000M
2000/3000M
8000FT
6000/12000FT
2000M/FL150
10000FT/FL250
TOP FL500
TOP ABV FL500
TOP BLW FL450
</td>
</tr>
<tr>
<td>Перемещение или ожидаемое перемещение</td>
<td>Перемещение или ожидаемое перемещение (направление и скорость) с указанием одного из шестнадцатикомпасных румбов или стационарное местополо-жение</td>
<td colspan="2">
MOV N [nnKMH] или MOV NNE [nnKMH] или
MOV NE [nnKMH] или MOV ENE [nnKMH] или
MOV E [nnKMH] или MOV ESE [nnKMH] или
MOV SE [nnKMH] или MOV SSE [nnKMH] или
MOV S [nnKMH] или MOV SSW [nnKMH] или
MOV SW [nnKMH] или MOV WSW [nnKMH] или
MOV W [nnKMH] или MOV WNW [nnKMH] или
MOV NW [nnKMH] или MOV NNW [nnKMH]
(или MOV N [nnKT] или MOV NNE [nnKT] или
MOV NE [nnKT] или MOV ENE [nnKT] или
MOV E [nnKT] или MOV ESE [nnKT] или
MOV SE [nnKT] или MOV SSE [nnKT] или
MOV S [nnKT] или MOV SSW [nnKT] или
MOV SW [nnKT] или MOV WSW [nnKT] или
MOV W [nnKT] или MOV WNW [nnKT] или
MOV NW [nnKT] или MOV NNW [nnKT]) или
STNR
</td>
<td colspan="4">
MOV SE
MOV NNW
MOV E 40KMH
MOV E 20KT
MOV WSW 20KT
STNR
</td>
</tr>
<tr>
<td>Изменение интенсивности</td>
<td>Ожидаемое изменение интенсив-ности</td>
<td colspan="2">
INTSF или
WKN или
NC
</td>
<td colspan="2">
INTSF
WKN
NC
</td>
<td colspan="2"></td>
</tr>
<tr>
<td>Прогнозируемое время</td>
<td>Указание прогнозиру-емого времени явления</td>
<td>FCST AT nnnnZ</td>
<td>___</td>
<td colspan="2">FCST AT 2200Z</td>
<td colspan="2">___</td>
</tr>
<tr>
<td>Прогнозируемое местоположение</td>
<td>Прогнозируемое местополо-жение явления погоды в конце периода действия сообщения SIGMET</td>
<td>
Nnn[nn] Wnnn[nn] или
Nnn[nn] Ennn[nn] или
Snn[nn] Wnnn[nn] или
Snn[nn] Ennn[nn]
или
N OF Nnn[nn] или
S OF Nnn[nn] или
N OF Snn[nn] или
S OF Snn[nn]
[AND]
W OF Wnnn[nn] или
E OF Wnnn[nn] или
W OF Ennn[nn] или
E OF Ennn[nn]
или
N OF Nnn[nn] или N OF
Snn[nn] AND S OF
Nnn[nn] или S OF
Snn[nn]
или
W OF Wnnn[nn] илиW
OF Ennn[nn] AND E OF
Wnnn[nn] или E OF
Ennn[nn]
или
N OF LINE или NE OF
LINE или E OF LINE
или SE OF LINE или S
OF LINE или SW OF
LINE или W OF LINE
или NW OF LINE
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn] –
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]
[– Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]]
[AND N OF LINE или
NE OF LINE или E OF
LINE или SE OF LINE
или S OF LINE или SW OF LINE или W OF LINE или NW OF
LINE Nnn[nn] или
Snn[nn] Wnnn[nn] или
Ennn[nn] – Nnn[nn] или
Snn[nn] Wnnn[nn] или
Ennn[nn] [– Nnn[nn] или
Snn[nn] Wnnn[nn] или
Ennn[nn]]]
или
WI Nnn[nn] или
Snn[nn] Wnnn[nn] или
Ennn[nn] –
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn] –
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn] –
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]]
или
APRX nnKM WID LINE
BTN (nnNM WID LINE BTN)
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]
– Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]
[ – Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]]
[ – Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]]
или
ENTIRE FIR
или
ENTIRE FIR[/UIR]
или
ENTIRE CTA
или
TC CENTRE PSN
Nnn[nn] или Snn[nn]
Wnnn[nn] или Ennn[nn]
(только для сообщений SIGMET касающихся тропических циклонов)
или
NO VA EXP
(только для сообщений SIGMET касающихся вулканического пепла)
</td>
<td>___</td>
<td colspan="2">
N30 W170
N OF N30
S OF S50 AND W OF E170
S OF N46 AND N OF N39
NE OF LINE N35 W020 –
N45 W040
SW OF LINE N48 W020 –
N43 E010 AND NE OF
LINE N43 W020 – N38
E010
WI N20 W090 – N05 W090
– N10 W100 – N20 W100
– N20 W090
APRX 50KM WID LINE
BTN N64 W017 – N57
W005 – N55 E010 – N55
E030
ENTIRE FIR
ENTIRE FIR/UIR
ENTIRE CTA
TC CENTRE PSN N2740
W07345
NO VA EXP
</td>
<td colspan="2"></td>
</tr>
<tr>
<td>Повторение элементов</td>
<td>Повторение элементов, включенных в сообщение SIGMET, касающееся облака вулканического пепла или тропического циклона</td>
<td>
[AND]
(используется для двух облаков вулканического пепла или двух центров тропических циклонов, находящихся одновременно в пределах РПИ)
</td>
<td>____</td>
<td colspan="2">AND</td>
<td colspan="2">____</td>
</tr>
<tr>
<td colspan="8">ИЛИ</td>
</tr>
<tr>
<td>Отмена сообщения SIGMET/ AIRMET</td>
<td>Отмена сообщения SIGMET/ AIRMET с указанием его идентификации</td>
<td>
CNL SIGMET
[n][n] n nnnnnn/nnnnnn или
CNL SIGMET
[n][n] n nnnnnn/nnnnnn
VA MOV TO nnnn FIR
</td>
<td>
CNL AIRMET
[n][n] n
nnnnnn/nnnnnn
</td>
<td colspan="3">
CNL SIGMET 2
211300/211700
CNL SIGMET A13
251030/251430
VA MOV TO
YUDO FIR
</td>
<td>
CNL AIRMET 05
151520/151800
</td>
</tr>
</table>

> *Приложение 9*  
> *к Правилам метеорологического*  
> *обеспечения гражданской авиации*  
> *Республики Казахстан*

## Примеры прогнозов погоды по маршрутам, районам полета в форме открытого текста

1. Прогноз погоды по маршруту по ПВП в форме открытого текста:

   Дата __________

   AK «Летный центр Тянь-Шань»

   ТЙН 3201 МИ 209

   БАЙСЕРКЕ – МЕЖДУРЕЧИНСКИЙ ШИЕН – ЗИМОВКА

   0600-1200 ПОЛЕ ПОВЫШЕННОГО ДАВЛЕНИЯ ВЛИЯНИЕ

   СТАЦИОНАРНОГО ФРОНТА

   ВЫСОТА УКАЗАНА НАД СР УР МОРЯ

   ПРОГНОЗ ВЕТРА/М/СЕК/ 600-1000 1500-2000 3000 4500

   И Т-РЫ ПО ВЫСОТАМ/C НСТ 05-12 НСТ 05-5 270 07-11 270 07-20

   ВЕТЕР У ЗЕМЛИ 040-13М/С ВИД 5000М ДЫМКА

   РАССЕЯНН СК 1800/3000М

   РАЗОРВАНН ВСПС УМРН ТУРБ СЛОЕ ЗЕМЛЯ/4000М

   Г/П/О Р МИН 774ММ=

   МЕЖДУРЕЧИНСКИЙ ШИЕН /ОРИЕНТИР/ 0300-0900 060-13 М/С

   ВИД 5000М ДЫМКА РАССЕЯН 0500М РАЗОРВАН 3000М=

   БАЙСЕРКЕ /ОРИЕНТИР/ 0300-0900 040 06М/С ВИД 3000М ДЫМКА

   РАССЕЯНН 0500М РАЗОРВ 3000М=

   UAAR 210200Z 2103/2112 04005MPS 3000 BR SCT030 BKN100

   TEMPO 2103/2105 0800 FZFG=

   ДЕЖУРНЫЙ СИНОПТИК ___________

   ПЕРЕДАНО _______________

   КВС________________ ВРЕМЯ_________

2. Прогнозы погоды по зонам МДП

   СЕКТОР А / Равнина /

   0900-1500 ПОЛЕ ПОВЫШЕННОГО ДАВЛЕНИЯ ВЛИЯНИЕ

   СТАЦИОНАРНОГО ФРОНТА

   ВЫСОТА УКАЗАНА НАД УР ЗЕМЛИ

   ПРОГНОЗ ВЕТРА /М/СЕК/ 600-1000 1500-2000

   И Т-РЫ ПО ВЫСОТАМ/C НСТ 05-4 НСТ 05-5

   ВИД 5000М ДЫМКА РАССЕЯНН СК 0600/3000М

   РАЗОРВАН ВСПС УМРН TУРБ СЛОЕ ЗЕМЛЯ/3000М

   Р МИН 771ММ

   НА УЧ-КЕ БАЛХАШ-САЯК РАЗОРВАН СК 0300/3000М

   Р МИН 775ММ

   СРОКЕ 1200-1500 АЛМАТЫ Р20 КМ 1000М ДЫМКА ДЫМ =

   СЕКТОР B F / Горы до 2000м /

   0900-1500 ПОЛЕ ПОВЫШЕННОГО ДАВЛЕНИЯ ВЛИЯНИЕ

   СТАЦИОНАРНОГО ФРОНТА

   ВЫСОТА УКАЗАНА НАД СР УР МОРЯ

   ПРОГНОЗ ВЕТРА/М/СЕК/ 600-1000 1500-2000 3000 4500

   И Т-РЫ ПО ВЫСОТАМ/C НСТ 05-4 НСТ 05-5 270 07-11 270 07-18

   ВИД 5000М ДЫМКА РАССЕЯНН СК 1800/3000М

   РАЗОРВАНН ВСПС

   УМРН ТУРБ СЛОЕ ЗЕМЛЯ/4000М

   Г/П/О Р МИН 771ММ

   СРОКЕ 1200-1500 АЛМАТЫ Р20 КМ 1000М ДЫМКА ДЫМ =

   СЕКТОР C D / Горы выше 2000м /

   0900-1500 ПОЛЕ ПОВЫШЕННОГО ДАВЛЕНИЯ ВЛИЯНИЕ

   СТАЦИОНАРНОГО ФРОНТА

   ВЫСОТА УКАЗАНА НАД СР УР МОРЯ

   ПРОГНОЗ ВЕТРА/М/СЕК/ 600-1000 1500-2000 3000 4500

   И Т-РЫ ПО ВЫСОТАМ/C НСТ 05-4 НСТ 05-5 270 07-11 270 07-18

   ВИД 8000М РАССЕЯНН СК 2200/3500М

   РАЗОРВАНН ВСПС УМРН ТУРБ СЛОЕ ЗЕМЛЯ/4000М

   Г/П/О Р МИН 771MМ

   СРОКЕ 1200-1500 АЛМАТЫ Р20 КМ 1000М ДЫМКА ДЫМ=

   ДЕЖУРНЫЙ СИНОПТИК _____________

3. Прогноз погоды для авиационных химических работ(АХР):

   ДАТА _________

   ККА 1211 КАЗАВИА УПЛА008

   УШАРАЛ Р - 25

   0000-0600 ПОЛЕ ПОНИЖЕННОГО ДАВЛЕНИЯ

   ВЛИЯНИЕ ХОЛОДНОГО ФРОНТА

   ВЫСОТА УКАЗАНА НАД СР УР МОРЯ

   ПРОГНОЗ ВЕТРА/М/СЕК/ 600-1000 1500-2000 3000 4500

   И Т-РЫ ПО ВЫСОТАМ/C НСТ 05+21 НСТ 05+20 240 07+11 240 10 -1

   ВЕТЕР У ЗЕМЛИ 040-10М/С ПРИ ГРОЗЕ 260-15М/С ВИД 10КМ ОЧАГИ

   ВНУТ/МАСС ГРОЗЫ РЕДК КД 1800/10000М

   РАЗОРВАН ВСПС УМЕРЕН ТУРБ СЛОЕ ЗЕМЛЯ/4000М

   НУЛЬ 4100М

   Г/П/ВЫШЕ 1800М ЗАКРЫТЫ

   Т МАХ +28 °С Т МИН +20 °С Р МИН 751 ММ=

   УШАРАЛ /ОРИЕНТ/0000-0600 240 10 М/СЕК ВИД 10 КМ

   РАССЕЯНН КД 800М ВРЕМ 0200-1000 НЕУС 15М/С ГРОЗА ШКВАЛ =

   ДЕЖУРНЫЙ СИНОПТИК ______________

   ПЕРЕДАНО ____________

> *Приложение 10*  
> *к Правилам метеорологического*  
> *обеспечения гражданской авиации*  
> *Республики Казахстан*

## Образец составления предупреждений по аэродрому на английском языке (AD WRNG)

<table>
<tr>
<td>Элемент кода</td>
<td>Подробное содержание</td>
<td>Формат</td>
<td>Пример</td>
</tr>
<tr>
<td>Указатель местоположения</td>
<td>Указатель местоположения аэродрома</td>
<td>nnnn</td>
<td>UAAA</td>
</tr>
<tr>
<td>Идентификация типа сообщения</td>
<td>Тип сообщения и порядковый номер сообщения</td>
<td>AD WRNG [n]n</td>
<td>AD WRNG 2</td>
</tr>
<tr>
<td>Срок действия</td>
<td>Дата и срок действия (в UTC)</td>
<td>VALID nnnnnn/nnnnnn</td>
<td>
VALID
210830/211230
</td>
</tr>
<tr>
<td colspan="4">Порядок отмены предупреждения по аэродрому указан в конце образца</td>
</tr>
<tr>
<td>Явление (одно явление или сочетание явлений в соответствии с п. 337 настоящих Правил)</td>
<td>Описание явления, обуславливающего выпуск предупреждения по аэродрому</td>
<td>
[HVY]TS или GR, или [HVY]SN [nnCM], или [HVY]FZRA, или [HVY]FZDZ,
RIME,
[HVY]SS, или [HVY]DS,
или SA,
или DU, или,
SFC WSPD nn[n]MPS MAXnn[n], или
(SFC WSPD nn[n]KT
MAX nn[n]), или
SFC WINDnnn/nn[n]MPS MAXnn[n], или
(SFC WIND nnn/nn[n]KT
MAX nn[n]), или
SQ, или FROST, или
VA[DEPO],
или TOX CHEM, или свободный текст до 32знаков
</td>
<td>
VRB17MPS TSSQSFC WSPD 20MPS
HVY SN 25CM
SFC WSPD 20MPS MAX30
</td>
</tr>
<tr>
<td>Наблюдаемое или прогнозируемое явление</td>
<td>Указание о том, является ли эта информация данными наблюдения и предполагается ли ее обновление или она является прогнозом</td>
<td>OBS [ATnnnnZ], или FCST</td>
<td>
OBS AT1200Z
FCST
</td>
</tr>
<tr>
<td>Изменение интенсивности</td>
<td>Ожидаемое изменение интенсивности</td>
<td>INTSF, или WKN, или NC</td>
<td>INTSF, WKN, NC</td>
</tr>
<tr>
<td colspan="4">или</td>
</tr>
<tr>
<td>Отмена предупреждения по аэродрому</td>
<td>Отмена предупреждения по аэродрому с указанием его идентификации</td>
<td>
CNL AD WRNG [n]
nnnnnnn/nnnnnn
</td>
<td>CNLAD WRNG 2 210800/211200</td>
</tr>
<tr>
<td colspan="4">
Пример:
UAAA AD WRNG 2 VALID 211000/211400 - HVY SN 25CM
FCST NC=
Алматы предупреждение по аэродрому номер 2, действительно 21 числа с 10.00UTC до 14.00 UTC: прогнозируется сильный снег высота отложения
25 сантиметров, интенсивность без изменения.
</td>
</tr>
</table>

> *Приложение 11*  
> *к Правилам метеорологического*  
> *обеспечения гражданской авиации*  
> *Республики Казахстан*

## Образец составления предупреждений и оповещений о сдвиге ветра на аэродроме на английском языке (WS WRNG)

<table>
<tr>
<td>Элемент кода</td>
<td>Подробное содержание</td>
<td>Формат (ы)</td>
<td>Пример (ы)</td>
</tr>
<tr>
<td>Указатель местоположения</td>
<td>Указатель местоположения аэродрома</td>
<td>nnnn</td>
<td>UAAA</td>
</tr>
<tr>
<td>Идентификация типа сообщения</td>
<td>Тип сообщения и порядковый номер</td>
<td>WS WRNG [n] n</td>
<td>WS WRNG 1</td>
</tr>
<tr>
<td>Время составления и период действия</td>
<td>Дата и время выпуска и, когда применимо, срок действия в UTC</td>
<td>nnnnnn [VALID TL nnnnnn] или [VALID nnnnnn/nnnnnn]</td>
<td>
211230 VALID TL 211330
221200 VALID 221215/221315
</td>
</tr>
<tr>
<td colspan="4">Порядок отмены предупреждения и оповещения о сдвиге ветра указан в конце образца</td>
</tr>
<tr>
<td>Явление</td>
<td>Идентификация явления и его местоположение</td>
<td>
(MOD) или (SEV) WS IN APCH; или
(MOD) или (SEV) WS (APCH) RWYnnn, или (MOD), или (SEV) WS IN CLIMB-OUT, или
(MOD), или (SEV) WS CLIMB-OUT, (RWYnnn), или
MBST IN APCH, или
MBST[APCH]RWYnnn,
или
MBST IN CLIMB-OUT, или MBST CLIMB-OUT RWYnnn
</td>
<td>
WS IN APCH RWY05,
MOD WS RWY23,
WS IN CLIMB-OUT,
SEV WS IN CLIMB-OUT,
MBST APCH RWY05,
MBST IN CLIMB-OUT
</td>
</tr>
<tr>
<td>Наблюдаемое, cообщаемое или прогнозируемое явление</td>
<td>Указание о том, наблюдается ли явление, или о нем сообщается и ожидается его продолжение, или оно прогнозируется</td>
<td>
REP AT nnn nnnnnnnn, или OBS (AT nnnn), или
FCST
</td>
<td>
REP AT 1510 B747
OBS AT 1205
FCST
</td>
</tr>
<tr>
<td>Подробная информация о явлении</td>
<td>Описание явления, служащего причиной выпуска предупреждения о сдвиге ветра</td>
<td>
SFC WIND: nnn/nnMPS
nnnM -WIND: nnn/nnMPS
(или nnn/nnKT),
или
nnKMH (или nnKT) LOSS nnKM (или nnNM) FNA RWYnn
или
nnKMH (или nnKT) GAIN nnKM (или nnNM) FNA RWYnn
</td>
<td>
SFC WIND: 320/05MРS
60M- WIND: 360/13MРS
(SFC WIND: 320/10KT
200FT-WIND: 360/26KT)
60KMH LOSS 4KM
FNA RWY13
(30KT LOSS 2NM
FNA RWY13
</td>
</tr>
<tr>
<td colspan="4">Или</td>
</tr>
<tr>
<td>Отмена Предупреждения о сдвиге ветра</td>
<td>Отмена предупреждения о сдвиге ветра с указанием его идентификации</td>
<td>
CNL WS WRNG n
nnnnnn/nnnnnn
</td>
<td>
CNL WS WRNG 1
211230/211330
</td>
</tr>
<tr>
<td colspan="4">
Пример:
UAAA WS WRNG 1 211130 VALID 211230/211330- SEV WS IN CLIMB-OUT FCST
Алматы предупреждение о сдвиге ветра номер 1, выпущено 21 числа в 11.30 UTC, действительно с 12.30 UTC до 13.30 UTC сильный сдвиг ветра прогнозируется при наборе высоты.
</td>
</tr>
</table>

> *Приложение 12*  
> *к Правилам метеорологического*  
> *обеспечения гражданской авиации*  
> *Республики Казахстан*

## Порядок распространения авиационных метеорологических прогнозов, предупреждений, включая информацию SIGMET и AIRMET, и консультативную информацию о вулканическом пепле и тропическом циклоне

<table>
<tr>
<td>Тип прогноза</td>
<td>Зона/воздушное пространство прогнозирования</td>
<td>Этап планирования полетов</td>
<td>Ответственность за подготовку/выпуск прогноза</td>
</tr>
<tr>
<td>TAF</td>
<td>Аэродром</td>
<td>Предполетный и в полете</td>
<td>АМО</td>
</tr>
<tr>
<td>Прогноз для посадки («тренд»)</td>
<td>Аэродром</td>
<td>В полете</td>
<td>АМО</td>
</tr>
<tr>
<td>Прогноз для взлета</td>
<td>Комплекс ВПП</td>
<td>Предполетный</td>
<td>АМО</td>
</tr>
<tr>
<td>Прогнозы особых явлений погоды, прогнозы ветра и температуры на высотах и др. прогнозы ВЦЗП</td>
<td>Маршрут(ы) зона(ы) или эшелоны, используемые для производства полетов</td>
<td>Предполетный и в полете</td>
<td>ВЦЗП</td>
</tr>
<tr>
<td>Прогнозы условий погоды по маршрутам и районам полетов на малых эшелонах</td>
<td>Маршрут(ы) зона(ы) или эшелоны, используемые для производства полетов в слое от поверхности земли до ЭП 100 (до ЭП 150 или выше в горных районах)</td>
<td>Предполетный и в полете</td>
<td>АМО</td>
</tr>
<tr>
<td>Информация SIGMET</td>
<td>РПИ или диспетчерский район (CTA)/охватываются все эшелоны, используемые для производства полетов</td>
<td>Предполетный и в полете</td>
<td>ОМС</td>
</tr>
<tr>
<td>Информация AIRMET</td>
<td>РПИ или диспетчерская зона или ее подзона/охватываются все эшелоны полета до ЭП 100 (ЭП 150 или выше в горных районах)</td>
<td>Предполетный и в полете</td>
<td>ОМС</td>
</tr>
<tr>
<td>Предупреждения по аэродрому</td>
<td>Аэродром/приземные метеорологические условия</td>
<td>Неприменимо (предназначено для воздушных судов, находящихся на стоянке, аэродромных сооружений)</td>
<td>АМО</td>
</tr>
<tr>
<td>Предупреждения о сдвиге ветра</td>
<td>Аэродром и маршруты захода на посадку/взлета между уровнем ВПП и 500 м (1600 фут) или при необходимости выше</td>
<td>В полете</td>
<td>АМО</td>
</tr>
<tr>
<td>Консультативная информация по вулканическому пеплу</td>
<td>Зона охваченная облаком вулканического пепла</td>
<td>Предполетный и в полете</td>
<td>VAAC</td>
</tr>
<tr>
<td>Консультативная информация по тропическим циклонам</td>
<td>Зона охваченная тропическим циклоном</td>
<td>Предполетный и в полете</td>
<td>TCAC</td>
</tr>
</table>
