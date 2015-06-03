---
source: https://zan.gov.kz/client/#!/doc/91965/kaz/03.06.2015
---

# Қаржы мониторингі субъектілерінің электрондық тәсілмен берілетін ақпараттың ХМL пішімін бекіту туралы

«Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтер мен ақпарат беру қағидаларын және күдікті операцияны айқындау критерийлерінің белгілерін бекіту туралы» Қазақстан Республикасы Үкіметінің 2012 жылғы 23 қарашадағы № 1484 қаулысымен бекітілген Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтер мен ақпарат беру қағидаларының 3-тармағына сәйкес БҰЙЫРАМЫН:

1. Қоса беріліп отырған Қаржы мониторингi субъектiлерiнің электрондық тәсілмен берілетін ақпараттың XML пішімін бекіту туралы нысаны бекітілсін.

2. Қазақстан Республикасы Қаржы министрлігінің Қаржы мониторингі комитеті (Б.Ш. Тәжіяқов) заңнамада белгіленген тәртіпте:

   1) осы бұйрықты Қазақстан Республикасы Әділет министрлігінде мемлекеттік тіркеуді;

   2) осы бұйрықты мемлекеттік тіркелгеннен кейін күнтізбелік он күн ішінде оны орналастыруды мерзімді баспа басылымдарында және «Әділет» ақпараттық-құқықтық жүйесінде ресми жариялауға жіберуді;

   3) осы бұйрықты Қазақстан Республикасы Қаржы министрлігінің интернет - ресурсында орналастыруды қамтамасыз етсін.

3. Осы бұйрық 2015 жылғы 1 шілдеден бастап қолданысқа енгізіледі және ресми жариялануға жатады.

**Қазақстан Республикасының Қаржы министрі**

**Б. Сұлтанов**

> *Қазақстан Республикасы*  
> *Қаржы министрінің*  
> *2015 жылғы 3 маусымдағы*  
> *№ 345 бұйрығымен бекітілген*

# Қаржы мониторингі субъектілері электрондық тәсілмен берілетін ақпараттың XML пішімі

## 1. Жүйедегі хабарламалардың типтері

<table>
<tr>
<td>
№
р/с
</td>
<td>Жүйедегі хабарламаның типі</td>
<td>xml файлдың атауы</td>
</tr>
<tr>
<td>1</td>
<td>ФМ-1 нысаны бойынша ақпараттық хабар</td>
<td>doc</td>
</tr>
<tr>
<td>2</td>
<td>ФМ-1 нысанын қабылдау туралы хабарлама</td>
<td>Ack1</td>
</tr>
<tr>
<td>3</td>
<td>ФМ-1 нысанын қабылдамау туралы хабарлама</td>
<td>Ack2</td>
</tr>
<tr>
<td>4</td>
<td>ҚМС-ны тіркеуді сұрату</td>
<td>Registration</td>
</tr>
<tr>
<td>5</td>
<td>ҚМС-ны тіркеуді сұратуды жеткізу туралы түбіртек</td>
<td>Ack12</td>
</tr>
<tr>
<td>6</td>
<td>ҚМС-ны тіркеуге үшін сұратуды қараудың оң нәтижесі туралы хабарлама</td>
<td>Ack14</td>
</tr>
<tr>
<td>7</td>
<td>ҚМС-ны тіркеуге сұратуды қараудың теріс нәтижесі туралы хабарлама</td>
<td>Ack13</td>
</tr>
<tr>
<td>8</td>
<td>Қосымша ақпарат ұсынуға сұрау салу</td>
<td>DocInfo</td>
</tr>
<tr>
<td>9</td>
<td>Қосымша ақпарат ұсынуға сұрау салуды қабылдау туралы хабарлама</td>
<td>Ack1</td>
</tr>
<tr>
<td>10</td>
<td>Қосымша ақпарат ұсынуға сұрау салуды қабылдамау туралы хабарлама</td>
<td>Ack2</td>
</tr>
<tr>
<td>11</td>
<td>Қосымша ақпарат ұсынуға сұрау салудың жауабы</td>
<td>UponDocInfo</td>
</tr>
<tr>
<td>12</td>
<td>Қосымша ақпарат ұсынуға сұрау салудың жауабын қабылдау туралы хабарлама</td>
<td>Ack1</td>
</tr>
<tr>
<td>13</td>
<td>Қосымша ақпарат ұсынуға сұрау салудың жауабын қабылдамау туралы хабарлама</td>
<td>Ack2</td>
</tr>
</table>

