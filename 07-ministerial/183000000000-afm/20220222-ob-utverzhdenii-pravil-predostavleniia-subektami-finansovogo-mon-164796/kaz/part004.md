---
part_of: ../kaz.md
source: https://zan.gov.kz/client/#!/doc/164796/kaz/10.07.2025
---

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтер мен ақпарат беру қағидаларына*  
> *2-қосымша*

## Қаржы мониторингі субъектілері электрондық тәсілмен берілетін ақпараттың XML пішімі

### 1. Жүйедегі хабарламалардың типтері

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
<td>Қаржы мониторингі субъектінің (бұдан әрі- ҚМС) тіркеуін сұрату</td>
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

### 2. Әртүрлі хабарламалар үшін міндетті түрде болуы тиіс тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элементтің типі</td>
<td>Элементтің сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Sender</td>
<td>Мәтіндік жол. Мәтіндік жол (32 символ: A–Z символдары, 0-9 цифрлары)</td>
<td>Жіберуші. 1) ҚМA-не хабарламаны жіберуді орындаған ҚМС ұйымының атауы жазылған жол. Егер хабарламаны жіберуші ҚМС болса көрсетіледі.. 2) «AFM» жолы. Егер хабарламаны жіберуші ҚМA болса көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Receiver</td>
<td>Мәтіндік жол (32 символ: A–Z символдары, 0-9 цифрлары)</td>
<td>Алушы. 1) «AFM» жолы. Егер хабарламаны алушы ҚМA болса көрсетіледі. 2) ҚМС ұйымының атауы жазылған жол. Егер хабарламаны алушы ҚМС болса көрсетіледі.</td>
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

