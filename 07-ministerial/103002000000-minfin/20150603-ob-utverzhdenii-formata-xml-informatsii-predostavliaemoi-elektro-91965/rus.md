---
version_id: '91965_35308'
act_code: '91965'
language: rus
title: Об утверждении формата XML информации, предоставляемой электронным способом субъектами финансового мониторинга
requisite: Приказ Министра финансов Республики Казахстан от 3 июня 2015 года № 345. Зарегистрирован в Министерстве юстиции Республики Казахстан 7 июля 2015 года № 11569. Утратил силу приказом Министра финансов Республики Казахстан от 24 сентября 2020 года № 915 (вводится в действие с 15 ноября 2020 года)
form: ПРИК
type_codes:
- ПРИК
approved_by:
- '103002000000'
approval_date: 2015-06-03
version_date: 2015-06-03
registry_number: '91965'
source: https://zan.gov.kz/client/#!/doc/91965/rus/03.06.2015
---

# Об утверждении формата XML информации, предоставляемой электронным способом субъектами финансового мониторинга

В соответствии с пунктом 3 Правил представления субъектами финансового мониторинга сведений и информации об операциях, подлежащих финансовому мониторингу, утвержденных постановлением Правительства Республики Казахстан от 23 ноября 2012 года № 1484 «Об утверждении Правил представления субъектами финансового мониторинга сведений и информации об операциях, подлежащих финансовому мониторингу, и признаков критериев определения подозрительной операции», ПРИКАЗЫВАЮ:

1. Утвердить прилагаемый формат XML информации, предоставляемой электронным способом субъектами финансового мониторинга.

2. Комитету по финансовому мониторингу Министерства финансов Республики Казахстан (Таджияков Б.Ш.) в установленном законодательством порядке обеспечить:

   1) государственную регистрацию настоящего приказа в Министерстве юстиции Республики Казахстан;

   2) в течение десяти календарных дней после государственной регистрации настоящего приказа его направление на официальное опубликование в периодических печатных изданиях и информационно-правовой системе «Әділет»;

   3) размещение настоящего приказа на интернет-ресурсе Министерства финансов Республики Казахстан.

3. Настоящий приказ вводится в действие с 1 июля 2015 года и подлежит официальному опубликованию.

**Министр финансов Республики Казахстан**

**Б. Султанов**

> *Утвержден*  
> *приказом Министра финансов*  
> *Республики Казахстан*  
> *от 3 июня 2015 года № 345*

# Формат XML информации, предоставляемой электронным способом субъектами финансового мониторинга

## 1. Типы сообщений в системе

<table>
<tr>
<td>
№
п/п
</td>
<td>Тип сообщения в системе</td>
<td>Наименование xml файла</td>
</tr>
<tr>
<td>1</td>
<td>Информационное сообщение по форме ФМ-1</td>
<td>doc</td>
</tr>
<tr>
<td>2</td>
<td>Извещение о принятии формы ФМ-1</td>
<td>Ack1</td>
</tr>
<tr>
<td>3</td>
<td>Извещение о непринятии формы ФМ-1</td>
<td>Ack2</td>
</tr>
<tr>
<td>4</td>
<td>Запрос регистрации СФМ</td>
<td>Registration</td>
</tr>
<tr>
<td>5</td>
<td>Квитанция о доставке запроса регистрации СФМ</td>
<td>Ack12</td>
</tr>
<tr>
<td>6</td>
<td>Уведомление о положительном результате рассмотрения запроса на регистрацию СФМ</td>
<td>Ack14</td>
</tr>
<tr>
<td>7</td>
<td>Извещение об отрицательном результате рассмотрения запроса на регистрацию СФМ</td>
<td>Ack13</td>
</tr>
<tr>
<td>8</td>
<td>Запрос на предоставление дополнительной информации</td>
<td>DocInfo</td>
</tr>
<tr>
<td>9</td>
<td>Извещение о принятии запроса дополнительной информации</td>
<td>Ack1</td>
</tr>
<tr>
<td>10</td>
<td>Извещение о непринятии запроса дополнительной информации</td>
<td>Ack2</td>
</tr>
<tr>
<td>11</td>
<td>Ответ на запрос на получение дополнительной информации</td>
<td>UponDocInfo</td>
</tr>
<tr>
<td>12</td>
<td>Извещение о принятии ответа на запрос дополнительной информации</td>
<td>Ack1</td>
</tr>
<tr>
<td>13</td>
<td>Извещение о непринятии ответа на запрос дополнительной информации</td>
<td>Ack2</td>
</tr>
</table>