Деректерді ұсыну үшін UTF-16 таңбалар кодировкасы қолданылады, рұқсат етілген таңбалар жиынынан арнайы таңбалар алынып тасталынды: &(амперсанд), <> (ашылған және жабылған жақшалар), `(апостроф).

## 2. Әртүрлі хабарламалар үшін міндетті түрде болуы тиіс тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элементтің типі</td>
<td>Элементтің сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Sender</td>
<td>
Мәтіндік жол.
Мәтіндік жол
(32 символ: A–Z символдары, 0-9 цифрлары)
</td>
<td>
Жіберуші.
1) ҚМК-не хабарламаны жіберуді орындаған ҚМС ұйымының атауы жазылған жол. Егер хабарламаны жіберуші ҚМС болса көрсетіледі..
2) «KFM» жолы. Егер хабарламаны жіберуші ҚМК болса көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Receiver</td>
<td>Мәтіндік жол (32 символ: A–Z символдары, 0-9 цифрлары)</td>
<td>
Алушы.
1) «KFM» жолы. Егер хабарламаны алушы ҚМК болса көрсетіледі.
2) ҚМС ұйымының атауы жазылған жол.
Егер хабарламаны алушы ҚМС болса көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/TimeStamp</td>
<td>DateType типі (дд.мм.гггг чч24:мм:сс түрінде көрсетіледі)</td>
<td>Құжатты жіберу уақыты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Version</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>Құжат нұсқасының GUID-ы ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматында (оналтылық санау жүйесіндегі саны. Жоғарғы тіркелімде дефистер арқылы).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/DocumentUniqueIdentifier</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>Құжат нұсқасының GUID-ы ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматында (он алтылық санау жүйесіндегі сан, жоғарғы тіркелімде дефистер арқылы).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Signature</td>
<td>base64 типіндегі жол, W3C форматында Tumar криптопровайдерінің комегімен құралған</td>
<td>Құжаттың электрондық цифрлық қолтаңбасы.</td>
</tr>
<tr>
<td>/ExportData/TransportType</td>
<td>Сан</td>
<td>Транспорт типі.</td>
</tr>
</table>

## 3. ФМ-1 нысаны бойынша ақпараттық хабарламаларды қалыптастыру үшін қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элементтің типі</td>
<td>Элементтің сипаттамасы *</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData</td>
<td></td>
<td>[2] ФМ-1 нысанын жіберген қаржы мониторингі субъектісі туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/FirstName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.7 (1)] Тегі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/SecondName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.7 (2)] Аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/MiddleName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.7 (3)] Әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/JobName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[2.7.1] Жауапты лауазымды тұлғаның қызметі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Phone</td>
<td>Қала коды / телефон нөмірі / ішкі телефонның нөмірі – форматында, телефондар үтір арқылы</td>
<td>[2.8] Байланыс телефондары</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Email</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.9] Электрондық пошта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationCode</td>
<td>Сан</td>
<td>
[2.1] Қаржы мониторингі субъектісінің коды. Ереженің** нөмірленуі және сипаттамасы
3-қосымшаға сәйкестендірілген.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationOPF</td>
<td>Сан</td>
<td>[2.2 (1.1)] Қаржы мониторингі субъектісінің ұйымдық нысаны.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Organisation</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[2.2 (1.2)] Қаржы мониторингі субъектісінің атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationArea/@Code</td>
<td>Сан</td>
<td>[2.5 (1)] Облыстың коды (ӘАОЖ анықтамалығына сәйкес)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/OrganisationCity/@Code</td>
<td>Сан</td>
<td>[2.5 (3)] Елді мекеннің коды (қала/кент/ауыл) (ӘАОЖ анықтамалығына сәйкес)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationDistrict/@Code</td>
<td>Сан</td>
<td>[2.5 (2)] Ауданның коды (ӘАОЖ анықтамалығына сәйкес)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationStreet</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.5 (4)] Көшенің/даңғылдың/шағын ауданның атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationHouse</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.5 (5)] Үйдің нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationOffice</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.5 (6)] Пәтердің/кеңсенің нөмірі (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationPostalIndex</td>
<td>Сан</td>
<td>[2.5 (7)] Пошталық индекс</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/IINBIN</td>
<td>12 цифр</td>
<td>[2.4] ЖСН/БСН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Additiona lAcData</td>
<td></td>
<td>[2.6 – 2.6.3] Жеке басын куәландыру құжаты туралы мәліметтер (жеке тұлға болып табылатын ҚМС-тер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data / Root/PersonalData/Addition alAcData/FirstName</td>
<td>Мәтіндік жол</td>
<td>[2.2 (1.2.2)] Жеке тұлға немесе дара кәсіпкер болып табылатын ҚМС-тің аты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data / Root/PersonalData/Additiona lAcData/LastName</td>
<td>Мәтіндік жол</td>
<td>[2.2 (1.2.1)] Жеке тұлға немесе дара кәсіпкер болып табылатын ҚМС-тің тегі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/Additional AcData/MiddleName</td>
<td>Мәтіндік жол</td>
<td>[2.2 (1.2.3)] Жеке тұлға немесе дара кәсіпкер болып табылатын ҚМС-тің әкесінің аты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Additional AcData/@IsAc</td>
<td>True немесе False</td>
<td>ҚМС-і есеп тапсыратын жеке тұлға болып табылатындығын көрсететін атрибут. Егер жоқ болса, онда Қағидалардың [2.6 – 2.6.3] тармақшаларына сәйкес келетін тегтер көрсетілмейді.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Additiona lAcData/DocumentIdentity</td>
<td>Сан</td>
<td>[2.6] Жеке басын куәландыратын құжат типінің коды (жеке тұлғалар үшін). Нөмірленуі және сипаттамасы Қағидалардың** 4-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Additional AcData/SeriesDocIdentity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[2.6.1 (1)] Жеке басын куәландыратын құжаттың нөмірі (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Addition alAcData/NumberDocIdentity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[2.6.1 (2)] Жеке басын куәландыратын құжаттың сериясы (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Additional AcData/DateIssuance</td>
<td>Күн (дд.мм.гггг түрінде)</td>
<td>[2.6.3] Жеке басын куәландыратын құжаттың берілген уақыты (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Additional AcData/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[2.6.2] Жеке басын куәландыратын құжатты кім берген (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation</td>
<td></td>
<td>[1] Хабарлама туралы мәлімет және [3] қаржы мониторингіне жататын операциялар туралы ақпарат.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/DocumentType</td>
<td>Сан</td>
<td>[1.3] Құжаттың түрі – Нөмірленуі және сипаттамасы Қағидалардың ** 1-қосымшасының 1.3–тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MessageNumber</td>
<td>Сан</td>
<td>[1.1(1)] ФМ-1 нысанының нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/LastModifyDate</td>
<td>Күн (dd.mm.yyyy түрінде)</td>
<td>[1.2] ФМ-1 нысанының күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/TransactionDate</td>
<td>Күн (dd.mm.yyyy hh24:mi:ss түрінде)</td>
<td>ҚМС-нің операциясының аяқталған/басталған/тоқтатылған уақыты. Егер Қағидалардың** [1.4] тармағында 4 саны белгіленсе, онда толтырылмайды.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ViewOperationId</td>
<td>Сан</td>
<td>[3.2 (1)] Операция түрінің коды – нөмірленуі және сипаттамасы Қағидалардың** 5-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/EknpId</td>
<td>Сан</td>
<td>[3.3 (1)] ТББЖ – Төлем белгілеудің бірыңғай жіктеушісінің коды. ТББЖ кодының идентификаторы көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/EknpId/ @IsEknpNotSetup</td>
<td>True немесе False</td>
<td>[3.3 (2)] ТББЖ-кодын анықтау мүмкін емес - мәні True болғанда.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ OperationNumber</td>
<td>Мәтіндік жол (30 символ)</td>
<td>[3.1] Операция нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedParticipant/ ndividualIssueData/Data/Root/ MessageInformation/ DocOperationReason</td>
<td>Сан</td>
<td>
[3.8] Операцияны жасау негіздемесі.
Нөмірленуі және сипаттамасы Қағидалардың** 6-қосымшасына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ DocOperationDate</td>
<td>Күн (dd.mm.yyyy түрінде)</td>
<td>[3.9 (1)] Операцияны жүзеге асыруға негізделген құжаттың күні.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ DocOperationNumber</td>
<td>Мәтіндік жол (30 символ)</td>
<td>[3.9 (2)] Операцияны жүзеге асыруға негізделген құжаттың нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ CurrencyCodeId</td>
<td>Сан</td>
<td>[3.5] «Кедендік декларацияларды толтыру үшін пайдаланылатын жіктеуіштер туралы» Кеден одағы комиссиясының 2010 жылғы 20 қыркүйектегі № 378 шешімімен бекітілген «Валюталар жіктеуіші» 23-қосымшасына сәйкес операция валютасының коды.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/AmountCurrency</td>
<td>Сан</td>
<td>
[3.6] Операцияны жүргізу валютасындағы сома.
Ақша форматы -99999999999999999999.99 (нүкте арқылы).
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ AmountCurrencyTenge</td>
<td>Сан</td>
<td>[3.7] Операцияның теңгедегі сомасы. Ақша форматы - 99999999999999999999.99 (нүкте арқылы).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/OperationStatusId</td>
<td>Сан</td>
<td>[1.4] Операция жай-күйі. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасының 1.4-тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ReasonFilingId</td>
<td>Сан</td>
<td>
[1.5 ] Хабарламаны жіберу негіздемесі. Нөмірленуі және сипаттамасы Қағидалардың**
1-қосымшасының
1.5-тармағына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/CounterMeasure</td>
<td></td>
<td>[1.5 ] Ұйымдар мен тұлғалардың тізбесіне сәйкес келгенде қарсы іс-қимыл шарасы. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасы 1.5-тармағының 4-тармақшасының екінші деңгейіне сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/SuspicionFirst</td>
<td>Сан</td>
<td>[3.10] Операцияның күдіктілік белгілерінің коды. Нөмірленуі және сипаттамасы Қағидаларға** 7-қосымшаға сәйкес келеді. Қағидалардың** 1-қосымшаның 1.5-деректемесінде 2-тармақ көрсетілген жағдайда деректеме толтырылуға міндетті.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/SuspicionSecond</td>
<td>Сан</td>
<td>
[3.11] Күдіктіліктің 1-қосымша белгісі. Нөмірленуі және сипаттамасы Қағидалардың**
7-қосымшасына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/SuspicionThird</td>
<td>Сан</td>
<td>
[3.12] Күдіктіліктің 2-қосымша белгісі. Нөмірленуі және сипаттамасы Қағидалардың**
7-қосымшасына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ DescriptionDifficulties</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[3.13] Операцияны күдікті ретінде жіктеуде туындаған қиындықтар сипаттамасы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ MoreInformation</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[3.14] Операция бойынша қосымша ақпарат.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ParticipantCount</td>
<td>Сан</td>
<td>[3.4] Операцияға қатысушылар саны.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MerchTypes</td>
<td>Сан</td>
<td>
[3.2 (2.1)] Мүліктің түрі. Мүлік түрінің коды:
1 – Автомобиль
2 – Пәтер
3 – Жер учаскесі
4 - Басқа
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MerchReginfo</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[3.2 (2.2)] Мүліктің тіркеу нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ReferCount</td>
<td></td>
<td>Өзге ФМ-1 нысандарымен байланыстар саны.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References</td>
<td></td>
<td>[1.1 (2)] Өзге ФМ-1 нысандарымен байланыстар туралы мәліметтер (бар болса).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference</td>
<td></td>
<td>[1.1 (2)] Өзге ФМ-1 нысанымен байланысы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference/ ReferenceId</td>
<td>Сан</td>
<td>Өзге нысанмен байланыстың реттік нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference / ReferenceOperationNumber</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[1.1 (2.1)] Байланысты ФМ-1 нысанының нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference / ReferenceDocOperationDate</td>
<td>Мәтіндік жол (dd.mm.yyyy түрінде)</td>
<td>[1.1 (2.2)] Байланысты ФМ-1 нысанының күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference /ReferenceDocOperationNumber</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Байланысты нысандағы операция нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants</td>
<td></td>
<td>[4] Қаржы мониторингіне жататын операцияға қатысушылар туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant</td>
<td></td>
<td>[4] Қаржы мониторингіне жататын операцияның қатысушысы туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/MemberId</td>
<td>Сан</td>
<td>
[4.1] Қатысушы. Нөмірленуі және сипаттамасы Қағидалардың**
1-қосымшасының 4.1-тармағына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ ParticipantsView</td>
<td>Сан</td>
<td>[4.3] Қатысушының түрі. Нөмірленуі және сипаттамасы Қағидалардың** 6-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ ParticipantsType</td>
<td>Сан</td>
<td>
[4.5] Операцияға қатысушының типі.
Нөмірленуі және сипаттамасы ҚМС мәліметтерді ұсыну Қағидаларының** 1-қосымшасының 4.5-тармағына сәйкес.
Қатысушы субъекті типіне қарай тармақтың біреуі толтырылады:
- AdditionalInformationUr – заңды тұлғалар үшін;
- AdditionalInformationAc – жеке тұлғалар үшін;
- AdditionalInformationIp – дара кәсіпкерлер үшін.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ IsClientSubject</td>
<td>Сан</td>
<td>
[4.2] Қаржы мониторингі субъектісінің клиенті. Нөмірленуі және сипаттамасы Қағидалардың**
1-қосымшасының 4.2-тармағына сәйкес. Егер ҚМС клиенті болып табылмаса, онда «1» саны көрсетіледі, егер ҚМС клиенті болып табылса, онда «2» саны көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Residence</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>
[4.4] Резиденттік. Нөмірленуі және сипаттамасы «Кедендік декларацияларды толтыру үшін қолданылатын жіктеуіштер туралы» Кеден одағы Комиссиясының 2010 жылғы
20 қыркүйектегі № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ ForeignPerson</td>
<td>Сан</td>
<td>
[4.6] Шетелдік жария лауазымды тұлға. Нөмірлеу және сипаттамасы Қағидалардың**
1-қосымшасының 4.6-тармағына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank</td>
<td></td>
<td>[4.7] Операцияға қатысушының банкі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/AccountNumber</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.7 (1.4)] Қатысушының шот нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Name</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.7 (1.2)] Банктің/филиалдың атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Code</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[4.7 (1.3)] Банктің/филиалдың коды.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/BankAddress</td>
<td></td>
<td></td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/BankCountry</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.7 (1.1)] Банк орналасқан жер. Нөмірленуі және сипаттамасы «Кедендік декларацияларды толтыру үшін қолданылатын жіктеуіштер туралы» Кеден одағы Комиссиясының 2010 жылғы 20 қыркүйектегі № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/BankCity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[4.7 (1.1)] Филиалдың орналасқан жері - Филиал Қазақстан Республикасының аумағында орналасқан жағдайда. Операцияға бастамашы болған/аяқталған елді мекен көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/BankOffshoreAddr</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>
[4.7 (1.1)] Оффшор ел, егер 3.2 &quot;Операция түрі кодының&quot; реквизиті 611-634 мәніне ие болса. Оффшорлық аймақтың сәйкестігі «Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы&quot; Қазақстан Республикасы Заңының мақсаттары үшін Оффшорлық аймақтар тізбесін бекіту туралы» Қазақстан Республикасы Қаржы министрінің м.а. 2010 жылғы 10 ақпандағы N 52 бұйрығына сәйкес көрсетіледі, нормативтік құқықтық актілерінің мемлекеттік реестрінде
N 6058 болып тіркелген.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/Participants/Participant /CorrespondentBank/@IsOffshore</td>
<td>True немесе False</td>
<td>Филиалдың оффшорлық аймақта орналасуының қосалқы белгісі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Correspon dentsInformations</td>
<td></td>
<td>[4.7 (1.5) ] Операцияға қатысушылардың корреспонденттік шоттары туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Correspon dentsInformations/Correspon dentInformation</td>
<td></td>
<td>[4.7 (1.5)] Операцияға қатысушының корреспонденттік шоты туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Correspon dentsInformations/Correspond entInformation/BankName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.7 (1.5.2)] Банктің атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Correspon dentsInformations/Correspond entInformation/BankCountry</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>
[4.7 (1.5.1)] )] Банктің орналасқан жері. Нөмірленуі және сипаттамасы «Кедендік декларацияларды толтыру үшін қолданылатын жіктеуіштер туралы» Кеден одағы Комиссиясының 2010 жылғы
20 қыркүйектегі № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/IndividualIssue</td>
<td>Мәтіндік жол (32 символ)</td>
<td>[4.13] ЖСН/БСН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/OKED</td>
<td>
Мәтіндік жол
(5 символ)
</td>
<td>
[4.12] ЭҚЖЖ. ЭҚЖЖ Қазақстан Республикасының Статистика жөніндегі агенттігі Төрағасының 2008 жылғы 20 мамырдағы № 67 бұйрығымен бекітілген «Экономикалық қызмет түрлерінің номенклатурасына
(5-таңбалы ЭҚЖЖ)» сәйкес көрсетіледі, Қазақстан Республикасы Ұлттық экономика министрлігінің Статистика комитетінің ресми сайтында орналастырылған.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/PhoneNumber</td>
<td>Қала коды/телефон нөмірі/ішкі телефонның нөмірі – форматында, телефондар үтір арқылы</td>
<td>[4.22] Байланыс телефонының нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Email</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[4.23] Электрондық пошта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalInformation</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.25] Операцияға қатысушы туралы қосымша ақпарат.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ MoneyTransSys</td>
<td>Сан</td>
<td>[4.7 (1.2.1)] Ақша аударымдары жүйесінің атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Founders</td>
<td></td>
<td>[4.9] Операцияға қатысушының құрылтайшылары (заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder</td>
<td></td>
<td>[4.9] Операцияға қатысушының құрылтайшысы (заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/FounderType</td>
<td>Сан</td>
<td>
Құрылтайшының типінің қосалқы белгісі:
1 - Заңды тұлға
2 – Жеке тұлға
3 – Дара кәсіпкер
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/FounderOPF</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.9 (1.1)] Қатысушы құрылтайшысының ұйымдық нысаны (заңды тұлға үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/Name</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.9 (2.1)] Қатысушы құрылтайшысының атауы (заңды тұлға үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/FirstName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.9 (1.2.2)] Қатысушы құрылтайшысының аты (жеке тұлғаның құрылтайшысы үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/SecondName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.9 (1.2.1)] Қатысушы құрылтайшысының тегі (жеке тұлғаның құрылтайшысы үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/MiddleName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.9 (1.2.3)] Қатысушы құрылтайшысының әкесінің аты (жеке тұлғаның құрылтайшысы үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/Residence</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.9 (2)] Операцияға қатысушы құрылтайшысының резиденттігі. Нөмірленуі және сипаттамасы «Кедендік декларацияларды толтыру үшін қолданылатын жіктеуіштер туралы» Кеден одағы Комиссиясының 2010 жылғы 20 қыркүйектегі № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo</td>
<td></td>
<td>Операцияға қатысушылар бойынша қосымша ақпарат. Заңды, жеке тұлғаларға және дара кәсіпкерлерге бөлу.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr</td>
<td></td>
<td>Қатысушы заңды тұлға бойынша қосымша ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/URAddress</td>
<td>Address құрамды тип</td>
<td>[4.21] Заңды мекенжайы. Сипаттамасы төменде құрамдас элементтер типтерінің сипаттамасында келтірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/ACAddress</td>
<td>Address құрамды тип</td>
<td>[4.24] Нақты мекенжайы. Сипаттамасы төменде құрамдас элементтер типтерінің сипаттамасында келтірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FullName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.8 (1.2)] Операцияға қатысушының атауы (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FullName/@IsFullNameSetup</td>
<td>True немесе False</td>
<td>[4.8 (2)] Операцияға қатысушының атауын анықтау мүмкін емес - True мәнінде (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead</td>
<td></td>
<td>[4.10] Бірінші басшы (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead/FirstName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.10 (2)] Бірінші басшының аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead/SecondName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.10 (1)] Бірінші басшының тегі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead/MiddleName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.10 (3)] Бірінші басшының әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/ParticipantOPF</td>
<td>Сан</td>
<td>[4.8 (1.1)] Операцияға қатысушының ұйымдық нысаны (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc</td>
<td></td>
<td>Қатысушы жеке тұлға бойынша қосымша ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/URAddress</td>
<td>Address құрамды тип</td>
<td>[4.21] Заңды мекенжайы. Сипаттамасы төменде келтірілген</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/ACAddress</td>
<td>Address құрамды тип</td>
<td>[4.24] Нақты мекенжайы. Сипаттамасы төменде келтірілген</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO</td>
<td></td>
<td>[4.14] Т.А.Ә. (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/FirstName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.2)] Аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/SecondName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.1)] Тегі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/MiddleName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.3)] Әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/@IsFioNotSetup</td>
<td>True немесе False</td>
<td>[4.14 (2.1)] Анықтау мүмкін емес - True мәнінде</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/PlaceBirth</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.20] Туған жері (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DateBirth</td>
<td>Мәтіндік жол dd.mm.yyyy түрінде</td>
<td>[4.19] Туған күні (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DocumentIdentity</td>
<td>Сан</td>
<td>[4.15] Жеке басын куәландыратын құжат. Нөмірлеу және сипаттамасы Қағидалардың** 4-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/SeriesDocIdentity</td>
<td>Мәтіндік жол (10 символ)</td>
<td>[4.16 (2)] Жеке басын куәландыратын құжаттың сериясы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/NumberDocIdentity</td>
<td>Мәтіндік жол (20 символ)</td>
<td>[4.16 (1)] Жеке басын куәландыратын құжаттың нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.17] Жеке басын куәландыратын құжатты кім берді</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DateIssuance</td>
<td>Мәтіндік жол (dd.mm.yyyy түрінде)</td>
<td>[4.18] Жеке басын куәландыратын құжат қашан берілді</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp</td>
<td></td>
<td>Дара кәсіпкер бойынша қосымша ақпарат – төменде келтірілген «ParticipantOPF» тегінен басқа, тегтерінің құрамы жеке тұлғаның тегтеріне ұқсас. Осы тег «FIO» және «PlaceBirth» тегтерінің арасында орналасқан.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/URAddress</td>
<td>Address құрамды тип</td>
<td>[4.21] Заңды мекенжайы. Сипаттамасы төменде келтірілген</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/ACAddress</td>
<td>Address құрамды тип</td>
<td>[4.24]Нақты мекен-жайы. Сипаттамасы төменде келтірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO</td>
<td></td>
<td>[4.14] Т.А.Ә. (дара кәсіпкерлер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/FirstName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.2)] Аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/SecondName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.1)] Тегі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/MiddleName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.3)] Әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/@IsFioNotSetup</td>
<td>True немесе False</td>
<td>[4.14 (2.1)] Анықтау мүмкін емес - True мәнінде</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/PlaceBirth</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.20] Туған жері (дара кәсіпкерлер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DateBirth</td>
<td>Мәтіндік жол (dd.mm.yyyy түрінде)</td>
<td>[4.19] Туған күні (дара кәсіпкерлер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DocumentIdentity</td>
<td>Сан</td>
<td>[4.15] Жеке басын куәландыратын құжат. Нөмірлеу және сиппатамасы Қағидалардың** 4-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/SeriesDocIdentity</td>
<td>Мәтіндік жол (10 символ)</td>
<td>[4.16 (2)] Жеке басын куәландыратын құжаттың сериясы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/NumberDocIdentity</td>
<td>Мәтіндік жол (20 символ)</td>
<td>[4.16 (1)] Жеке басын куәландыратын құжаттың нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.17] Жеке басын куәландыратын құжатты кім берген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DateIssuance</td>
<td>Мәтіндік жол (dd.mm.yyyy түрінде)</td>
<td>[4.18] Жеке басын куәландыратын құжат қашан берілген.</td>
</tr>
</table>

## 4. Элементтердің құрамды типтерінің сиппатамасы

<table>
<tr>
<td>Типті сәйкестендіруші</td>
<td>Жай элементтің сәйкестендірушісі</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>Address</td>
<td>Country</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>Елдің коды. Нөмірленуі және сипаттамасы «Кедендік декларацияларды толтыру үшін қолданылатын жіктеуіштер туралы» Кеден одағы Комиссиясының 2010 жылғы 20 қыркүйектегі № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
</tr>
<tr>
<td></td>
<td>Area</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Облыс</td>
</tr>
<tr>
<td></td>
<td>Area/@Code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығындағы облыс коды</td>
</tr>
<tr>
<td></td>
<td>District</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Аудан</td>
</tr>
<tr>
<td></td>
<td>District/@Code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығындағы аудан коды</td>
</tr>
<tr>
<td></td>
<td>Town</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Елді мекен</td>
</tr>
<tr>
<td></td>
<td>Town/@Code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығындағы елді мекеннің коды</td>
</tr>
<tr>
<td></td>
<td>Street</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Көше</td>
</tr>
<tr>
<td></td>
<td>HomeNumber</td>
<td>Мәтіндік жол (10 символ)</td>
<td>Үй нөмірі</td>
</tr>
<tr>
<td></td>
<td>OfficeNumber</td>
<td>Мәтіндік жол (10 символ)</td>
<td>Офис нөмірі</td>
</tr>
<tr>
<td></td>
<td>PostalCode</td>
<td>Цифрлары бар мәтіндік жол</td>
<td>Пошта индексі</td>
</tr>
</table>

## 5. ФМ-1 формасын қабылдау/қабылдамау туралы хабарламаны қалыптастыруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/Description</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Түсіндірме (хабарламаны қайта жіберу кезінде қолданылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/OriginalDocumentGuid</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегіоналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorCode</td>
<td>Сан</td>
<td>Қате коды. Қабылданбау жөнінде хабарлама кезінде 0-ден өзгеше</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorName</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Қатенің атауы/пайда болған қиындықтар</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/AcceptanceDateTime</td>
<td>Күн (dd.mm.yyyy hh24:mi:ss түрінде)</td>
<td>ФМ-1 нысанын қабылдау (қабылдамау) күні мен уақыты</td>
</tr>
</table>

## 6. ҚМС-ты тіркеу сұратуын құруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData</td>
<td></td>
<td>ҚМС, оның құрылтайшылары және жауапты тұлғалары туралы мәліметтер</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/SystemId</td>
<td>Сан</td>
<td>
Тіркелген ҚМС-тың идентификаторы. Тіркеу мәліметтерін түзету немесе өзгерту кезінде ғана қолданылады.
ҚМС-ты тіркеуді сұратуды мақұлдау туралы хабарламадағы /ExportData/SignedData/Data/Root/SystemId тегтің мәніне сәйкес болуға тиісті.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/CfmCode</td>
<td>Сан</td>
<td>Қаржы мониторингі субъектісінің коды. Нөмірлері мен сипаттамалары Қағидалардың 3-қосымшасына сәйкес. (Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.1] бөлімінде көрсетіледі)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/OpfCode</td>
<td>Сан</td>
<td>
Қаржы мониторингі субъектісінің ҰҚН коды. Нөмірлері мен сипаттамалары ұйымдық-құқықтық нысандарының жіктеушісіне сәйкес. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының
[2.2 (1.1)] бөлімінде көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/OrgName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>Қаржы мониторингі субъектісінің аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/IINBIN</td>
<td>12 цифр</td>
<td>Қаржы мониторингі субъектісінің ЖСН/БСН (Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.4] бөлімінде көрсетіледі).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/PostalIndex</td>
<td>Мәтіндік жол (30 символ)</td>
<td>Қаржы мониторингі субъектісінің пошта индексі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (7)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Area/@code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығына сәйкес облыс коды. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/District/@code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығына сәйкес аудан коды. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/City/@code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығына сәйкес елді мекен коды (қала/кент/ауыл). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (3)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Street</td>
<td>Мәтіндік жол (100 символ)</td>
<td>
Көшенің/даңғылдың/шағын ауданның атауы. Бұл мән сәтті тіркелу кезінде
ФМ-1 нысанының [2.5 (4)] бөлімінде көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/House</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Үй нөмірі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (5)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Office</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Пәтер/офис нөмірі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (6)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData</td>
<td></td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлға туралы қосымша ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/@IsAc</td>
<td>True немесе False</td>
<td>Есеп беруші қаржы мониторингі субъектісі жеке тұлға болып табылатындығын көрсететін атрибут. Егер жеке тұлға болмаса, онда /ExportData/SignedData/Data/Root/OrganisationData/AdditionalAcData тегтері көрсетілмейді.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/FirstName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлғаның аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2.2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/LastName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлғаның тегі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2.1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/MiddleName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлғаның әкесінің аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2.3)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/DocumentIdentity</td>
<td>Сан</td>
<td>
Жеке басын куәландыратын құжат түрінің коды (жеке тұлғалар үшін). Нөмірлері мен сипаттамалары Қағидалардың
4-қосымшасына сәйкес**. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6] бөлімінде көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/SeriesDocIdentity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>
Жеке басын куәландыратын құжат нөмірі (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының
[2.6.1 (1)] бөлімінде көрсетіледі.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/NumberDocIdentityы</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Жеке басын куәландыратын құжат сериясы (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.1 (2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/DateIssuance</td>
<td>Күн (дд.мм.гггг түрінде)</td>
<td>Жеке басын куәландыратын құжат қашан берілді (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.3] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>Жеке басын куәландыратын құжатты кім берді (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.2] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons</td>
<td></td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғалары туралы ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person</td>
<td></td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасы туралы ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/FirstName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7(2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/LastName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының тегі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7(1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/MiddleName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының әкесінің аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7(3)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/JobName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының лауазымы. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7.1] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/ Persons/Person/Phone</td>
<td>Мәтіндік жол (300 символ), қала коды/телефон нөмірі/ішкі телефонның нөмірі – форматында, телефондар үтір арқылы</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының телефоны. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.8] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Email</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының электрондық поштасының мекен жайы. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.8] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Certificate</td>
<td>32Кб дейін</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының ашық кілт сертификаты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Certificate/@Name</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының ашық кілт сертификатының аты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Certificate/@Size</td>
<td>Сан</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының ашық кілт сертификатының өлшемі.</td>
</tr>
</table>

## 7. ҚМС-ты тіркеуді сұратуды жеткізу туралы түбіртекті қалыптастыруда қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/Description</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Түсініктеме (түбіртекті қайтадан жібергенде қолданылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/OriginalDocumentGuid</td>
<td>
Мәтіндік жол (36 символ:
A–F символдары, 0-9 цифрлары)
</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегіоналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/MessDate</td>
<td>Күн (дд.мм.гггг чч:мм:сс түрінде)</td>
<td>Түбіртегі қалыптастырылған тіркеу сұратуын жіберу күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/MessOwn</td>
<td>Мәтіндік жол</td>
<td>Түбіртегі қалыптастырылған тіркеу сұратуын жіберуші</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorCode</td>
<td>Сан</td>
<td>Қате коды. Қабылданбау жөнінде түбіртек болған жағдайда 0-ден өзгеше</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorName</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Қатенің атауы/пайда болған қиындықтар</td>
</tr>
</table>

## 8. ҚМС-ты тіркеу сұратуын қараудың оң нәтижесі туралы хабарламанықалыптастыруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Description</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Түсініктеме (хабарламаны қайта жіберу кезінде қолданылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегі оналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessDate</td>
<td>Күн (дд.мм.гггг чч:мм:сс түрінде)</td>
<td>Хабарлама қалыптастырылған тіркеуді сұратуды жіберу күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessOwn</td>
<td></td>
<td>Хабарлама қалыптастырылған тіркеуді сұратуды жіберуші</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/SystemId</td>
<td>Сан</td>
<td>Тіркеу кезінде берілген ҚМС-тың сәйкестендірушісі</td>
</tr>
</table>

## 9. ҚМС-ты тіркеу сұратуын қараудың теріс нәтижесі туралы хабарламаны қалыптастыруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Description</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Түсініктеме (хабарламаны қайта жіберу кезінде қолданылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегі оналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessDate</td>
<td>Күн (дд.мм.гггг чч:мм:сс түрінде)</td>
<td>Хабарлама қалыптастырылған тіркеу сұратуды жіберу күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessOwn</td>
<td>Мәтіндік жол</td>
<td>Хабарлама қалыптастырылған тіркеуді сұратуды жіберуші</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ErrorCode</td>
<td>Сан</td>
<td>Қате коды. 0-ден өзгеше</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ErrorName</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Қатенің атауы/пайда болған қиындықтар</td>
</tr>
</table>

## 10. ҚМС-тен қосымша ақпаратты алуға сұратуды қалыптастыруда қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/FormNumber</td>
<td>Сан</td>
<td>Хабарлама нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркеліміндегі оналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/CountDays</td>
<td>Сан</td>
<td>Сұратуға жауап беретін күндер саны</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Description</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>ҚМС-тен қосымша ақпаратты алуды сұрату мәтіні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/RequestDateTime</td>
<td>Күні (дд.мм.гггг чч:мм:сс түрінде)</td>
<td>Сұратуды жіберу күні мен уақыты</td>
</tr>
</table>

## 11. Қосымша ақпаратқа сұрату қабылдау туралы хабарламаны қалыптастыруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/FormNumber</td>
<td>Сан</td>
<td>Хабарлама нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/OriginalDocumentGuid</td>
<td>Мәтіндік жол (32 немесе 36 символ: A–F және a-f символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегіоналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorCode</td>
<td>Сан</td>
<td>Қате коды. Қабылданбау жөнінде хабарлама болған жағдайда 0-ден өзгеше</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorName</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>Қатенің атауы/пайда болған қиындықтар</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/AcceptanceDateTime</td>
<td>Күн (dd.mm.yyyy hh24:mi:ss түрінде)</td>
<td>Сұратуды қабылдау күні мен уақыты</td>
</tr>
</table>

## 12. ҚМС-ке қосымша ақпаратты алу сұратуына жауап қалыптастыруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OriginalDocumentGuid</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегіоналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Comment</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>ҚМС-ке қосымша ақпаратты алу сұрату жауабының мәтіні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/ResponseDateTime</td>
<td>
Күн
(dd.mm.yyyy hh24:mi:ss түрінде)
</td>
<td>Жауапты жіберу күні мен уақыты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/FileName</td>
<td>Мәтіндік жол (255 символ)</td>
<td>Салынған файлдың аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/Length</td>
<td>Сан</td>
<td>Файл өлшемі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Name</td>
<td>Мәтіндік жол (255 символ)</td>
<td>Салынған файл бөлігінің аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Length</td>
<td>Сан</td>
<td>Салынған файл бөлігінің көлемі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Buffer</td>
<td>Base64 кодпен жазылған жол</td>
<td>Салынған файл бөлігінің құрамы</td>
</tr>
</table>

Ескерту:

* Нөмірленуі Қазақстан Республикасы Үкіметінің 2012 жылғы 23 қарашадағы № 1484 қаулысымен бекітілген Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтер мен ақпарат беру қағидалары 1-қосымшасының ФМ-1 нысанындағы деректемелерге сәйкес келеді.

** Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтер мен ақпарат беру қағидаларын және күдікті операцияны айқындау белгілерін бекіту туралы Қазақстан Республикасы Үкіметінің 2012 жылғы 23 қарашадағы № 1484 қаулысы.

Аббревиатуралардың мағынасын ашу:

ҚМК – Қазақстан Республикасы Қаржы министрлігінің Қаржы мониторингі комитеті;

ҚМС – Қаржы мониторингі субъектілері;

ЭЦҚ – Электрондық цифрлық қолтаңба;

ӘАОЖ – Әкімшілік-аумақтық объектілер жіктеушісі;

ТББЖ – Төлем белгілеудің бірыңғай жіктеушісі;

ҰҚН – Ұйымдық-құқықтық нысаны;

ЭҚЖЖ – Экономикалық қызметтің жалпы жіктеушісі.