### 3. ФМ-1 нысаны бойынша ақпараттық хабарламаларды қалыптастыру үшін қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элементтің типі</td>
<td>Элементтің сипаттамасы *</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData</td>
<td></td>
<td>[2] ФМ-1 нысанын жіберген қаржы мониторингі субъектісі туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ FirstName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.7 (1)] Тегі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ SecondName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.7 (2)] Аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ MiddleName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.7 (3)] Әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ JobName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[2.7.1] Жауапты лауазымды тұлғаның қызметі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ Phone</td>
<td>Қала коды / телефон нөмірі / ішкі телефонның нөмірі – форматында, телефондар үтір арқылы</td>
<td>[2.8] Байланыс телефондары</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ Email</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.9] Электрондық пошта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationCode</td>
<td>Сан</td>
<td>[2.1] Қаржы мониторингі субъектісінің коды. Ереженің** нөмірленуі және сипаттамасы 3-қосымшаға сәйкестендірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationOPF</td>
<td>Сан</td>
<td>[2.2 (1.1)] Қаржы мониторингі субъектісінің ұйымдық нысаны.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ Organisation</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[2.2 (1.2)] Қаржы мониторингі субъектісінің атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationArea/@Code</td>
<td>Сан</td>
<td>[2.5 (1)] Облыстың коды (ӘАОЖ анықтамалығына сәйкес)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationCity/@Code</td>
<td>Сан</td>
<td>[2.5 (3)] Елді мекеннің коды (қала/кент/ауыл) (ӘАОЖ анықтамалығына сәйкес)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationDistrict/@Code</td>
<td>Сан</td>
<td>[2.5 (2)] Ауданның коды (ӘАОЖ анықтамалығына сәйкес)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationStreet</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.5 (4)] Көшенің/даңғылдың/шағын ауданның атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationHouse</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.5 (5)] Үйдің нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationOffice</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[2.5 (6)] Пәтердің/кеңсенің нөмірі (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationPostalIndex</td>
<td>Сан</td>
<td>[2.5 (7)] Пошталық индекс</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ IINBIN</td>
<td>12 цифр</td>
<td>[2.4] ЖСН/БСН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData</td>
<td></td>
<td>[2.6 – 2.6.3] Жеке басын куәландыру құжаты туралы мәліметтер (жеке тұлға болып табылатын ҚМС-тер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/ AdditionalAcData/FirstName</td>
<td>Мәтіндік жол</td>
<td>[2.2 (1.2.2)] Жеке тұлға немесе дара кәсіпкер болып табылатын ҚМС-тің аты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/ AdditionalAcData/LastName</td>
<td>Мәтіндік жол</td>
<td>[2.2 (1.2.1)] Жеке тұлға немесе дара кәсіпкер болып табылатын ҚМС-тің тегі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/AdditionalAcData/MiddleName</td>
<td>Мәтіндік жол</td>
<td>[2.2 (1.2.3)] Жеке тұлға немесе дара кәсіпкер болып табылатын ҚМС-тің әкесінің аты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData/@IsAc</td>
<td>True немесе False</td>
<td>ҚМС-і есеп тапсыратын жеке тұлға болып табылатындығын көрсететін атрибут. Егер жоқ болса, онда Қағидалардың [2.6–2.6.3] тармақшаларына сәйкес келетін тегтер көрсетілмейді.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData/DocumentIdentity</td>
<td>Сан</td>
<td>[2.6] Жеке басын куәландыратын құжат типінің коды (жеке тұлғалар үшін). Нөмірленуі және сипаттамасы Қағидалардың** 4-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData/SeriesDocIdentity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[2.6.1 (1)] Жеке басын куәландыратын құжаттың нөмірі (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData/NumberDocIdentity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[2.6.1 (2)] Жеке басын куәландыратын құжаттың сериясы (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData/DateIssuance</td>
<td>Күн (дд.мм.гггг түрінде)</td>
<td>[2.6.3] Жеке басын куәландыратын құжаттың берілген уақыты (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[2.6.2] Жеке басын куәландыратын құжатты кім берген (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation</td>
<td></td>
<td>[1] Хабарлама туралы мәлімет және [3] қаржы мониторингіне жататын операциялар туралы ақпарат.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ DocumentType</td>
<td>Сан</td>
<td>[1.3] Құжаттың түрі – Нөмірленуі және сипаттамасы Қағидалардың ** 1-қосымшасының 1.3–тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ MessageNumber</td>
<td>Сан</td>
<td>[1.1(1)] ФМ-1 нысанының нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ LastModifyDate</td>
<td>Күн (dd.​mm.​yyyy түрінде)</td>
<td>[1.2] ФМ-1 нысанының күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ TransactionDate</td>
<td>Күн (dd.​mm.​yyyy hh24:mi:ss түрінде)</td>
<td>ҚМС-нің операциясының аяқталған/басталған/тоқтатылған уақыты. Егер Қағидалардың** [1.4] тармағында 4 саны белгіленсе, онда толтырылмайды.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ ViewOperationId</td>
<td>Сан</td>
<td>[3.2 (1)] Операция түрінің коды – нөмірленуі және сипаттамасы Қағидалардың** 5-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ EknpId</td>
<td>Сан</td>
<td>[3.3 (1)] ТББЖ – Төлем белгілеудің бірыңғай жіктеушісінің коды. ТББЖ кодының идентификаторы көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ EknpId/@IsEknpNotSetup</td>
<td>True немесе False</td>
<td>[3.3 (2)] ТББЖ-кодын анықтау мүмкін емес - мәні True болғанда.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ OperationNumber</td>
<td>Мәтіндік жол (30 символ)</td>
<td>[3.1] Операция нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedParticipant/IndividualIssueData/Data/ Root/MessageInformation/ DocOperationReason</td>
<td>Сан</td>
<td>
[3.8] Операцияны жасау негіздемесі.
Нөмірленуі және сипаттамасы Қағидалардың** 6-қосымшасына сәйкес.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ DocOperationDate</td>
<td>Күн (dd.​mm.​yyyy түрінде)</td>
<td>[3.9 (1)] Операцияны жүзеге асыруға негізделген құжаттың күні.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ DocOperationNumber</td>
<td>Мәтіндік жол (30 символ)</td>
<td>[3.9 (2)] Операцияны жүзеге асыруға негізделген құжаттың нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ CurrencyCodeId</td>
<td>Сан</td>
<td>[3.5] КОК-тың № 378 шешімімен бекітілген «Валюталар жіктеуіші» 23-қосымшасына сәйкес операция валютасының коды.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ AmountCurrency</td>
<td>Сан</td>
<td>[3.6] Операцияны жүргізу валютасындағы сома. Ақша форматы -99999999999999999999.99 (нүкте арқылы).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ AmountCurrencyTenge</td>
<td>Сан</td>
<td>[3.7] Операцияның теңгедегі сомасы. Ақша форматы - 99999999999999999999.99 (нүкте арқылы).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ OperationStatusId</td>
<td>Сан</td>
<td>[1.4] Операция жай-күйі. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасының 1.4-тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ ReasonFilingId</td>
<td>Сан</td>
<td>[1.5] Хабарламаны жіберу негіздемесі. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасының 1.5-тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ CounterMeasure</td>
<td></td>
<td>[1.5] Ұйымдар мен тұлғалардың тізбесіне сәйкес келгенде қарсы іс-қимыл шарасы. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасы 1.5-тармағының 4-тармақшасының екінші деңгейіне сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ SuspicionFirst</td>
<td>Сан</td>
<td>[3.10] Операцияның күдіктілік белгілерінің коды. Нөмірленуі және сипаттамасы Қағидаларға** 7-қосымшаға сәйкес келеді. Қағидалардың** 1-қосымшаның 1.5-деректемесінде 2-тармақ көрсетілген жағдайда деректеме толтырылуға міндетті.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ SuspicionSecond</td>
<td>Сан</td>
<td>[3.11] Күдіктіліктің 1-қосымша белгісі. Нөмірленуі және сипаттамасы Қағидалардың** 7-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ SuspicionThird</td>
<td>Сан</td>
<td>[3.12] Күдіктіліктің 2-қосымша белгісі. Нөмірленуі және сипаттамасы Қағидалардың** 7-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ DescriptionDifficulties</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[3.13] Операцияны күдікті ретінде жіктеуде туындаған қиындықтар сипаттамасы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ MoreInformation</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[3.14] Операция бойынша қосымша ақпарат.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ ParticipantCount</td>
<td>Сан</td>
<td>[3.4] Операцияға қатысушылар саны.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ MerchTypes</td>
<td>Сан</td>
<td>[3.2 (2.1)] Мүліктің түрі. Мүлік түрінің коды: 1 – Автомобиль 2 – Пәтер 3 – Жер учаскесі 4 - Басқа</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ MerchReginfo</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[3.2 (2.2)] Мүліктің тіркеу нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessageInformation/ ReferCount</td>
<td></td>
<td>Өзге ФМ-1 нысандарымен байланыстар саны.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/References</td>
<td></td>
<td>[1.1 (2)] Өзге ФМ-1 нысандарымен байланыстар туралы мәліметтер (бар болса).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/References/Reference</td>
<td></td>
<td>[1.1 (2)] Өзге ФМ-1 нысанымен байланысы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/References/Reference/ ReferenceId</td>
<td>Сан</td>
<td>Өзге нысанмен байланыстың реттік нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/References/Reference /ReferenceOperationNumber</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[1.1 (2.1)] Байланысты ФМ-1 нысанының нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/References/Reference /ReferenceDocOperationDate</td>
<td>Мәтіндік жол (dd.​mm.​yyyy түрінде)</td>
<td>[1.1 (2.2)] Байланысты ФМ-1 нысанының күні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/References/Reference /ReferenceDocOperationNumber</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Байланысты нысандағы операция нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants</td>
<td></td>
<td>[4] Қаржы мониторингіне жататын операцияға қатысушылар туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant</td>
<td></td>
<td>[4] Қаржы мониторингіне жататын операцияның қатысушысы туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ MemberId</td>
<td>Сан</td>
<td>[4.1] Қатысушы. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасының 4.1-тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ ParticipantsView</td>
<td>Сан</td>
<td>[4.3] Қатысушының түрі. Нөмірленуі және сипаттамасы Қағидалардың** 6-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ ParticipantsType</td>
<td>Сан</td>
<td>[4.5] Операцияға қатысушының типі. Нөмірленуі және сипаттамасы ҚМС мәліметтерді ұсыну Қағидаларының** 1-қосымшасының 4.5-тармағына сәйкес. Қатысушы субъекті типіне қарай тармақтың біреуі толтырылады: - AdditionalInformationUr – заңды тұлғалар үшін; - AdditionalInformationAc – жеке тұлғалар үшін; - AdditionalInformationIp – дара кәсіпкерлер үшін.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ IsClientSubject</td>
<td>Сан</td>
<td>[4.2] Қаржы мониторингі субъектісінің клиенті. Нөмірленуі және сипаттамасы Қағидалардың** 1-қосымшасының 4.2-тармағына сәйкес. Егер ҚМС клиенті болып табылмаса, онда «1» саны көрсетіледі, егер ҚМС клиенті болып табылса, онда «2» саны көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Residence</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.4] Резиденттік. Нөмірленуі және сипаттамасы КОК-тың № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ ForeignPerson</td>
<td>Сан</td>
<td>[4.6] Шетелдік жария лауазымды тұлға. Нөмірлеу және сипаттамасы Қағидалардың** 1-қосымшасының 4.6-тармағына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank</td>
<td></td>
<td>[4.7] Операцияға қатысушының банкі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/AccountNumber</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.7 (1.4)] Қатысушының шот нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/Name</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.7 (1.2)] Банктің/филиалдың атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/Code</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[4.7 (1.3)] Банктің/филиалдың коды.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/BankAddress</td>
<td></td>
<td></td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/BankCountry</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.7 (1.1)] Оффшор ел, егер 3.2 «Операция түрінің коды» деректемесі 611-634 мәніне ие болса. Оффшорлық аймақтың сәйкестігі «Банктік және сақтандыру қызметінің, бағалы қағаздар рыногының кәсіби қатысушылары қызметінің және бағалы қағаздар рыногында лицензияланатын басқа да қызмет түрлерінің, акционерлік инвестициялық қорлар және микроқаржылық қызметті жүзеге асыратын ұйымдар қызметінің мақсаттары үшін офшорлық аймақтардың тізбесін белгілеу туралы» Қазақстан Республикасының Қаржы нарығын реттеу және дамыту агенттігі Басқармасының 2020 жылғы 24 ақпандағы № 8 қаулысына сәйкес көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/BankCity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>[4.7 (1.1)] Филиалдың орналасқан жері - Филиал Қазақстан Республикасының аумағында орналасқан жағдайда. Операцияға бастамашы болған/аяқталған елді мекен көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/BankOffshoreAddr</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.7 (1.1)] Оффшор ел, егер 3.2 &quot;Операция түрі кодының&quot; реквизиті 611-634 мәніне ие болса. Оффшорлық аймақтың сәйкестігі «Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы&quot; Қазақстан Республикасы Заңының мақсаттары үшін Оффшорлық аймақтар тізбесін бекіту туралы» Қазақстан Республикасы Қаржы министрінің м.а. 2010 жылғы 10 ақпандағы N 52 бұйрығына сәйкес көрсетіледі, нормативтік құқықтық актілерінің мемлекеттік реестрінде N 6058 болып тіркелген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/@IsOffshore</td>
<td>True немесе False</td>
<td>Филиалдың оффшорлық аймақта орналасуының қосалқы белгісі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/CorrespondentsInformations</td>
<td></td>
<td>[4.7 (1.5)] Операцияға қатысушылардың корреспонденттік шоттары туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/ CorrespondentsInformations/ CorrespondentInformation</td>
<td></td>
<td>[4.7 (1.5)] Операцияға қатысушының корреспонденттік шоты туралы мәліметтер.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/ CorrespondentsInformations/CorrespondentInformation/ BankName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.7 (1.5.2)] Банктің атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ CorrespondentBank/ CorrespondentsInformations/CorrespondentInformation/ BankCountry</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.7 (1.5.1)] )] Банктің орналасқан жері. Нөмірленуі және сипаттамасы КОК-тың № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ IndividualIssue</td>
<td>Мәтіндік жол (32 символ)</td>
<td>[4.13] ЖСН/БСН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ OKED</td>
<td>Мәтіндік жол (5 символ)</td>
<td>[4.12] ЭҚЖЖ. ЭҚЖЖ Қазақстан Республикасының Статистика жөніндегі агенттігі Төрағасының 2008 жылғы 20 мамырдағы № 67 бұйрығымен бекітілген «Экономикалық қызмет түрлерінің номенклатурасына (5-таңбалы ЭҚЖЖ)» сәйкес көрсетіледі, Қазақстан Республикасы Ұлттық экономика министрлігінің Статистика комитетінің ресми сайтында орналастырылған.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ PhoneNumber</td>
<td>Қала коды/телефон нөмірі/ішкі телефонның нөмірі – форматында, телефондар үтір арқылы</td>
<td>[4.22] Байланыс телефонының нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Email</td>
<td>Мәтіндік жол (100 символ)</td>
<td>[4.23] Электрондық пошта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalInformation</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.25] Операцияға қатысушы туралы қосымша ақпарат.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ MoneyTransSys</td>
<td>Сан</td>
<td>[4.7 (1.2.1)] Ақша аударымдары жүйесінің атауы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders</td>
<td></td>
<td>[4.9] Операцияға қатысушының құрылтайшылары (заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/Founder</td>
<td></td>
<td>[4.9] Операцияға қатысушының құрылтайшысы (заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/FounderType</td>
<td>Сан</td>
<td>Құрылтайшының типінің қосалқы белгісі: 1 - Заңды тұлға 2 – Жеке тұлға 3 – Дара кәсіпкер</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/FounderOPF</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.9 (1.1)] Қатысушы құрылтайшысының ұйымдық нысаны (заңды тұлға үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/Name</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.9 (2.1)] Қатысушы құрылтайшысының атауы (заңды тұлға үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/FirstName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.9 (1.2.2)] Қатысушы құрылтайшысының аты (жеке тұлғаның құрылтайшысы үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/SecondName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.9 (1.2.1)] Қатысушы құрылтайшысының тегі (жеке тұлғаның құрылтайшысы үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/MiddleName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.9 (1.2.3)] Қатысушы құрылтайшысының әкесінің аты (жеке тұлғаның құрылтайшысы үшін толтырылады)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ Founders/ Founder/Residence</td>
<td>Мәтіндік жол (2 символ) (елдің символдық коды)</td>
<td>[4.9 (2)] Операцияға қатысушы құрылтайшысының резиденттігі. Нөмірленуі және сипаттамасы Кок-тың № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo</td>
<td></td>
<td>Операцияға қатысушылар бойынша қосымша ақпарат. Заңды, жеке тұлғаларға және дара кәсіпкерлерге бөлу.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr</td>
<td></td>
<td>Қатысушы заңды тұлға бойынша қосымша ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/URAddress</td>
<td>Address құрамды тип</td>
<td>[4.21] Заңды мекенжайы. Сипаттамасы төменде құрамдас элементтер типтерінің сипаттамасында келтірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/ACAddress</td>
<td>Address құрамды тип</td>
<td>[4.24] Нақты мекенжайы. Сипаттамасы төменде құрамдас элементтер типтерінің сипаттамасында келтірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/FullName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.8 (1.2)] Операцияға қатысушының атауы (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/FullName/@IsFullNameSetup</td>
<td>True немесе False</td>
<td>[4.8 (2)] Операцияға қатысушының атауын анықтау мүмкін емес - True мәнінде (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/FirstHead</td>
<td></td>
<td>[4.10] Бірінші басшы (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/FirstHead/FirstName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.10 (2)] Бірінші басшының аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/FirstHead/SecondName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.10 (1)] Бірінші басшының тегі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/FirstHead/MiddleName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.10 (3)] Бірінші басшының әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationUr/ParticipantOPF</td>
<td>Сан</td>
<td>[4.8 (1.1)] Операцияға қатысушының ұйымдық нысаны (қатысушы заңды тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc</td>
<td></td>
<td>Қатысушы жеке тұлға бойынша қосымша ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/URAddress</td>
<td>Address құрамды тип</td>
<td>[4.21] Заңды мекенжайы. Сипаттамасы төменде келтірілген</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/ACAddress</td>
<td>Address құрамды тип</td>
<td>[4.24] Нақты мекенжайы. Сипаттамасы төменде келтірілген</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/FIO</td>
<td></td>
<td>[4.14] Т.А.Ә. (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/FIO/FirstName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.2)] Аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/FIO/SecondName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.1)] Тегі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/FIO/MiddleName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.3)] Әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/FIO/@IsFioNotSetup</td>
<td>True немесе False</td>
<td>[4.14 (2.1)] Анықтау мүмкін емес - True мәнінде</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/PlaceBirth</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.20] Туған жері (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/DateBirth</td>
<td>Мәтіндік жол dd.​mm.​yyyy түрінде</td>
<td>[4.19] Туған күні (жеке тұлғалар үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/DocumentIdentity</td>
<td>Сан</td>
<td>[4.15] Жеке басын куәландыратын құжат. Нөмірлеу және сипаттамасы Қағидалардың** 4-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/SeriesDocIdentity</td>
<td>Мәтіндік жол (10 символ)</td>
<td>[4.16 (2)] Жеке басын куәландыратын құжаттың сериясы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/NumberDocIdentity</td>
<td>Мәтіндік жол (20 символ)</td>
<td>[4.16 (1)] Жеке басын куәландыратын құжаттың нөмірі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.17] Жеке басын куәландыратын құжатты кім берді</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationAc/DateIssuance</td>
<td>Мәтіндік жол (dd.​mm.​yyyy түрінде)</td>
<td>[4.18] Жеке басын куәландыратын құжат қашан берілді</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp</td>
<td></td>
<td>Дара кәсіпкер бойынша қосымша ақпарат – төменде келтірілген «ParticipantOPF» тегінен басқа, тегтерінің құрамы жеке тұлғаның тегтеріне ұқсас. Осы тег «FIO» және «PlaceBirth» тегтерінің арасында орналасқан.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/URAddress</td>
<td>Address құрамды тип</td>
<td>[4.21] Заңды мекенжайы. Сипаттамасы төменде келтірілген</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/ACAddress</td>
<td>Address құрамды тип</td>
<td>[4.24]Нақты мекен-жайы. Сипаттамасы төменде келтірілген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO</td>
<td></td>
<td>[4.14] Т.А.Ә. (дара кәсіпкерлер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO/FirstName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.2)] Аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO/SecondName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.1)] Тегі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO/MiddleName</td>
<td>Мәтіндік жол (1000 символ)</td>
<td>[4.14 (1.3)] Әкесінің аты (бар болса)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO/@IsFioNotSetup</td>
<td>True немесе False</td>
<td>[4.14 (2.1)] Анықтау мүмкін емес - True мәнінде</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/PlaceBirth</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.20] Туған жері (дара кәсіпкерлер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/DateBirth</td>
<td>Мәтіндік жол (dd.​mm.​yyyy түрінде)</td>
<td>[4.19] Туған күні (дара кәсіпкерлер үшін)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/DocumentIdentity</td>
<td>Сан</td>
<td>[4.15] Жеке басын куәландыратын құжат. Нөмірлеу және сиппатамасы Қағидалардың** 4-қосымшасына сәйкес.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/SeriesDocIdentity</td>
<td>Мәтіндік жол (10 символ)</td>
<td>[4.16 (2)] Жеке басын куәландыратын құжаттың сериясы.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/NumberDocIdentity</td>
<td>Мәтіндік жол (20 символ)</td>
<td>[4.16 (1)] Жеке басын куәландыратын құжаттың нөмірі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>[4.17] Жеке басын куәландыратын құжатты кім берген.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/Participant/ AdditionalPersonInfo/ AdditionalInformationIp/DateIssuance</td>
<td>Мәтіндік жол (dd.​mm.​yyyy түрінде)</td>
<td>[4.18] Жеке басын куәландыратын құжат қашан берілген.</td>
</tr>
</table>

### 4. Элементтердің құрамды типтерінің сиппатамасы

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
<td>Елдің коды. Нөмірленуі және сипаттамасы КОК-тың № 378 шешімімен бекітілген 22 «Әлем елдерінің жіктеуіші» қосымшасына сәйкес.</td>
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

### 5. ФМ-1 формасын қабылдау/қабылдамау туралы хабарламаны қалыптастыруға қолданылатын тегтер

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
<td>
Қате коды. Қабылданбау жөнінде хабарлама кезінде 0-ден өзгеше
Қатенің атауы/пайда болған қиындықтар
</td>
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

### 6. ҚМС-ты тіркеу сұратуын құруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData</td>
<td></td>
<td>ҚМС, оның құрылтайшылары және жауапты тұлғалары туралы мәліметтер</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ SystemId</td>
<td>Сан</td>
<td>Тіркелген ҚМС-тың идентификаторы. Тіркеу мәліметтерін түзету немесе өзгерту кезінде ғана қолданылады. ҚМС-ты тіркеуді сұратуды мақұлдау туралы хабарламадағы /ExportData/SignedData/Data/Root/SystemId тегтің мәніне сәйкес болуға тиісті.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ CfmCode</td>
<td>Сан</td>
<td>Қаржы мониторингі субъектісінің коды. Нөмірлері мен сипаттамалары Қағидалардың 3-қосымшасына сәйкес. (Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.1] бөлімінде көрсетіледі)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ OpfCode</td>
<td>Сан</td>
<td>Қаржы мониторингі субъектісінің ҰҚН коды. Нөмірлері мен сипаттамалары ұйымдық-құқықтық нысандарының жіктеушісіне сәйкес. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ OrgName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>Қаржы мониторингі субъектісінің аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ IINBIN</td>
<td>12 цифр</td>
<td>Қаржы мониторингі субъектісінің ЖСН/БСН (Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.4] бөлімінде көрсетіледі).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ PostalIndex</td>
<td>Мәтіндік жол (30 символ)</td>
<td>Қаржы мониторингі субъектісінің пошта индексі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (7)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Area/@code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығына сәйкес облыс коды. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ District/@code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығына сәйкес аудан коды. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ City/@code</td>
<td>Сан</td>
<td>ӘАОЖ анықтамалығына сәйкес елді мекен коды (қала/кент/ауыл). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (3)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Street</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Көшенің/даңғылдың/шағын ауданның атауы. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (4)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ House</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Үй нөмірі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (5)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Office</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Пәтер/офис нөмірі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.5 (6)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData</td>
<td></td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлға туралы қосымша ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/@IsAc</td>
<td>True немесе False</td>
<td>Есеп беруші қаржы мониторингі субъектісі жеке тұлға болып табылатындығын көрсететін атрибут. Егер жеке тұлға болмаса, онда /ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData тегтері көрсетілмейді.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/FirstName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлғаның аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2.2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/LastName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлғаның тегі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2.1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/MiddleName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісі болып табылатын жеке тұлғаның әкесінің аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.2 (1.2.3)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/DocumentIdentity</td>
<td>Сан</td>
<td>Жеке басын куәландыратын құжат түрінің коды (жеке тұлғалар үшін). Нөмірлері мен сипаттамалары Қағидалардың 4-қосымшасына сәйкес**. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/SeriesDocIdentity</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Жеке басын куәландыратын құжат нөмірі (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.1 (1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/NumberDocIdentityы</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Жеке басын куәландыратын құжат сериясы (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.1 (2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/DateIssuance</td>
<td>Күн (дд.мм.гггг түрінде)</td>
<td>Жеке басын куәландыратын құжат қашан берілді (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.3] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ AdditionalAcData/DocumentIssued</td>
<td>Мәтіндік жол (300 символ)</td>
<td>Жеке басын куәландыратын құжатты кім берді (жеке тұлғалар үшін). Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.6.2] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons</td>
<td></td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғалары туралы ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person</td>
<td></td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасы туралы ақпарат</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/FirstName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7(2)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/LastName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының тегі. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7(1)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/MiddleName</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының әкесінің аты. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7(3)] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/JobName</td>
<td>Мәтіндік жол (300 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының лауазымы. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.7.1] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/Phone</td>
<td>Мәтіндік жол (300 символ), қала коды/телефон нөмірі/ішкі телефонның нөмірі – форматында, телефондар үтір арқылы</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының телефоны. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.8] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/Email</td>
<td>Мәтіндік жол (100 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының электрондық поштасының мекен жайы. Бұл мән сәтті тіркелу кезінде ФМ-1 нысанының [2.8] бөлімінде көрсетіледі.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/Certificate</td>
<td>32Кб дейін</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының ашық кілт сертификаты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/Certificate/@Name</td>
<td>Мәтіндік жол (50 символ)</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының ашық кілт сертификатының аты.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/Certificate/@Size</td>
<td>Сан</td>
<td>Қаржы мониторингі субъектісінің жауапты тұлғасының ашық кілт сертификатының өлшемі.</td>
</tr>
</table>

### 7. ҚМА-ны тіркеуді сұратуды жеткізу туралы түбіртекті қалыптастыруда қолданылатын тегтер

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
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
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

### 8. ҚМС-ты тіркеу сұратуын қараудың оң нәтижесі туралы хабарламанықалыптастыруға қолданылатын тегтер

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

### 9. ҚМС-ты тіркеу сұратуын қараудың теріс нәтижесі туралы хабарламаны қалыптастыруға қолданылатын тегтер

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

### 10. ҚМС-тен қосымша ақпаратты алуға сұратуды қалыптастыруда қолданылатын тегтер

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

### 11. Қосымша ақпаратқа сұрату қабылдау туралы хабарламаны қалыптастыруға қолданылатын тегтер

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

### 12. ҚМС-ке қосымша ақпаратты алу сұратуына жауап қалыптастыруға қолданылатын тегтер

<table>
<tr>
<td>Тегтің құжатта орналасуы</td>
<td>Элемент типі</td>
<td>Элемент сипаттамасы</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Мәтіндік жол (36 символ: A–F символдары, 0-9 цифрлары)</td>
<td>ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ форматындағы негізгі хабарламаның GUID-і (сызықшалары бар жоғарғы тіркелімдегіоналтылық сан)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Comment</td>
<td>Мәтіндік жол (3000 символ)</td>
<td>ҚМС-ке қосымша ақпаратты алу сұрату жауабының мәтіні</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ResponseDateTime</td>
<td>Күн (dd.mm.yyyy hh24:mi:ss түрінде)</td>
<td>Жауапты жіберу күні мен уақыты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/Attachment/ FileName</td>
<td>Мәтіндік жол (255 символ)</td>
<td>Салынған файлдың аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/Attachment/ Length</td>
<td>Сан</td>
<td>Файл өлшемі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Name</td>
<td>Мәтіндік жол (255 символ)</td>
<td>Салынған файл бөлігінің аты</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Length</td>
<td>Сан</td>
<td>Салынған файл бөлігінің көлемі</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Buffer</td>
<td>Base64 кодпен жазылған жол</td>
<td>Салынған файл бөлігінің құрамы</td>
</tr>
</table>

Ескерту:

* Нөмірленуі осы Қағидалардың 1-қосымшасының ФМ-1 нысанындағы деректемелерге сәйкес келеді.

** осы Қағида.

Аббревиатуралардың мағынасын ашу:

ӘАОЖ – Әкімшілік-аумақтық объектілер жіктеушісі;

ҚМА – Қазақстан Республикасының Қаржылық мониторинг агенттігі;

ҚМС – Қаржы мониторингі субъектілері;

ТББЖ – Төлем белгілеудің бірыңғай жіктеушісі;

ҰҚН – Ұйымдық-құқықтық нысаны;

ЭҚЖЖ – Экономикалық қызметтің жалпы жіктеушісі.

ЭЦҚ – Электрондық цифрлық қолтаңба.

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *3-қосымша*

Нысан

## ҚМ-1 нысанының қабылданғаны немесе қабылданбағаны туралы хабарлама

```
____________________________________________________________________
                                                      (уәкілетті орган)
____________________________________________________________________
                              (қаржы мониторингі субъектісінің атауы)
_____ № __ ҚМ-1 нысаны ___________________________ туралы хабарлайды.
                                                 (қабылданғаны/қабылданбағаны)
Қабылданбау себебі (ҚМ-1 нысаны қабылданбаған жағдайда ғана көрсетіледі)
____________________________________________________________________.
Осыған байланысты __________________________________________________:
                                             (қаржы мониторингі субъектісінің атауы)
          1. Бұрмаланған түрде немесе толық емес көлемде ұсынылған ақпаратты
________________________________ жіберу себептерін жоюы.
              (уәкілетті орган)
          2. Осы хабарламаны _____________________________________________
                                                          (қаржы мониторингінің субъектісі)
алған күннен бастап 1 жұмыс күні ішінде қаржы мониторингіне жататын
операциялар туралы ____________________________________ қабылданбаған
                                                                          (уәкілетті орган)
хабарламаны түзетуі және осы Қаржы мониторингі субъектілерінің қаржы
мониторингіне жататын операциялар туралы мәліметтер мен ақпарат беру
қағидаларының ережелеріне сәйкес оны қайтадан ұсынуы қажет.
________________________           ____________           ______________________
      (уәкілетті органның                           (қолы)                (қолдың толық жазылуы)
 уәкілетті адамының тегі,
аты, әкесінің аты (болған жағдайда))
ҚМ-1 нысанының қабылданған немесе қабылданбаған күні мен уақыты:
_______________________________
```

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *4-қосымша*

## Қаржы мониторингі субъектілерінің түрлері кодтарының анықтамалығы

> *Ескерту. 4-қосымшаға өзгерістер енгізілді - ҚР Қаржылық мониторинг агенттігі Төрағасының 30.03.2024 № 2 (алғашқы ресми жарияланған күнінен кейін күнтізбелік он күн өткен соң қолданысқа енгізіледі); 24.09.2024 № 4 (алғашқы ресми жарияланған күнінен кейін күнтізбелік он күн өткен соң қолданысқа енгізіледі); 01.04.2025 № 5 (10.07.2025 бастап қолданысқа енгізіледі) бұйрықтарымен.*

<table>
<tr>
<td>Коды</td>
<td>Атауы</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>011</td>
<td>Банктер</td>
</tr>
<tr>
<td>013</td>
<td>Айырбастау пункттері</td>
</tr>
<tr>
<td>014</td>
<td>Агроөнеркәсіптік кешен саласындағы ұлттық басқарушы холдингтің еншілес кәсіпорындары</td>
</tr>
<tr>
<td>015</td>
<td>Ипотекалық ұйымдар</td>
</tr>
<tr>
<td>016</td>
<td>Банктік операциялардың жекелеген түрлерін жүзеге асыратын өзге ұйымдар</td>
</tr>
<tr>
<td>022</td>
<td>Қор биржалары</td>
</tr>
<tr>
<td>023</td>
<td>Тауар биржалары</td>
</tr>
<tr>
<td>024</td>
<td>Өз қызметін тауар биржасында жүзеге асыратын және биржалық тауарлармен мәмілелер жасайтын биржалық брокерлер</td>
</tr>
<tr>
<td>025</td>
<td>Тауар биржаларының клирингтік орталықтары</td>
</tr>
<tr>
<td>031</td>
<td>Сақтандыру (қайта сақтандыру) ұйымдары</td>
</tr>
<tr>
<td>032</td>
<td>Сақтандыру брокерлері</td>
</tr>
<tr>
<td>033</td>
<td>Өзара сақтандыру қоғамы</td>
</tr>
<tr>
<td>034</td>
<td>Қазақстанның Экспорттық-кредиттік агенттігі</td>
</tr>
<tr>
<td>042</td>
<td>Бірыңғай жинақтаушы зейнетақы қоры</td>
</tr>
<tr>
<td>043</td>
<td>Ерікті жинақтаушы зейнетақы қорлары</td>
</tr>
<tr>
<td>051</td>
<td>Бағалы қағаздар нарығының кәсіби қатысушылары</td>
</tr>
<tr>
<td>052</td>
<td>Орталық депозитарий</td>
</tr>
<tr>
<td>061</td>
<td>Ақшамен және (немесе) өзге де мүлікпен нотариаттық iс-әрекеттерді жүзеге асыратын нотариустар</td>
</tr>
<tr>
<td>071</td>
<td>Адвокаттар</td>
</tr>
<tr>
<td>072</td>
<td>Заң мәселелері жөніндегі тәуелсіз мамандар</td>
</tr>
<tr>
<td>073</td>
<td>Заң консультанттары</td>
</tr>
<tr>
<td>081</td>
<td>Аудиторлық ұйымдар</td>
</tr>
<tr>
<td>082</td>
<td>Бухгалтерлік есеп саласында кәсіпкерлік қызметті жүзеге асыратын бухгалтерлiк ұйымдар мен кәсiби бухгалтерлер</td>
</tr>
<tr>
<td>092</td>
<td>Лотерея ұйымдастырушылар</td>
</tr>
<tr>
<td>093</td>
<td>Казино</td>
</tr>
<tr>
<td>094</td>
<td>Ойын автоматтары залы</td>
</tr>
<tr>
<td>095</td>
<td>Букмекерлік кеңселер</td>
</tr>
<tr>
<td>096</td>
<td>Тотализаторлар</td>
</tr>
<tr>
<td>101</td>
<td>Ақша аударымы бойынша қызмет көрсететін пошта операторлары</td>
</tr>
<tr>
<td>110</td>
<td>Микроқаржы ұйымдары</td>
</tr>
<tr>
<td>111</td>
<td>Кредиттік серіктестіктер</td>
</tr>
<tr>
<td>130</td>
<td>Лизинг беруші ретінде лицензиясыз лизингтік қызметті жүзеге асыратын жеке кәсіпкерлер мен заңды тұлғалар</td>
</tr>
<tr>
<td>140</td>
<td>Ломбардтар</td>
</tr>
<tr>
<td>150</td>
<td>Бағалы металдармен және асыл тастармен, олардан жасалған зергерлік бұйымдармен операцияларды жүзеге асыратын жеке кәсіпкерлер және заңды тұлғалар</td>
</tr>
<tr>
<td>160</td>
<td>Жылжымайтын мүлікті сатып алу-сату мәмілелерін жүзеге асыру кезінде делдалдық қызметтер көрсететін жеке кәсіпкерлер мен заңды тұлғалар</td>
</tr>
<tr>
<td>171</td>
<td>Әлеуметтік медициналық сақтандыру қоры</td>
</tr>
<tr>
<td>172</td>
<td>Төлем ұйымдары</td>
</tr>
<tr>
<td>173</td>
<td>«Астана» халықаралық қаржы орталығының қатысушылары</td>
</tr>
<tr>
<td>174</td>
<td>Қазақстан Республикасының бейрезидент банктерінің филиалдары</td>
</tr>
<tr>
<td>175</td>
<td>Қазақстан Республикасы сақтандыру (қайта сақтандыру) бейрезидент ұйымдарының филиалдары</td>
</tr>
<tr>
<td>176</td>
<td>Қазақстан Республикасының бейрезидент сақтандыру брокерлерінің филиалдары</td>
</tr>
<tr>
<td>177</td>
<td>Қамтамасыз етілген цифрлық активтерді шығаруды және олардың айналымын жүзеге асыратын тұлғалар</td>
</tr>
</table>

> *Қаржы мониторингі*  
> *субъектілерінің қаржы*  
> *мониторингіне жататын*  
> *операциялар туралы*  
> *мәліметтер мен ақпарат*  
> *беру қағидаларына*  
> *5-қосымша*

## Жеке басты куәландыратын құжаттардың түрлері кодтарының анықтамалығы

> *Ескерту. 5-қосымша жаңа редакцияда - ҚР Қаржылық мониторинг агенттігі Төрағасының 28.09.2023 № 6 (алғашқы ресми жарияланған күнінен кейін күнтізбелік он күн өткен соң қолданысқа енгізіледі) бұйрығымен.*

<table>
<tr>
<td>Коды</td>
<td>Жеке басты куәландыратын құжаттардың атауы</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>01</td>
<td>Қазақстан Республикасы азаматының жеке куәлігі</td>
</tr>
<tr>
<td>02</td>
<td>Қазақстан Республикасы азаматының паспорты</td>
</tr>
<tr>
<td>03</td>
<td>Шетел паспорты</td>
</tr>
<tr>
<td>04</td>
<td>Шетелдіктің Қазақстан Республикасында тұруына ықтиярхат</td>
</tr>
<tr>
<td>05</td>
<td>Азаматтығы жоқ адамның куәлігі</td>
</tr>
<tr>
<td>06</td>
<td>Қазақстан Республикасының дипломатиялық паспорты</td>
</tr>
<tr>
<td>07</td>
<td>Қазақстан Республикасының қызметтік паспорты</td>
</tr>
<tr>
<td>08</td>
<td>Босқын куәлігі</td>
</tr>
<tr>
<td>09</td>
<td>Қазақстан Республикасы теңізшісінің жеке куәлігі</td>
</tr>
<tr>
<td>010</td>
<td>Туу туралы куәлік</td>
</tr>
<tr>
<td>011</td>
<td>Қайтып оралуға арналған куәлік</td>
</tr>
<tr>
<td>012</td>
<td>Шет мемлекет берген жеке куәлік</td>
</tr>
</table>

> *Қаржы мониторингі субъектілерінің*  
> *қаржы мониторингіне жататын*  
> *операциялар туралы мәліметтер*  
> *мен ақпарат беру қағидаларына*  
> *6-қосымша*

## Қаржы мониторингіне жататын операциялардың түрлері кодтарының анықтамалығы

> *Ескерту. 6-қосымша жаңа редакцияда - ҚР Қаржылық мониторинг агенттігі Төрағасының 28.09.2023 № 6 (алғашқы ресми жарияланған күнінен кейін күнтізбелік он күн өткен соң қолданысқа енгізіледі) бұйрығымен.*

<table>
<tr>
<td>Коды</td>
<td>Атауы</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>0111</td>
<td>Бәс тігуді өткізудің нәтижесі бойынша ұтысты қолма-қол ақшалай нысанда алу</td>
</tr>
<tr>
<td>0112</td>
<td>Бәс тігуді өткізудің нәтижесі бойынша ұтысты электрондық нысанда алу</td>
</tr>
<tr>
<td>0121</td>
<td>Ойын мекемелерінде құмар ойындар өткізудің нәтижесі бойынша ұтысты қолма-қол ақшалай нысанда алу</td>
</tr>
<tr>
<td>0122</td>
<td>Ойын мекемелерінде құмар ойындар өткізудің нәтижесі бойынша ұтысты электрондық нысанда алу</td>
</tr>
<tr>
<td>0131</td>
<td>Лотерея өткізудің нәтижесі бойынша ұтысты қолма-қол ақшалай нысанда алу</td>
</tr>
<tr>
<td>0132</td>
<td>Лотерея өткізудің нәтижесі бойынша ұтысты электрондық нысанда алу</td>
</tr>
<tr>
<td>0211</td>
<td>Клиенттің айырбастау пункттері арқылы шетел валютасын қолма-қол ақшалай нысанда сатып алуы</td>
</tr>
<tr>
<td>0221</td>
<td>Клиенттің айырбастау пункттері арқылы шетел валютасын қолма-қол ақшалай нысанда сатуы</td>
</tr>
<tr>
<td>0311</td>
<td>Чек бойынша қолма-қол ақшалай нысанда ақша алу</td>
</tr>
<tr>
<td>0321</td>
<td>Вексель бойынша қолма-қол ақшалай нысанда ақша алу</td>
</tr>
<tr>
<td>0511</td>
<td>Клиенттiң банктік шотынан ақша алу</td>
</tr>
<tr>
<td>0521</td>
<td>Клиенттiң банктік шотына ақша салу</td>
</tr>
<tr>
<td>0530</td>
<td>Клиентке қолма-қол ақша беру</td>
</tr>
<tr>
<td>0540</td>
<td>Клиенттен қолма-қол ақша қабылдау</td>
</tr>
<tr>
<td>0623</td>
<td>Оффшорлық аймақта тиісінше тiркелген, тұрғылықты жерi немесе орналасқан жерi бар және оффшорлық аймақта тiркелген банкте шоты бар жеке немесе заңды тұлғаның ақшаны клиенттің банктiк шотына салуы немесе аударуы</td>
</tr>
<tr>
<td>0633</td>
<td>Оффшорлық аймақта тiркелген, тұрғылықты жерi немесе орналасқан жерi бар, оффшорлық аймақта тiркелген банкте шоты бар жеке немесе заңды тұлғалардың пайдасына клиенттің ақшаны салуы немесе аударуы</td>
</tr>
<tr>
<td>0640</td>
<td>Клиенттің оффшорлық аймақта тiркелген, тұрғылықты жерi немесе орналасқан жерi бар, оффшорлық аймақта тiркелген банкте шоты бар жеке немесе заңды тұлғалармен ақшамен және (немесе) өзге мүлікпен жүргізетін операциялары</td>
</tr>
<tr>
<td>0711</td>
<td>Анонимді иеленушiге ашылған шетелдегi шоттарға (салымдарға) қол ақшалай немесе қолма-қол ақшасыз нысанда ақша аудару</td>
</tr>
<tr>
<td>0721</td>
<td>Анонимді иеленушiге ашылған шетелдегi шоттан (салымнан) ақшаның қолма-қол ақшалай немесе қолма-қол ақшасыз нысанда түсуi</td>
</tr>
<tr>
<td>0911</td>
<td>Өтеусiз негiзде басқа тұлғаның пайдасына клиент жүзеге асыратын қолма-қол ақшалай немесе қолма-қол ақшасыз нысандағы төлемдер мен ақша аударымдары</td>
</tr>
<tr>
<td>1011</td>
<td>Мәдени құндылықтарды қолма-қол ақшалай нысанда сатып алу</td>
</tr>
<tr>
<td>1012</td>
<td>Мәдени құндылықтарды қолма-қол ақшалай нысанда сату</td>
</tr>
<tr>
<td>1021</td>
<td>Мәдени құндылықтарды Қазақстан Республикасына әкелу</td>
</tr>
<tr>
<td>1022</td>
<td>Мәдени құндылықтарды Қазақстан Республикасынан әкету</td>
</tr>
<tr>
<td>1111</td>
<td>Мемлекеттiк тiркелген сәттен бастап үш ай аз уақыт өткен заңды тұлғалардың қолма-қол ақшалай немесе қолма-қол ақшасыз нысанда жүргізген операциялары</td>
</tr>
<tr>
<td>1211</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, Қазақстан Республикасына қолма-қол валютаны әкелу</td>
</tr>
<tr>
<td>1212</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, ұсынушыға құжаттық бағалы қағаздарды Қазақстан Республикасына әкелу</td>
</tr>
<tr>
<td>1213</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, Қазақстан Республикасына векселдерді әкелу</td>
</tr>
<tr>
<td>1214</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, Қазақстан Республикасына чектерді әкелу</td>
</tr>
<tr>
<td>1221</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкетуді қоспағанда, Қазақстан Республикасынан қолма-қол валютаны әкету</td>
</tr>
<tr>
<td>1222</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, ұсынушыға құжаттық бағалы қағаздарды Қазақстан Республикасынан әкету</td>
</tr>
<tr>
<td>1223</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, Қазақстан Республикасынан векселдерді әкету</td>
</tr>
<tr>
<td>1224</td>
<td>Қазақстан Республикасының Ұлттық Банкі, банктері мен ұлттық пошта операторы жүзеге асыратын әкелуді қоспағанда, Қазақстан Республикасынан чектерді әкету</td>
</tr>
<tr>
<td>1311</td>
<td>Сақтандыру төлемiн қолма-қол ақшалай нысанда жүзеге асыру</td>
</tr>
<tr>
<td>1321</td>
<td>Сақтандыру сыйлықақысын қолма-қол ақшалай нысанда алу</td>
</tr>
<tr>
<td>1411</td>
<td>Жинақтаушы зейнетақы қорларына еріктi зейнетақы жарналарын қолма-қол ақшалай нысанда енгізу</td>
</tr>
<tr>
<td>1421</td>
<td>Жинақтаушы зейнетақы қорларына еріктi зейнетақы жарналарын қолма-қол ақшалай нысанда аудару</td>
</tr>
<tr>
<td>1431</td>
<td>Еріктi зейнетақы жарналары есебінен жинақтаушы зейнетақы қорларынан зейнетақы төлемдерін қолма-қол ақшалай нысанда жүзеге асыру</td>
</tr>
<tr>
<td>1511</td>
<td>Қаржы лизингінің шарты бойынша мүлікті қолма-қол ақшалай нысанда және қолма-қол ақшасыз нысанда алу</td>
</tr>
<tr>
<td>1521</td>
<td>Қаржы лизингінің шарты бойынша мүлікті қолма-қол ақшалай нысанда және қолма-қол ақшасыз нысанда ұсыну</td>
</tr>
<tr>
<td>1611</td>
<td>Мердігер қызметтерін көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1621</td>
<td>Тасымалдау қызметтерін көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1631</td>
<td>Көліктік экспедиция қызметтерін көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1641</td>
<td>Сақтау қызметтерін көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1651</td>
<td>Комиссия қызметтерін көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1661</td>
<td>Мүлікті сенімгерлік басқару қызметтерін көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1671</td>
<td>Мердiгерлiк, тасымалдау, көлiк экспедициясы, сақтау, комиссиялар және мүлiктi сенiмгерлiк басқару қызметтерін қоспағанда, өзге де қызметтер көрсету бойынша қолма-қол ақшалай нысандағы мәмілелер</td>
</tr>
<tr>
<td>1711</td>
<td>Клиенттің бағалы металдар мен асыл тастарды, олардан жасалған зергерлік бұйымдарды қолма-қол ақшалай және қолма-қол ақшасыз нысанда сатып алуы</td>
</tr>
<tr>
<td>1721</td>
<td>Клиенттің бағалы металдар мен асыл тастарды, олардан жасалған зергерлік бұйымдарды қолма-қол ақшалай және қолма-қол ақшасыз нысанда сатуы</td>
</tr>
<tr>
<td>1811</td>
<td>Жасау нәтижесінде мұндай мүлікке меншік құқығы өтетін жылжымайтын мүлiкпен жасалатын мәмiлелер</td>
</tr>
<tr>
<td>1911</td>
<td>Ұйымдастырылған нарықтағы ашық сауда-саттық әдісімен репо операцияларын қоспағанда, облигациялармен және мемлекеттік бағалы қағаздармен қолма-қол ақшалай немесе қолма-қол ақшасыз нысандағы мәмілелер</td>
</tr>
<tr>
<td>2020</td>
<td>Ұйымдастырылған нарықтағы ашық сауда-саттық әдісімен репо операцияларын қоспағанда, акциялармен және пайлық инвестициялық қорлардың пайларымен қолма-қол ақшалай немесе қолма-қол ақшасыз нысандағы мәмілелер</td>
</tr>
<tr>
<td>2110</td>
<td>Ломбардтардың ақшамен, бағалы қағаздармен, бағалы металдармен және асыл тастармен, олардан жасалған зергерлік бұйымдармен және өзге де құндылықтармен (бағалы металдардан жасалған ұлттық валюта монеталарынан басқа) қолма-қол ақшалай немесе қолма-қол ақшасыз нысанда операциялар жасауы</td>
</tr>
<tr>
<td>2200</td>
<td>Квазимемлекеттік сектор субъектілерінің операцияны жасаған кезеңде қолданыста болған облигациялық қарыздары шеңберінде Қазақстан Республикасы Ұлттық қорының қаражаты есебінен кәсіпкерлік субъектілерін қаржыландыру бағдарламалары бойынша қарыз алған клиенттердің қолма-қол ақшалай немесе қолма-қол ақшасыз нысандағы операциялары</td>
</tr>
<tr>
<td>2300</td>
<td>
Өзінің сипаты бойынша трансшекаралық төлемге және клиенттің банктік шотынан қолма-қол ақшасыз нысанда ақша аударуға жататын операциялар
Әр түрлі елдердегі қатысушылар арасындағы төлем немесе аударым трансшекаралық болып табылады
</td>
</tr>
<tr>
<td>2301</td>
<td>
Өзінің сипаты бойынша трансшекаралық төлемге және қолма-қол ақшасыз нысандағы ақшаны клиенттің банк шотына трансшекаралық аударуға жататын операциялар
Әр түрлі елдердегі қатысушылар арасындағы төлем немесе аударым трансшекаралық болып табылады
</td>
</tr>
<tr>
<td>2302</td>
<td>Өзіндік сипаты бойынша шетел мемлекетінен клиенттің шотына (оның ішінде үшінші тұлғалардың шоттары арқылы) бұрын түскен қолма-қол ақшасыз нысандағы ақшаны клиенттің банктік шотынан аударуға және трансшекаралық төлемдерге жататын операциялар</td>
</tr>
<tr>
<td>6010</td>
<td>Терроризмді және экстремизмді қаржыландырумен байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген жеке тұлғаның еңбек демалысына ақы төлеу және жалақы түрінде ақша алуы</td>
</tr>
<tr>
<td>6020</td>
<td>Терроризмді және экстремизмді қаржыландырумен байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген жеке тұлғаның зейнетақы, қызметтік іссапарларға арналған шығыстар, стипендия, жәрдемақы, өзге де әлеуметтік төлем түрінде ақша алуы</td>
</tr>
<tr>
<td>6030</td>
<td>Терроризмді және экстремизмді қаржыландырумен байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген жеке тұлғаның салықтар, коммуналдық және әлеуметтік төлемдер, бюджетке төленетін басқа да міндетті төлемдер, өсімпұлдар мен айыппұлдар төлеу бойынша төлемдері мен аударымдары</td>
</tr>
<tr>
<td>6040</td>
<td>Терроризмді және экстремизмді қаржыландырумен байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген ұйымның немесе жеке тұлғаның банктік шотына ақша салу</td>
</tr>
<tr>
<td>6055</td>
<td>Терроризмді және экстремизмді қаржыландыруға байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген, бенефициарлық меншік иесі болып табылатын тұлғаның ұйымның банктік шотына ақша салуы.</td>
</tr>
<tr>
<td>6060</td>
<td>Сот шешімі негізінде терроризм мен экстремизмді қаржыландыруға байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген ұйымдар мен жеке тұлғалардың ақшасымен және (немесе) өзге де мүлкімен жүргізілетін операциялар мына кодтарда көзделген операцияларды қоспағанда: 6010, 6020, 6030, 6040, 6055</td>
</tr>
<tr>
<td>6061</td>
<td>Жаппай қырып-жою қаруын таратуды қаржыландыруға байланысты ұйымдар мен тұлғалардың тізбесіне енгізілген ұйымдар мен жеке тұлғалардың ақшасымен және (немесе) өзге мүлкімен жүргізілетін операциялар</td>
</tr>
<tr>
<td>6062*</td>
<td>Қаржы мониторингіне жататын, операция түрлері кодтарының бірде біріне жатпайтын операциялар</td>
</tr>
<tr>
<td>6064</td>
<td>«Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы» Қазақстан Республикасы Заңының 12-бабы 4-тармағының 7) тармақшасында көзделген негіздер бойынша Терроризмді және экстремизмді қаржыландырумен байланысты ұйымдар мен тұлғалардың тізбесімен енгізілген жеке тұлғаларға қатысты ақшамен және (немесе) өзге мүлікпен операцияларды тоқтатып қою бойынша қолданылатын шаралардың ішінара немесе толық күшін жою</td>
</tr>
<tr>
<td>6065*</td>
<td>Заңның 12-1-бабы 5-тармағында көзделген негіздер бойынша Терроризмді және экстремизмді қаржыландырумен байланысты ұйымдар мен тұлғалардың тізбесімен енгізілген жеке тұлғаларға қатысты ақшамен және (немесе) өзге мүлікпен операцияларды тоқтатып қою бойынша қолданылатын шаралардың ішінара немесе толық күшін жою</td>
</tr>
</table>

*күдікті деп танылған операцияларға қолданылады

> *Қаржы мониторингі субъектілерінің*  
> *қаржы мониторингіне жататын*  
> *операциялар туралы мәліметтер*  
> *мен ақпарат беру қағидаларына*  
> *7-қосымша*

## Ақшамен және (немесе) өзге мүлікпен мәмілелер мен қатысушылардың түрлері кодтарының анықтамалығы

> *Ескерту. 7-қосымша жаңа редакцияда - ҚР Қаржылық мониторинг агенттігі Төрағасының 28.09.2023 № 6 (алғашқы ресми жарияланған күнінен кейін күнтізбелік он күн өткен соң қолданысқа енгізіледі) бұйрығымен.*

<table>
<tr>
<td>Қатысушы түрінің коды</td>
<td>Қатысушы түрінің атауы</td>
<td>Мәміле түрінің коды</td>
<td>Мәміле түрінің атауы</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
</tr>
<tr>
<td rowspan="2">01</td>
<td rowspan="2">Сатушы</td>
<td>01</td>
<td>Жылжымайтын мүлікті сатып алу-сату шарты</td>
</tr>
<tr>
<td>02</td>
<td rowspan="2">Тауарды немесе қызметті сатып алу-сату шарты</td>
</tr>
<tr>
<td rowspan="2">02</td>
<td rowspan="2">Сатып алушы</td>
<td rowspan="2">03</td>
</tr>
<tr>
<td>Басқа да мүлікті сатып алу-сату шарты</td>
</tr>
<tr>
<td>03</td>
<td>Сыйлық беруші</td>
<td rowspan="2">04</td>
<td rowspan="2">Сыйға беру шарты</td>
</tr>
<tr>
<td>04</td>
<td>Сыйлық алушы</td>
</tr>
<tr>
<td>05</td>
<td>Рента алушы</td>
<td rowspan="4">05</td>
<td rowspan="4">Мүліктік жалдау (жалға алу) шарты</td>
</tr>
<tr>
<td>06</td>
<td>Рента төлеуші</td>
</tr>
<tr>
<td>07</td>
<td>Жалға беруші</td>
</tr>
<tr>
<td>08</td>
<td>Жалға алушы</td>
</tr>
<tr>
<td>09</td>
<td>Лизинг беруші</td>
<td rowspan="2">06</td>
<td rowspan="2">Лизинг шарты</td>
</tr>
<tr>
<td>10</td>
<td>Лизинг алушы</td>
</tr>
<tr>
<td>11</td>
<td>Несие беруші</td>
<td rowspan="2">07</td>
<td rowspan="2">Мүлікті өтеусіз пайдалану шарты</td>
</tr>
<tr>
<td>12</td>
<td>Несие алушы</td>
</tr>
<tr>
<td>13</td>
<td>Тапсырыс беруші</td>
<td rowspan="5">08</td>
<td rowspan="5">Мердігер шарты</td>
</tr>
<tr>
<td>14</td>
<td>Мердігер</td>
</tr>
<tr>
<td>15</td>
<td>Жобалаушы</td>
</tr>
<tr>
<td>16</td>
<td>Іздестіруші</td>
</tr>
<tr>
<td>17</td>
<td>Орындаушы</td>
</tr>
<tr>
<td>18</td>
<td>Жөнелтуші (көлік қызметі)</td>
<td rowspan="5">09</td>
<td rowspan="5">Көліктік экспедицияны тасымалдау шарты</td>
</tr>
<tr>
<td>19</td>
<td>Тасымалдаушы</td>
</tr>
<tr>
<td>20</td>
<td>Алушы (көлік қызметі)</td>
</tr>
<tr>
<td>21</td>
<td>Экспедитор</td>
</tr>
<tr>
<td>22</td>
<td>Қарыз беруші</td>
</tr>
<tr>
<td>23</td>
<td>Қарыз алушы</td>
<td rowspan="2">10</td>
<td rowspan="2">Қарыз шарты</td>
</tr>
<tr>
<td>24</td>
<td>Кредит беруші</td>
</tr>
<tr>
<td>25</td>
<td>Қаржы агенті</td>
<td rowspan="2">11</td>
<td rowspan="2">Кредиттік шарт</td>
</tr>
<tr>
<td>26</td>
<td>Клиент (факторинг)</td>
</tr>
<tr>
<td>27</td>
<td>Бенефициар</td>
<td rowspan="3">12</td>
<td rowspan="3">Ақша талабына жол беруді қаржыландыру шарты (факторинг)</td>
</tr>
<tr>
<td>28</td>
<td>Принципал</td>
</tr>
<tr>
<td>29</td>
<td>Салымшы</td>
</tr>
<tr>
<td rowspan="3">30</td>
<td rowspan="3">Эмитент</td>
<td>13</td>
<td>Банктік шот шарты</td>
</tr>
<tr>
<td>14</td>
<td>Ақшаны аудару шарты</td>
</tr>
<tr>
<td rowspan="2">15</td>
<td rowspan="2">Банктік салым шарты</td>
</tr>
<tr>
<td rowspan="2">31</td>
<td rowspan="2">Иеленуші</td>
</tr>
<tr>
<td rowspan="2">16</td>
<td rowspan="2">Басқа да банктік қызмет көрсету шарты</td>
</tr>
<tr>
<td>32</td>
<td>Кепілзат беруші</td>
</tr>
<tr>
<td>33</td>
<td>Кепілзат ұстаушы</td>
<td rowspan="2">17</td>
<td rowspan="2">Кепілзат шарты</td>
</tr>
<tr>
<td>34</td>
<td>Сақтаушы</td>
</tr>
<tr>
<td>35</td>
<td>Жүк беруші</td>
<td rowspan="2">18</td>
<td rowspan="2">Сақтау шарты</td>
</tr>
<tr>
<td>36</td>
<td>Сақтандырушы</td>
</tr>
<tr>
<td>37</td>
<td>Сақтанушы</td>
<td rowspan="3">19</td>
<td rowspan="3">Сақтандыру шарты</td>
</tr>
<tr>
<td>38</td>
<td>Сақтандырылған</td>
</tr>
<tr>
<td>39</td>
<td>Сенім білдіруші</td>
</tr>
<tr>
<td>40</td>
<td>Сенім білдірілген адам</td>
<td>20</td>
<td rowspan="2">Тапсырма шарты</td>
</tr>
<tr>
<td rowspan="2">41</td>
<td rowspan="2">Комитент</td>
<td rowspan="2">21</td>
</tr>
<tr>
<td>Кепілгерлік шарты</td>
</tr>
<tr>
<td>42</td>
<td>Комиссионер</td>
<td rowspan="2">22</td>
<td rowspan="2">Комиссия шарты</td>
</tr>
<tr>
<td>43</td>
<td>Басқарма құрылтайшысы</td>
</tr>
<tr>
<td>44</td>
<td>Сенімгерлікпен басқарушы</td>
<td rowspan="2">23</td>
<td rowspan="2">Мүлікті сенімгерлік басқару шарты</td>
</tr>
<tr>
<td>45</td>
<td>Құқық иеленуші</td>
</tr>
<tr>
<td rowspan="3">46</td>
<td rowspan="3">Пайдаланушы</td>
<td>24</td>
<td>Патенттік құқықтарды беру туралы шарт</td>
</tr>
<tr>
<td>25</td>
<td>Зияткерлік шығармашылық қызмет нәтижелерін құру және пайдалану туралы шарт</td>
</tr>
<tr>
<td rowspan="2">26</td>
<td rowspan="2">Өнертабысты, пайдалы моделді және/немесе өнеркәсіптік үлгіні пайдалануға арналған лицензиялық немесе қосалқы лицензиялық шарт</td>
</tr>
<tr>
<td>47</td>
<td>Лицензиат</td>
</tr>
<tr>
<td>48</td>
<td>Патент иесі</td>
<td rowspan="2">27</td>
<td rowspan="2">Кешенді кәсіпкерлік лицензияның шарты (франчайзинг)</td>
</tr>
<tr>
<td>49</td>
<td>Лотерея, тотализатор ұйымдастырушы</td>
</tr>
<tr>
<td>50</td>
<td>Лотерея, тотализатор қатысушысы</td>
<td rowspan="4">28</td>
<td rowspan="4">Басқа шарт, келісім немесе келісімшарт</td>
</tr>
<tr>
<td>51</td>
<td>Өнім беруші</td>
</tr>
<tr>
<td>52</td>
<td>Өндіруші</td>
</tr>
<tr>
<td rowspan="2">53</td>
<td rowspan="2">Жалға беруші</td>
</tr>
<tr>
<td rowspan="3">29</td>
<td rowspan="3">Негіздік құжатсыз мәміле</td>
</tr>
<tr>
<td>54</td>
<td>Жалға алушы</td>
</tr>
<tr>
<td>55</td>
<td>Басқа да қатысушы</td>
</tr>
<tr>
<td>56</td>
<td>Салымшы</td>
<td rowspan="2">30</td>
<td rowspan="2">Міндетті зейнетақы жарналары, міндетті кәсіби зейнетақы жарналары,ерікті зейнетақы жарналары есебінен зейнетақыны қамтамасыз ету туралы шарт</td>
</tr>
<tr>
<td>57</td>
<td>Алушы</td>
</tr>
<tr>
<td>58</td>
<td>Өз қаражатын жөнелтуші</td>
<td rowspan="2">31</td>
<td rowspan="2">Өз қаражатын аудару</td>
</tr>
<tr>
<td>59</td>
<td>Өз қаражатын алушы</td>
</tr>
<tr>
<td>60</td>
<td>Инвестор</td>
<td rowspan="2">32</td>
<td rowspan="2">Инвестициялық шарт</td>
</tr>
<tr>
<td>61</td>
<td>Инвестиция алушы</td>
</tr>
<tr>
<td>62</td>
<td>Бас компания</td>
<td>33</td>
<td rowspan="2">Бас компания мен филиал арасындағы аударымдар</td>
</tr>
<tr>
<td>63</td>
<td>Компанияның филиалы</td>
<td></td>
</tr>
</table>

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *8-қосымша*

Нысан

## Қажетті ақпаратты, мәліметтер мен құжаттарды беру жөнінде сұрау салу

«Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы» Қазақстан Республикасы Заңының 17-бабы 1-тармағының 1) тармақшасына және 10-бабының 3-1-тармақтарына сәйкес