Для предоставления данных применяется кодировка символов UTF-16, из множества допустимых символов исключаются специальные символы: &(амперсанд), <> (открывающаяся закрывающаяся скобки), `(апостроф).

## 2. Теги, обязательно присутствующие в сообщениях различного назначения

<table>
<tr>
<td>
Расположение
тега в документе
</td>
<td>
Тип
Элемента
</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Sender</td>
<td>
Текстовая строка
до 32 символов: символы от A –Z, цифры от 0-9
</td>
<td>
Отправитель.
1) Строка с наименованием организации-СФМ, выполнившего отправку сообщения в КФМ. Указывается, если отправителем сообщения является СФМ.
2) Строка «KFM». Указывается, если отправителем сообщения является КФМ.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Receiver</td>
<td>
Текстовая строка
до 32 символов: символы от A –Z, цифры от 0-9
</td>
<td>
Получатель.
1) Строка «KFM». Указывается, если получателем сообщения является КФМ.
2) Строка с наименованием организации-СФМ. Указывается, если получателем сообщения является СФМ.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/TimeStamp</td>
<td>Тип DateType (предоставляется в виде дд.мм.гггг чч24:мм:сс)</td>
<td>Время отправки документа</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Version</td>
<td>
Текстовая строка
36 символов: символы A –F, цифры от 0-9
</td>
<td>GUID версии документа в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/DocumentUniqueIdentifier</td>
<td>
Текстовая строка
36 символов: символы A –F, цифры от 0-9
</td>
<td>GUID документа в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Signature</td>
<td>base64 строка, сформированная при помощи криптопровайдера Tumar в формате, соответствующем W3C</td>
<td>ЭЦП документа</td>
</tr>
<tr>
<td>/ExportData/TransportType</td>
<td>Число</td>
<td>Тип транспорта</td>
</tr>
</table>

## 3. Теги, применяемые для формирования информационного сообщения по форме ФМ-1

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента *</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData</td>
<td></td>
<td>[2] Сведения о субъекте финансового мониторинга, направившего форму ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/FirstName</td>
<td>Текстовая строка 100 символов</td>
<td>[2.7 (1)] Фамилия</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/SecondName</td>
<td>Текстовая строка 100 символов</td>
<td>[2.7 (2)] Имя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/MiddleName</td>
<td>Текстовая строка 100 символов</td>
<td>[2.7 (3)] Отчество (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/JobName</td>
<td>Текстовая строка 300 символов</td>
<td>[2.7.1] Должность ответственного должностного лица</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Phone</td>
<td>в формате код города/номер телефона/номер внутреннего телефона через запятую</td>
<td>[2.8] Контактные телефоны</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Email</td>
<td>Текстовая строка 100 символов</td>
<td>[2.9] Электронная почта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationCode</td>
<td>Число</td>
<td>[2.1] Код субъекта финансового мониторинга. Нумерация и описания соответствуют Приложению 3 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationOPF</td>
<td>Число</td>
<td>[2.2 (1.1)] Организационная форма субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/Organisation</td>
<td>Текстовая строка 300 символов</td>
<td>[2.2 (1.2)] Наименование субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ PersonalData/OrganisationArea/@Code</td>
<td>Число</td>
<td>[2.5 (1)] Код области (согласно справочнику КАТО)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationCity/@Code</td>
<td>Число</td>
<td>[2.5 (3)] Код населенного пункта (город/поселок/село) (справочнику КАТО)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationDistrict/@Code</td>
<td>Число</td>
<td>[2.5 (2)] Код района (согласно справочнику КАТО)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationStreet</td>
<td>Текстовая строка 100 символов</td>
<td>[2.5 (4)] Наименование улицы/проспекта/микрорайона</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationHouse</td>
<td>Текстовая строка 100 символов</td>
<td>[2.5 (5)] Номер дома</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationOffice</td>
<td>Текстовая строка 100 символов</td>
<td>[2.5 (6)] Номер квартиры/офиса (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/OrganisationPostalIndex</td>
<td>Число</td>
<td>[2.5 (7)] Почтовый индекс</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/IINBIN</td>
<td>12 цифр</td>
<td>[2.4] ИИН/БИН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/AdditionalAcData</td>
<td></td>
<td>[2.6 – 2.6.3] Сведения о документе, удостоверяющем личность (для СФМ, являющимся физическим лицом)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/AdditionalAcData/FirstName</td>
<td>Текстовая строка</td>
<td>[2.2 (1.2.2)] Имя СФМ, являющегося физическим лицом или индивидуальным предпринимателем</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/AdditionalAcData/LastName</td>
<td>Текстовая строка</td>
<td>[2.2 (1.2.1)] Фамилия СФМ, являющегося физическим лицом или индивидуальным предпринимателем</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data / Root/PersonalData/AdditionalAcData/MiddleName</td>
<td>Текстовая строка</td>
<td>[2.2 (1.2.3)] Отчество СФМ, являющегося физическим лицом или индивидуальным предпринимателем</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/AdditionalAcData/@IsAc</td>
<td>
True
или
False
</td>
<td>Атрибут, показывающий является ли СФМ, подающий отчет физическим лицом. Если нет, то теги соответствующие п.п.[2.6 – 2.6.3] Правил не указываются.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/AdditionalAcData/DocumentIdentity</td>
<td>Число</td>
<td>[2.6] Код типа документа, удостоверяющего личность (для физических лиц). Нумерация и описания соответствуют Приложению 4 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/AdditionalAcData/SeriesDocIdentity</td>
<td>Строка до 50 символов</td>
<td>[2.6.1 (1)] Номер документа удостоверяющего личность (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/AdditionalAcData/NumberDocIdentity</td>
<td>Строка до 50 символов</td>
<td>[2.6.1 (2)] Серия документа удостоверяющего личность (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/AdditionalAcData/DateIssuance</td>
<td>Дата (в виде дд.мм.гггг)</td>
<td>[2.6.3] Когда выдан документ, удостоверяющий личность (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/PersonalData/AdditionalAcData/DocumentIssued</td>
<td>Строка до 300 символов</td>
<td>[2.6.2] Кем выдан документ, удостоверяющий личность (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData /Data/Root/MessageInformation</td>
<td></td>
<td>[1] Сведения о сообщении и [3] Информация об операции, подлежащейнансовому мониторингу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/DocumentType</td>
<td>Число</td>
<td>[1.3] Вид документа – Нумерация и описания соответствуют п. 1.3 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MessageNumber</td>
<td>Число</td>
<td>[1.1(1)] Номер формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/LastModifyDate</td>
<td>Дата в виде dd.mm.yyyy</td>
<td>[1.2] Дата формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/TransactionDate</td>
<td>Дата в виде dd.mm.yyyy hh24:mi:ss</td>
<td>Время завершения/начала/ приостановки операции СФМ. Отсутствует в случае указания числа 4 в п [1.4] Правил **.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ViewOperationId</td>
<td>Число</td>
<td>[3.2 (1)] Код вида операции - Нумерация и описания соответствуют Приложению 5 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/EknpId</td>
<td>Число</td>
<td>[3.3 (1)] Код ЕКНП. Указывается идентификатор кода ЕКНП.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/EknpId/@IsEknpNotSetup</td>
<td>
True
или
False
</td>
<td>[3.3 (2)] Невозможно установить код ЕКНП - при значении True</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ OperationNumber</td>
<td>Текстовая строка 30 символов</td>
<td>[3.1] Номер операции</td>
</tr>
<tr>
<td>/ExportData/SignedParticipant/I ndividualIssueData/Data/Root/MessageInformation/ DocOperationReason</td>
<td>Число</td>
<td>[3.8] Основание совершения операции. Нумерация и описания соответствуют Приложению 6 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ DocOperationDate</td>
<td>Текстовая строка в виде dd.mm.yyyy</td>
<td>[3.9 (1)] Дата документа, на основании которого осуществляется операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/MessageInformation/ DocOperationNumber</td>
<td>Текстовая строка 30 символов</td>
<td>[3.9 (2)] Номер документа, на основании которого осуществляется операция</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ CurrencyCodeId</td>
<td>Число</td>
<td>[3.5] Код валюты операции в соответствии с Приложением 23 «Классификатор валют», утвержденным решением Комиссии Таможенного союза от 20 сентября 2010 года № 378 «О классификаторах, используемых для заполнения таможенных деклараций»</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/MessageInformation/AmountCurrency</td>
<td>Число</td>
<td>[3.6] Сумма операции в валюте ее проведения. Формат денежный - 99999999999999999999.99 (через точку).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/AmountCurrencyTenge</td>
<td>Число</td>
<td>[3.7] Сумма операции в тенге. Формат денежный - 99999999999999999999.99 (через точку).</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/OperationStatusId</td>
<td>Число</td>
<td>[1.4] Состояние операции. Нумерация и описание соответствуют п.1.4 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ReasonFilingId</td>
<td>Число</td>
<td>[1.5 ] Основание для подачи сообщения. Нумерация и описания соответствуют первому уровню п.1.5 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/CounterMeasure</td>
<td></td>
<td>[1.5] Мера противодействия при совпадении с перечнем организаций и лиц. Нумерация и описания соответствуют второму уровню пп. 4. п.1.5 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/SuspicionFirst</td>
<td>Число</td>
<td>[3.10] Код признака подозрительности операции. Нумерация и описания соответствуют Приложению 7 к Правилам**. Реквизит обязателен для заполнения в случае указания пункта 2 в реквизите 1.5 Приложения 1 Правил**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/SuspicionSecond</td>
<td>Число</td>
<td>[3.11] 1-й дополнительный признак подозрительности. Нумерация и описания соответствуют Приложению 7 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/SuspicionThird</td>
<td>Число</td>
<td>[3.12] 2-й дополнительный признак подозрительности. Нумерация и описания соответствуют Приложению 7 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/DescriptionDifficulties</td>
<td>Текстовая строка 1000 символов</td>
<td>[3.13] Описание возникших затруднений квалификации операции как подозрительной</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MoreInformation</td>
<td>Текстовая строка 1000 символов</td>
<td>[3.14] Дополнительная информация по операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ParticipantCount</td>
<td>Число</td>
<td>[3.4] Количество участников операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MerchTypes</td>
<td>Число</td>
<td>
[3.2 (2.1)] Вид имущества. Код вида имущества:
1 – Автомобиль
2 – Квартира
3 – Земельный участок
4 - Иное
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/MerchReginfo</td>
<td>Строка 50 символов</td>
<td>[3.2 (2.2)] Регистрационный номер имущества</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/MessageInformation/ReferCount</td>
<td></td>
<td>Количество связей с иными формами ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References</td>
<td></td>
<td>[1.1 (2)] Сведения о связях с иными формами ФМ-1 (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference</td>
<td></td>
<td>[1.1 (2)] Связь с иной формой ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference/ReferenceId</td>
<td>Число</td>
<td>Порядковый номер связи с иной формой</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference /Reference OperationNumber</td>
<td>Строка 50 символов</td>
<td>[1.1 (2.1)] Номер связанной формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference /Reference DocOperationDate</td>
<td>Текстовая строка в виде dd.mm.yyyy</td>
<td>
[1.1 (2.2)] Дата связанной формы
ФМ-1
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/References/Reference /ReferenceDocOperationNumber</td>
<td>Строка 50 символов</td>
<td>Номер операции в связанной форме</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants</td>
<td></td>
<td>[4] Сведения об участниках операции, подлежащей финансовому мониторингу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant</td>
<td></td>
<td>[4] Сведения об участнике операции, подлежащей финансовому мониторингу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/MemberId</td>
<td>Число</td>
<td>[4.1] Участник. Нумерация и описания соответствуют п.4.1 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ParticipantsView</td>
<td>Число</td>
<td>[4.3] Вид участника. Нумерация и описания соответствуют Приложению 6 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ParticipantsType</td>
<td>Число</td>
<td>
[4.5] Тип участника операции. Нумерация и описания соответствуют п.4.5 Приложения 1 к Правилам предоставления СФМ сведений.
В зависимости от типа субъекта–участника заполняется одна из веток:
- AdditionalInformationUr – для юридических лиц;
- AdditionalInformationAc – для физических лиц;
- AdditionalInformationIp – для индивидуальных предпринимателей.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/IsClientSubject</td>
<td>Число</td>
<td>[4.2] Клиент субъекта финансового мониторинга. Нумерация и описания соответствуют п.4.2 Приложения 1 к Правилам**. Указывается число «1», если не является клиентом СФМ, число «2», если является клиентом</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ Participants/Participant/Residence</td>
<td>Стро ка 2 сим вола (симво льный код стра ны)</td>
<td>[4.4] Резидентство. Нумерация и описания соответствуют Приложению 22 «Классификатор стран мира», утвержденным решением Комиссии Таможенного союза от 20 сентября 2010 года № 378 «О классификаторах, используемых для заполнения таможенных деклараций».</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ForeignPerson</td>
<td>Число</td>
<td>[4.6] Иностранное публичное должностное лицо. Нумерация и описания соответствуют п.4.6 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/CorrespondentBank</td>
<td></td>
<td>[4.7] Банк участника операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Account Number</td>
<td>Текстовая строка 300 символов</td>
<td>[4.7 (1.4)] Номер счета участника</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Name</td>
<td>Текстовая строка 300 символов</td>
<td>[4.7 (1.2)] Наименование банка/филиала</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Code</td>
<td>Текстовая строка 50 символов</td>
<td>[4.7 (1.3)] Код банка/филиала</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/BankAddress</td>
<td></td>
<td></td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Bank Country</td>
<td>Стро ка 2 сим вола (симво льный код стра ны)</td>
<td>[4.7 (1.1)] Местона хождение банка. Нумерация и описание соответствуют Приложе нию 22 «Классифи катор стран мира», утверж денным решением Комиссии Таможе нного союза от 20 сентября 2010 года № 378 «О классифи каторе использу емых для заполнения таможенных деклараций»</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Bank City</td>
<td>Текс товая стро ка 50 сим вол ов</td>
<td>[4.7 (1.1)] Место нахож дение филиала – в случае местона хождения филиала на терри тории Респуб лики Казахстан. Указы вается населен ный пункт, в котором иници ируется/ завер шается операция</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/Participants/Participant/ CorrespondentBank/Bank Offshore Addr</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>
[4.7 (1.1)] Страна оффшора в случае, если реквизит 3.2 &quot;Код вида операции&quot; имеет значение 611-634. Указы вается идентифи катор оффшорной зоны в соот ветствии с приказом и.о. Министра финансов Республики Казахстан от 10 февраля 2010 года № 52 «Об утверж дении Перечня оффшорных зон в целях Закона Республики Казахстан «О проти водействии легали зации (отмыванию доходов полученных преступным путем и финан сированию терро ризма)» зарегист рированный в Реестре государственной регистрации нормативных правовых актов под
№ 6058.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Corres pondentBank/@Is Offshore</td>
<td>True или False</td>
<td>Вспомо гательный признак нахож дения филиала в оффшо рной зоне</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/ Correspondents Informations</td>
<td></td>
<td>[4.7 (1.5) ] Сведе ния о коррес пондентс ких счетах, участвую щих в операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Corresponden tsInformations/ CorrespondentI nformation</td>
<td></td>
<td>[4.7 (1.5)] Сведения о коррес пондентском счете, участву ющем в операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Corresponden tsInformations/ CorrespondentInformation/BankName</td>
<td>Текс товая строка 300 симво лов</td>
<td>[4.7 (1.5.2)] Наи мено вание банка</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ CorrespondentBank/Corresponden tsInformations/Correspondent Information/BankCountry</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>[4.7 (1.5.1)] Место нахож дение банка. Нумера ция и описа ние соответ ствуют Приложе нию 22 «Классифи катор стран мира», утвержд енным реше нием Комиссии Таможен ного союза от 20 сентяб ря 2010 года № 378 «О классифи каторах, используе мых для заполне ния таможен ных декла раций».</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ IndividualIssue</td>
<td>Текс товая строка 32 символа</td>
<td>[4.13] ИИН/ БИН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/OKED</td>
<td>Текс товая строка 5 сим волов</td>
<td>[4.12] ОКЭД. Код ОКЭД указы вается в соответ ствии «Но менкла турой видов эконо мической деятельнос ти (ОКЭД 5- тизначный)» утверж денный приказом Предсе дателя Агентства Республики Казахстан по статистике от 20 мая 2008 года № 67, размещен ный на официаль ном сайте Коми тета по статис тике Минис терства нацио нальной эконо мики Республики Казахстан.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ PhoneNumber</td>
<td>в формате код города/номер телефона/номер внутреннего телефона через запятую</td>
<td>[4.22] Номер контактного телефона</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Email</td>
<td>Текстовая строка 100 символов</td>
<td>[4.23] Электронная почта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/Participants/Participant/ AdditionalInformation</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.25] Дополнительная информация об участнике операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/MoneyTransSys</td>
<td>Число</td>
<td>[4.7 (1.2.1)] Наименование системы денежных переводов.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Founders</td>
<td></td>
<td>[4.9] Учредители участника операции (для юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Founders/Founder</td>
<td></td>
<td>[4.9] Учредитель участника операции (для юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ Participants/Participant/Founders/ Founder/FounderType</td>
<td>Число</td>
<td>
Вспомогательный признак типа учредителя:
1 - Юридическое лицо
2 – Физическое лицо
3 – Индивидуальный предприниматель
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/FounderOPF</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.9 (1.1)] Организационная форма учредителя участника (заполняется для юридического лица)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/Name</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.9 (2.1)] Наименование учредителя участника (заполняется для юридического лица)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/FirstName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.9 (1.2.2)] Имя учредителя участника (заполняется для учредителя физического лица)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/SecondName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.9 (1.2.1)] Фамилия учредителя участника (заполняется для учредителя физического лица)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/MiddleName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.9 (1.2.3)] Отчество учредителя участника (заполняется для учредителя физического лица)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ Founders/Founder/Residence</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>[4.9 (2)] Резидентство учредителя участника операции. Нумерация и описания соответствуют Приложению 22 «Классификатор стран мира», утвержденным решением Комиссии Таможенного союза от 20 сентября 2010 года № 378 «О классификаторах, используемых для заполнения таможенных деклараций».</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo</td>
<td></td>
<td>Дополнительная информация по участникам операции. Разбиение на юридические, физические лица и индивидуальных предпринимателей</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/AdditionalInformationUr</td>
<td></td>
<td>Дополнительная информация по участнику - юридическому лицу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/URAddress</td>
<td>Составной типа Address</td>
<td>[4.21] Юридический адрес. Описание приведено ниже в описании составных типов элементов.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/ACAddress</td>
<td>Составной типа Address</td>
<td>[4.24] Фактический адрес. Описание приведено ниже в описании составных типов элементов.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FullName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.8 (1.2)] Наименование участника операции (для участников юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FullName/@IsFullNameSetup</td>
<td>
True
или
False
</td>
<td>[4.8 (2)] Невозможно установить наименование участника операции - при значении True (для участников юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/Additional PersonInfo/AdditionalInformationUr/FirstHead</td>
<td></td>
<td>[4.10] Первый руководитель (для участников юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead/FirstName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.10 (2)] Имя первого руководителя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead/SecondName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.10 (1)] Фамилия первого руководителя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/FirstHead/MiddleName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.10 (3)] Отчество первого руководителя (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationUr/ParticipantOPF</td>
<td>Число</td>
<td>[4.8 (1.1)] Организационная форма участника операции (для участников юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc</td>
<td></td>
<td>Дополнительная информация по участнику - физическому лицу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/URAddress</td>
<td>Составной типа Address</td>
<td>[4.21] Юридический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/ACAddress</td>
<td>Составной типа Address</td>
<td>[4.24] Фактический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO</td>
<td></td>
<td>[4.14] Ф.И.О. (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/FirstName</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.2)] Имя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/SecondName</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.1)] Фамилия</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/MiddleName</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.3)] Отчество (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/FIO/@IsFioNotSetup</td>
<td>
True
или
False
</td>
<td>[4.14 (2.1)] Невозможно установить - при значении True</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/PlaceBirth</td>
<td>Текстовая строка 300 символов</td>
<td>[4.20] Место рождения (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DateBirth</td>
<td>Текстовая строка в виде dd.mm.yyyy</td>
<td>[4.19] Дата рождения (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DocumentIdentity</td>
<td>Число</td>
<td>[4.15] Документ, удостоверяющий личность. Нумерация и описания соответствуют Приложению 4 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/SeriesDocIdentity</td>
<td>Текстовая строка 10 символов</td>
<td>[4.16 (2)] Серия документа, удостоверяющего личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/NumberDocIdentity</td>
<td>Текстовая строка 20 символов</td>
<td>[4.16 (1)] Номер документа, удостоверяющего личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DocumentIssued</td>
<td>Текстовая строка 300 символов</td>
<td>[4.17] Кем выдан документ, удостоверяющий личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationAc/DateIssuance</td>
<td>Текстовая строка в виде dd.mm.yyyy</td>
<td>[4.18] Когда выдан документ, удостоверяющий личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp</td>
<td></td>
<td>Дополнительная информация по индивидуальному предпринимателю - состав тегов аналогичен физическому лицу, кроме тега «ParticipantOPF» приведенного ниже. Данный тег располагается между тегами «FIO» и «PlaceBirth».</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/URAddress</td>
<td>Составной типа Address</td>
<td>[4.21] Юридический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/ACAddress</td>
<td>Составной типа Address</td>
<td>[4.24] Фактический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO</td>
<td></td>
<td>[4.14] Ф.И.О. (для индивидуальных предпринимателей)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Additiona lInformationIp/FIO/FirstName</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.2)] Имя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/SecondName</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.1)] Фамилия</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/MiddleName</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.3)] Отчество (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/FIO/@IsFioNotSetup</td>
<td>
True
или
False
</td>
<td>[4.14 (2.1)] Невозможно установить - при значении True</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/PlaceBirth</td>
<td>Текстовая строка 300 символов</td>
<td>[4.20] Место рождения (для индивидуальных предпринимателей)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DateBirth</td>
<td>Текстовая строка в виде dd.mm.yyyy</td>
<td>[4.19] Дата рождения (для индивидуальных предпринимателей)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Additiona lInformationIp/DocumentIdentity</td>
<td>Число</td>
<td>[4.15] Документ, удостоверяющий личность. Нумерация и описания соответствуют Приложению 4 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/SeriesDocIdentity</td>
<td>Текстовая строка 10 символов</td>
<td>[4.16 (2)] Серия документа, удостоверяющего личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/NumberDocIdentity</td>
<td>Текстовая строка 20 символов</td>
<td>[4.16 (1)] Номер документа, удостоверяющего личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DocumentIssued</td>
<td>Текстовая строка 300 символов</td>
<td>[4.17] Кем выдан документ, удостоверяющий личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Participants/Participant/ AdditionalPersonInfo/Addition alInformationIp/DateIssuance</td>
<td>Текстовая строка в виде dd.mm.yyyy</td>
<td>[4.18] Когда выдан документ, удостоверяющий личность</td>
</tr>
</table>

## 4. Описание составных типов элементов

<table>
<tr>
<td>Идентификатор типа</td>
<td>Идентификатор простого элемента</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>Address</td>
<td>Country</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>Код страны. Нумерация и описания соответствуют Приложению 22 «Классификатор стран мира», утвержденным решением Комиссии Таможенного союза от 20 сентября 2010 года № 378 «О классификаторах, используемых для заполнения таможенных деклараций».</td>
</tr>
<tr>
<td rowspan="10"></td>
<td>Area</td>
<td>Текстовая строка 100 символов</td>
<td>Область</td>
</tr>
<tr>
<td>Area/@Code</td>
<td>Число</td>
<td>Код области в справочнике КАТО</td>
</tr>
<tr>
<td>District</td>
<td>Текстовая строка 100 символов</td>
<td>Район</td>
</tr>
<tr>
<td>District/@Code</td>
<td>Число</td>
<td>Код района в справочнике КАТО</td>
</tr>
<tr>
<td>Town</td>
<td>Текстовая строка 100 символов</td>
<td>Населенный пункт</td>
</tr>
<tr>
<td>Town/@Code</td>
<td>Число</td>
<td>Код населенного пункта в справочнике КАТО</td>
</tr>
<tr>
<td>Street</td>
<td>Текстовая строка 100 символов</td>
<td>Улица</td>
</tr>
<tr>
<td>HomeNumber</td>
<td>Текстовая строка 10 символов</td>
<td>Номер дома</td>
</tr>
<tr>
<td>OfficeNumber</td>
<td>Текстовая строка 10 символов</td>
<td>Номер офиса</td>
</tr>
<tr>
<td>PostalCode</td>
<td>Текстовая строка, содержащая цифры</td>
<td>Почтовый индекс</td>
</tr>
</table>

## 5. Теги, применяемые для формирования извещения о принятии/непринятии формы ФМ-1

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/Description</td>
<td>Текстовая строка 3000 символов</td>
<td>Пояснения (применяется при повторной отправке извещения)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/OriginalDocumentGuid</td>
<td>Текстовая строка 36 символов: символы A –F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorCode</td>
<td>Число</td>
<td>Код ошибки. В случае извещения с отказом отличен от 0</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorName</td>
<td>Текстовая строка 3000 символов</td>
<td>Наименование ошибки\возникших затруднений</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/AcceptanceDateTime</td>
<td>Дата в виде dd.mm.yyyy hh24:mi:ss</td>
<td>Дата и время принятия (непринятия) формы ФМ-1</td>
</tr>
</table>

## 6. Теги, применяемые для формирования запроса регистрации СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Т и п э л е м е н т а</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData</td>
<td></td>
<td>Данные об СФМ, его учредителях и ответственных лицах</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/SystemId</td>
<td>Ч и с л о</td>
<td>Идентификатор зарегистрированного СФМ. Указывается только при корректировке или изменении регистрационных сведений. Значение должно соответствовать тегу /ExportData/SignedData/Data/Root/SystemId из уведомления об одобрении запроса регистрации в КФМ.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/CfmCode</td>
<td>Ч и с л о</td>
<td>Код субъекта финансового мониторинга. Нумерация и описания соответствуют Приложению 3 к Правилам**. (При успешной регистрации данное значение указывается в поле [2.1] Формы ФМ-1.)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/OpfCode</td>
<td>Ч и с л о</td>
<td>Код ОПФ субъекта финансового мониторинга. Нумерация и описания соответствуют классификатору организационно-правовых форм. При успешной регистрации данное значение указывается в поле [2.2 (1.1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/OrganisationData/OrgName</td>
<td>Текстовая строка 300 символов</td>
<td>Название субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.2 (1.2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/IINBIN</td>
<td>12 цифр</td>
<td>ИИН/БИН субъекта финансового мониторинга (При успешной регистрации данное значение указывается в поле [2.4] Формы ФМ-1.)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/PostalIndex</td>
<td>Текстовая строка 30 символов</td>
<td>Почтовый индекс субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.5 (7)] Формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Area/@code</td>
<td>Ч и с л о</td>
<td>Код области согласно справочнику КАТО. При успешной регистрации данное значение указывается в поле [2.5 (1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/District/@code</td>
<td>Ч и с л о</td>
<td>Код района согласно справочнику КАТО. При успешной регистрации данное значение указывается в поле [2.5 (2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/City/@code</td>
<td>Ч и с л о</td>
<td>Код населенного пункта (город/поселок/село) согласно справочнику КАТО. При успешной регистрации данное значение указывается в поле [2.5 (3)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Street</td>
<td>Текстовая строка 100 символов</td>
<td>Наименование улицы/проспекта/мр-на. При успешной регистрации данное значение указывается в поле [2.5 (4)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/House</td>
<td>Текстовая строка 100 символов</td>
<td>№ дома. При успешной регистрации данное значение указывается в поле [2.5 (5)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Office</td>
<td>Текстовая строка 100 символов</td>
<td>№ квартиры/офиса. При успешной регистрации данное значение указывается в поле [2.5 (6)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData</td>
<td></td>
<td>Дополнительная информация о физическом лице, являющемся субъектом финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Additional AcData/@IsAc</td>
<td>
True
или
False
</td>
<td>Атрибут, показывающий является ли субъект финансового мониторинга, подающий отчет физическим лицом. Если нет, то теги в /ExportData/SignedData/Data/Root/OrganisationData/AdditionalAcData не указываются.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/FirstName</td>
<td>Текстовая строка 100 символов</td>
<td>
Имя физического лица, являющегося субъектом финансового мониторинга
При успешной регистрации данное значение указывается в поле [2.2 (1.2.2)] Формы ФМ-1
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/LastName</td>
<td>Текстовая строка 100 символов</td>
<td>Фамилия физического лица, являющегося субъектом финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.2 (1.2.1)] Формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/MiddleName</td>
<td>Текстовая строка 100 символов</td>
<td>Отчество физического лица, являющегося субъектом финансового мониторинга/ При успешной регистрации данное значение указывается в поле [2.2 (1.2.3)] Формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/DocumentIdentity</td>
<td>Число</td>
<td>Код типа документа, удостоверяющего личность (для физических лиц). Нумерация и описания соответствуют Приложению 4 к Правилам**. При успешной регистрации данное значение указывается в поле [2.6] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/SeriesDocIdentity</td>
<td>Текстовая строка 50 символов</td>
<td>Номер документа удостоверяющего личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.1 (1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/NumberDocIdentity</td>
<td>Текстовая строка 50 символов</td>
<td>Серия документа удостоверяющего личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.1 (2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/DateIssuance</td>
<td>Дата (в виде дд.мм.гггг)</td>
<td>Когда выдан документ, удостоверяющий личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.3] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Addition alAcData/DocumentIssued</td>
<td>Текстовая строка 300 символов</td>
<td>Кем выдан документ, удостоверяющий личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.2] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons</td>
<td></td>
<td>Информация об ответственных лицах субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/Person</td>
<td></td>
<td>Информация об ответственном лице субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/FirstName</td>
<td>Текстовая строка 100 символов</td>
<td>Имя ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7(2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/LastName</td>
<td>Текстовая строка 100 символов</td>
<td>Фамилия ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7(1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/MiddleName</td>
<td>Текстовая строка 100 символов</td>
<td>Отчество ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7(3)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/JobName</td>
<td>Текстовая строка 300 символов</td>
<td>Должность ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7.1] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Phone</td>
<td>Текстовая строка 300 символов в формате код города/номер телефона/номер внутреннего телефона через запятую</td>
<td>Телефон ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.8] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Email</td>
<td>Текстовая строка 100 символов</td>
<td>Адрес электронной почты ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.9] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Certificate</td>
<td>До 32Кб</td>
<td>Сертификат открытого ключа ответственного лица субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Certificate/@Name</td>
<td>Текстовая строка 50 символов</td>
<td>Название сертификата открытого ключа ответственного лица субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OrganisationData/Persons/ Person/Certificate/@Size</td>
<td>Число</td>
<td>Размер сертификата открытого ключа ответственного лица субъекта финансового мониторинга</td>
</tr>
</table>

## 7. Теги, применяемые для формирования квитанции о доставке запроса регистрации в КФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/Description</td>
<td>Текстовая строка 3000 символов</td>
<td>Пояснения (применяется при повторной отправке квитанции)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/OriginalDocumentGuid</td>
<td>Текстовая строка 36 cимволов: символы A –F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/MessDate</td>
<td>Дата (в виде дд.мм.гггг чч:мм:сс)</td>
<td>Дата отправки запроса регистрации, по которому сформировано квитанция</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/MessOwn</td>
<td>Текстовая строка</td>
<td>Отправитель запроса регистрации, по которому сформировано квитанция</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorCode</td>
<td>Число</td>
<td>Код ошибки. В случае квитанции с отказом отличен от 0.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorName</td>
<td>Текстовая строка 3000 символов</td>
<td>Наименование ошибки\возникших затруднений</td>
</tr>
</table>

## 8. Теги, применяемые для формирования уведомления о положительном результате рассмотрения запроса регистрации СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Description</td>
<td>Текстовая строка 3000 символов</td>
<td>Пояснения (применяется при повторной отправке извещения)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Текстовая строка 36 cимволов: символы A –F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessDate</td>
<td>Дата (в виде дд.мм.гггг чч:мм:сс)</td>
<td>Дата отправки запроса регистрации, по которому сформировано уведомление</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessOwn</td>
<td></td>
<td>Отправитель запроса регистрации, по которому сформировано уведомление</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/SystemId</td>
<td>Число</td>
<td>Присвоенный при регистрации идентификатор СФМ</td>
</tr>
</table>

## 9. Теги, применяемые для формирования извещения об отрицательном результате рассмотрения запроса на регистрацию СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Description</td>
<td>Текстовая строка 3000 символов</td>
<td>Пояснения (применяется при повторной отправке извещения)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Текстовая строка 36 cимволов: символы A –F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessDate</td>
<td>Дата (в виде дд.мм.гггг чч:мм:сс)</td>
<td>Дата отправки запроса регистрации, по которому сформировано извещение</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/MessOwn</td>
<td>Текстовая строка</td>
<td>Отправитель запроса регистрации, по которому сформировано извещение</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ErrorCode</td>
<td>Число</td>
<td>Код ошибки. Отличен от 0</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ErrorName</td>
<td>Текстовая строка 3000 символов</td>
<td>Наименование ошибки\возникших затруднений</td>
</tr>
</table>

## 10. Теги, применяемые для формирования запроса на получение дополнительной информации в СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/FormNumber</td>
<td>Число</td>
<td>Номер сообщения</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OriginalDocumentGuid</td>
<td>Текстовая строка 36 cимволов: символы A –F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/CountDays</td>
<td>Число</td>
<td>Количество дней для предоставления ответа на запрос</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Description</td>
<td>Текстовая строка 3000 символов</td>
<td>Текст запроса на дополнительную информацию в СФМ</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/RequestDateTime</td>
<td>Дата в виде dd.mm.yyyy hh24:mi:ss</td>
<td>Дата и время направления запроса</td>
</tr>
</table>

## 11. Теги, применяемые для формирования извещения о принятии запроса дополнительной информации

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/FormNumber</td>
<td>Число</td>
<td>Номер сообщения</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/OriginalDocumentGuid</td>
<td>Текстовая строка 32 или 36 cимволов: символы A –F-a-f, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorCode</td>
<td>Число</td>
<td>Код ошибки. В случае извещения с отказом отличен от 0</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ErrorName</td>
<td>Текстовая строка 3000 символов</td>
<td>Наименование ошибки\возникших затруднений</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/AcceptanceDateTime</td>
<td>Дата в виде dd.mm.yyyy hh24:mi:ss</td>
<td>Дата и время принятия запроса</td>
</tr>
</table>

## 12. Теги, применяемые для формирования ответа на запрос дополнительной информации в СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/OriginalDocumentGuid</td>
<td>
Текстовая строка
36 cимволов: символы A –F, цифры от 0-9
</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data Root/Comment</td>
<td>Текстовая строка 3000 символов</td>
<td>Текст ответа на запроса дополнительной информации в СФМ</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/ResponseDateTime</td>
<td>Дата в виде dd.mm.yyyy hh24:mi:ss</td>
<td>Дата и время направления ответа</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/FileName</td>
<td>Текстовая строка 255 символов</td>
<td>Имя вложенного файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/Length</td>
<td>Число</td>
<td>Размер файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Name</td>
<td>Текстовая строка 255 символов</td>
<td>Имя порции вложенного файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Length</td>
<td>Число</td>
<td>Размер порции вложенного файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/ Root/Attachments/Attachment/ BrokenFilesInfo/BrokenFileInfo/Buffer</td>
<td>Строка в кодировке Base64</td>
<td>Содержимое порции вложенного файла</td>
</tr>
</table>

Примечание:

* нумерация соответствует реквизитам формы ФМ-1 приложения 1 к Правилам представления субъектами финансового мониторинга сведений и информации об операциях, подлежащих финансовому мониторингу, утвержденные постановлением Правительства Республики Казахстан от 23 ноября 2012 года № 1484.

** Правила представления субъектами финансового мониторинга сведений и информации об операциях, подлежащих финансовому мониторингу, и признаков определения подозрительной операции, утвержденные постановлением Правительства Республики Казахстан от 23 ноября 2012 года № 1484.

Расшифровка аббревиатур:

КФМ – Комитет по финансовому мониторингу Министерства финансов Республики Казахстан;

СФМ – субъекты финансового мониторинга;

ЭЦП – электронная цифровая подпись;

КАТО – классификатор административно - территориальных объектов;

ЕКНП – единый классификатор назначения платежей;

ОПФ – организационно- правовая форма;

ОКЭД – общий классификатор экономической деятельности.