```
____________________________________________________________________
                                                                 (уәкілетті орган)
```

ақша аударымдары жүйесі арқылы өткізілген, халықаралық ақша аударымдары бойынша клиенттердің және клиенттердің бенефициарлық меншік иелерінің операциялары туралы мынадай ақпаратты, мәліметтер мен құжаттарды беруді сұрайды:

1. _____________________;

2. _____________________.

```
___________________________           _________              ____________________
(уәкілетті органның уәкілетті                   (қолы)            (қолдың толық жазылуы)
      тұлғасының тегі, аты,
әкесінің аты (болған жағдайда))
```

Байланыс телефоны _________________

Сұрау салудың жіберілген күні мен уақыты: ________________________

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *9-қосымша*

Нысан

## Қажетті ақпаратты, мәліметтер мен құжаттарды беру жөнінде сұрау салудың қабылданғаны туралы хабарлама

```
__________________________________________________________________
                                 (қаржы мониторингі субъектісінің атауы)
__________________________________________________________________
                                                            (уәкілетті орган)
          ________ № ______ қаржы мониторингіне жататын операция бойынша
қажетті ақпаратты, мәліметтер мен құжаттарды беруге сұрау салудың
қабылданғаны туралы хабарлайды.
____________________________      ____________       __________________
(қаржы мониторингі субъектісінің     (қолы)            (қолдың толық жазылуы)
     жауапты адамының тегі, аты,
  әкесінің аты (болған жағдайда))
```

Сұрау салудың қабылданған күні мен уақыты: __________________________

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *10-қосымша*

Нысан

## Қажетті ақпаратты, мәліметтер мен құжаттарды беру жөнінде сұрау салуға жауап

«Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы» 2009 жылғы 28 тамыздағы Қазақстан Республикасының Заңының 17-бабы 1-тармағының және 10-бабының 3-1 және 3-2-тармақтарына сәйкес

```
___________________________________________________________________
                                       (қаржы мониторингі субъектінің аты)
```

__________ № ______ сұрау салуға мынадай ақпаратты, мәліметтер* мен құжаттарды жібереді:

1. _______________;

2. _______________.

Қосымша _____ парақта.

```
_____________________________     __________    _______________________
(қаржы мониторингі субъектісінің          (қолы)       (қолдың толық жазылуы)
      жауапты адамының тегі, аты,
   әкесінің аты (болған жағдайда))
```

Байланыс телефоны: _________________

Жауаптың жіберілген күні мен уақыты: ________________________

*клиенттің банктік шоты бойынша үзінді көшірмелер осы нысанға қосымшаға сәйкес Microsoft Excel форматында беріледі, өзге мәліметтер қаржы мониторингі субъектісі дербес белгілеген нысан бойынша беріледі.

> *«Қажетті ақпаратты, мәліметтер мен құжаттарды беру жөнінде сұрау салуға жауап» нысанына*  
> *қосымша*

## Уәкілетті органның сұрау салуы шеңберінде қаржы мониторингі субъектілері беретін мәліметтер

<table>
<tr>
<td>Операцияның күні мен уақыты</td>
<td>Операция валютасы</td>
<td>Операцияның түрлері (құжаттың санаты)</td>
<td>ААЖ-ның атауы (болған жағдайда)</td>
<td>Оны өткізу валютасындағы сома</td>
<td>Тенгедегі сома</td>
<td>Төлеушінің атауы / Т.А.Ә.</td>
<td>Төлеушінің ЖСН-і/БСН-і</td>
<td>Төлеушінің резидентттігі</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
<td>7</td>
<td>8</td>
<td>9</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</table>

Кестенің жалғасы

<table>
<tr>
<td>Төлеушінің банкі</td>
<td>Төлеушінің шот нөмірі</td>
<td>Алушының атауы / Т.А.Ә.</td>
<td>Алушының ЖСН/-і БСН-і</td>
<td>Алушының резиденттігі</td>
<td>Алушының банкі</td>
<td>Алушының шот нөмірі</td>
<td>Төлем мақсаты ның коды</td>
<td>Төлем мақсаты</td>
</tr>
<tr>
<td>10</td>
<td>11</td>
<td>12</td>
<td>13</td>
<td>14</td>
<td>15</td>
<td>16</td>
<td>17</td>
<td>18</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</table>

Аббревиатуралардың мағынасын ашу:

ЖСН-і /БСН-і – жеке сәйкестендіру нөмірі/ бизнес сәйкестендіру нөмірі

ААЖ – ақша аударымдардың жүйесі

Т.А.Ә. - тегі, аты, әкесінің аты

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *11-қосымша*

Нысан

## Қажетті ақпаратты, мәліметтер мен құжаттарды беру жөнінде сұрау салу мерзімін ұзарту туралы өтініш

```
___________________________________________________________________
                                      (қаржы мониторингі субъектісінің атауы)
__________________________ көрсетілген қажетті ақпаратты, мәліметтер мен
                (уәкілетті орган)
құжаттарды беру жөніндегі ____________№________ сұрау салуда көрсетілген
мерзімді _____ жұмыс күніне дейін ұзарту туралы өтініш береді.
_____________________________     _________      _______________________
(қаржы мониторингі субъектісінің        (қолы)           (қолдың толық жазылуы)
     жауапты адамының тегі, аты,
   әкесінің аты (болған жағдайда))
```

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *12-қосымша*

Нысан

> *Қаржы мониторингі*  
> *субъектісінің атауы*

## Күдікті операцияны тоқтата тұру қажеттілігінің жоқтығы туралы №_____хабарлама

Қазақстан Республикасы Қаржылық мониторинг агенттігі (бұдан әрі – Агенттік ) «Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы» Қазақстан Республикасы Заңының 13-бабының 3-тармағына сәйкес 20__ жылғы «__» ________ № _____ хабарлама бойынша күдікті операцияны тоқтата тұру қажеттілігінің жоқтығы туралы шешім қабылдады.

Негіздеме: Агенттіктің 20__ жылғы «__» _________ № ___ бұйрығы.

```
Құрылымдық бөлімшенің
басшысы                                     __________        _______________________
                                                            (қолы)            (қолдың толық жазылуы)
```

«__» __________ 20__ ж.

> *Қаржы мониторингі субъектілерінің қаржы мониторингіне жататын операциялар туралы мәліметтермен ақпарат беру қағидаларына*  
> *13-қосымша*

Нысан

> *Қаржы мониторингі*  
> *субъектісінің атауы*

## күдікті операцияны тоқтата тұру туралы №_____хабарлама

Қазақстан Республикасы Қаржылық мониторинг агенттігі (бұдан әрі – Агенттік ) «Қылмыстық жолмен алынған кірістерді заңдастыруға (жылыстатуға) және терроризмді қаржыландыруға қарсы іс-қимыл туралы» Қазақстан Республикасы Заңының 13-бабының 3-тармағына сәйкес 20__жылғы «__» ________ № _____ хабарлама бойынша күдікті операцияны 20___жылғы ______ сағат ____ бастап 20___жылғы ______ сағат_____ дейін тоқтата тұру қажеттігі туралы шешім қабылданды.

Негіздеме: Агенттіктің 20__ жылғы «__________» № ___ бұйрығы.

```
Құрылымдық бөлімшенің
басшысы                                  __________        ________________________
                                                         (қолы)             (қолдың толық жазылуы)
```

«__» __________ 20__ ж.
