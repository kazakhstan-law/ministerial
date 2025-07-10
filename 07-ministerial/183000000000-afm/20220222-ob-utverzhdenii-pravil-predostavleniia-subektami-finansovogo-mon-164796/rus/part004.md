---
part_of: ../rus.md
source: https://zan.gov.kz/client/#!/doc/164796/rus/10.07.2025
---

> *Приложение 2*  
> *к Правилам представления субъектами финансового мониторинга сведений и информации об операциях, подлежащих финансовому мониторингу*

## Формат XML информации, предоставляемой электронным способом субъектами финансового мониторинга

### 1. Типы сообщений в системе

<table>
<tr>
<td>№ п/п</td>
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
<td>Запрос регистрации субъектов финансового мониторинга</td>
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

### 2. Теги, обязательно присутствующие в сообщениях различного назначения

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>
/ExportData/SignedData/
Sender
</td>
<td>Текстовая строка до 32 символов: символы от A –Z, цифры от 0-9</td>
<td>
Отправитель.
1) Строка с наименованием организации-СФМ, выполнившего отправку сообщения в АФМ. Указывается, если отправителем сообщения является СФМ.
2) Строка «AFM». Указывается, ели отправителем сообщения является АФМ.
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/
Receiver
</td>
<td>Текстовая строка до 32 символов: символы от A –Z, цифры от 0-9</td>
<td>
Получатель.
1) Строка «AFM». Указывается, если получателем сообщения является АФМ.
2) Строка с наименованием организации-СФМ. Указывается, если получателем сообщения является СФМ.
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/
TieStamp
</td>
<td>Тип DateType (предоставляется в виде дд.мм.гггг чч24:мм:сс)</td>
<td>Время отправки документа</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Version</td>
<td>Текстовая строка 36 символов: символы A –F, цифры от 0-9</td>
<td>GUID версии документа в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/DocumentUniqueIdentifier</td>
<td>Текстовая строка 36 символов: символы A –F, цифры от 0-9</td>
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

_____________________

1 В извещениях о принятии вместо тега «Root» используется тег «Check».

### 3. Теги, применяемые для формирования информационного сообщения по Форме сведений и информации об операции, подлежащей финансовому мониторингу ФМ-1

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента *</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData</td>
<td></td>
<td>[2] Сведения о субъекте финансового мониторинга, направившего форму ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
PersonalData/FirstName
</td>
<td>Текстовая строка 100 символов</td>
<td>[2.7 (1)] Фамилия</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ SecondName</td>
<td>Текстовая строка 100 символов</td>
<td>[2.7 (2)] Имя</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
PersonalData/MiddleName
</td>
<td>Текстовая строка 100 символов</td>
<td>[2.7 (3)] Отчество (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ JobName</td>
<td>Текстовая строка 300 символов</td>
<td>[2.7.1] Должность ответственного должностного лица</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ Phone</td>
<td>в формате код города/номер телефона/номер внутреннего телефона через запяту</td>
<td>[2.8] Контактные телефоны</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ Email</td>
<td>Текстовая строка 100 символов</td>
<td>[2.9] Электронная почта</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationCode</td>
<td>Число</td>
<td>[2.1] Код субъекта финансового мониторинга. Нумерация и описания соответствуют Приложению 3 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationOPF</td>
<td>Число</td>
<td>[2.2 (1.1)] Организационная форма субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ Organisatio</td>
<td>Текстовая строка 300 символов</td>
<td>[2.2 (1.2)] Наименование субъекта финансового мониторинга</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/PersonalData/ OrganisationArea/
@Code
</td>
<td>Число</td>
<td>[2.5 (1)] Код области (согласно справочнику КАТО)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/PersonalData/ OrganisationCity/
@Code
</td>
<td>Число</td>
<td>[2.5 (3)] Код населенного пункта (город/поселок/село) (справочнику КАТО)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/PersonalData/ OrganisationDistrict/
@Code
</td>
<td>Число</td>
<td>[2.5 (2)] Код района (согласно справочнику КАТО)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PrsonalData/ OrganisationStreet</td>
<td>Текстовая строка 100 символов</td>
<td>[2.5 (4)] Наименование улицы/проспекта/микрорайона</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationHouse</td>
<td>Текстовая строка 100 символов</td>
<td>[2.5 (5)] Номер дома</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationOffice</td>
<td>Текстовая строка 100 символов</td>
<td>[2.5 (6)] Номер квартиры/офиса (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ OrganisationPostalIndex</td>
<td>Число</td>
<td>[2.5 (7)] Почтовый индекс</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PesonalData/ IINBIN</td>
<td>12 цифр</td>
<td>[2.4] ИИН/БИН</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/PersonalData/ AdditionalAcData</td>
<td></td>
<td>[2.6 – 2.6.3] Сведения о документе, удостоверяющем личность (для СФМ, являющимся физическим лицом)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/ AdditionalAcData/ FirstName</td>
<td>Текстовая строка</td>
<td>[2.2 (1.2.2)] Имя СФМ, являющегося физическим лицом или индивидуальным предпринимателем</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/ AdditionalAcData/ LastName</td>
<td>Текстовая строка</td>
<td>[2.2 (1.2.1)] Фамилия СФМ, являющегося физическим лицом или инд☐видуальным предпринимателем</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data /Root/PersonalData/ AdditionalAcData/ MiddleName</td>
<td>Текстовая строка</td>
<td>[2.2 (1.2.3)] Отчество СФМ, являющегося физическим лицом или индивидуальным предпринимателем</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ PersonalData/ AdditionalAcData/
@IsAc
</td>
<td>True или False</td>
<td>Атрибут, показывающий является ли СФМ, подающий отчет физическим лицом. Если нет, то теги соответствующие п.п.[2.6 – 2.6.3] Правил не указываются.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ PersonalData/ AdditionalAcData
/DocumentIdentity
</td>
<td>Число</td>
<td>[2.6] Код типа документа, удостоверяющего личность (для физических лиц). Нумерация и описания соответствуют Приложению 4 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
PersonalData/AdditionalAcData/
SeriesDocIdentity
</td>
<td>Строка до 50 символов</td>
<td>[2.6.1 (1)] Номер документа, удостоверяющего личность (для физических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
PersonalData/AdditionalAcData/
NumberDocIdentity
</td>
<td>Строка до 50 символов</td>
<td>[2.6.1 (2)] Серия документа, удостоверяющего личность (для физически☐ лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ PersonalData/ AdditionalAcData/
DateIssuance
</td>
<td>Дата (в виде дд.мм.гггг)</td>
<td>[2.6.3] Когда выдан документ, удостоверяющий личность (для физических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
PersonalData/AdditionalAcData/
DocumentIssued
</td>
<td>Строка до 300 символов</td>
<td>[2.6.2] Кем выдан документ, удостоверяющий личность (для физических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ MessageInformation</td>
<td></td>
<td>[1] Сведения о сообщении и [3] Информация об операции, подлежащейнансовому мониторингу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ MessageInformation/DocumentType</td>
<td>Число</td>
<td>[1.3] Вид документа – Нумерация и описания соответствуют п. 1.3 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Messagenformation/MessageNumbe
</td>
<td>Число</td>
<td>[1.1(1)] Номер формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/LastModifyDate
</td>
<td>Дата в виде dd.​mm.​yyyy</td>
<td>[1.2] Дата формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/TransactionDate
</td>
<td>Дата в виде dd.​mm.​yyyy hh24:m:ss</td>
<td>Время зав☐решения/начала/ приостановки операции СФМ. Отсутствует в случае указания числа 4 в п [1.4] Правил **.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/ViewOperationId
</td>
<td>Число</td>
<td>[3.2 (1)] Код вида операции - Нумерация и описания соответствуют Приложению 5 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/EknpId
</td>
<td>Число</td>
<td>[3.3 (1)] Код ЕКНП. Указывается идентификатор кода ЕКНП.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/EknpId/
@IsEknpNotSetup
</td>
<td>True или False</td>
<td>[3.3 (2)] Невозможно установить код ЕКНП - при значении True</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/ OperationNumber
</td>
<td>Текстовая строка 30 символов</td>
<td>[3.1] Номер операции</td>
</tr>
<tr>
<td>/ExportData/SignedParticipant/ IndividualIssueData/ Data/Root/MessageInformation/ DocOperationReason</td>
<td>Число</td>
<td>[3.8] Основание совершения операции. Нумерация и описания соответствуют Приложению 6 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ MessageInformation/ DocOperationDate</td>
<td>Текстовая строка в виде dd.​mm.​yyyy</td>
<td>[3.9 (1)] Дата документа, на основании которого осуществляется операции</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ MessageInformation/ DocOperationNumber</td>
<td>Текстовая строка 30 символов</td>
<td>[3.9 (2)] Номер документа, на основании которого осуществляется операция</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInforation/ CurrencyCodeId
</td>
<td>Число</td>
<td>[3.5] Код валюты операции в соответствии с Приложением 23 «Классификатор валют», утвержденным Решением КТС № 378.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ MessageInformation/AmountCurrency</td>
<td>Число</td>
<td>[3.6] Сумма операции в валюте ее проведения. Формат денежный - 99999999999999999999.99 (через точку)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/
AmountCurrencyTenge
</td>
<td>Число</td>
<td>[3.7] Сумма операции в тенге. Формат денежный - 99999999999999999999.99 (через точку).</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/
OperationStatusId
</td>
<td>Число</td>
<td>[1.4] Состояние операции. Нумерация и описание соответствуют п.1.4 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/ReasonFilingId
</td>
<td>Число</td>
<td>[1.5] Основание для подачи сообщения. Нумерация и описания соответствуют первому уровню п.1.5 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformaton/CounterMeasure
</td>
<td></td>
<td>[1.5] Мера противодействия при совпадении с перечнем организаций и лиц. Нумерация и описания соответствуют второму уровню пп. 4. п.1.5 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/SuspicionFirst
</td>
<td>Число</td>
<td>[3.10] Код признака подозрительности операции. Нумерация и описания соответствуют Приложению 7 к Правилам**. Реквизит обязателен для заполнения в случае указания пункта 2 в реквизите 1.5 Приложения 1 Правил**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInormation/SuspicionSecond
</td>
<td>Число</td>
<td>[3.11] 1-й дополнительный признак подозрительности. Нумерация и описания соответствуют Приложению 7 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/SuspicionThird
</td>
<td>Число</td>
<td>[3.12] 2-й дополнительный признак подозрительности. Нумерация и описания соответствуют Приложению 7 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/
DescriptionDifficulties
</td>
<td>Текстовая строка 1000 символов</td>
<td>[3.13] Описание возникших затруднений квалификации операции как подозрительной</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/MoreInformation
</td>
<td>Текстовая строка 1000 символов</td>
<td>[3.14] Дополнительная информация по операции</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/ParticipantCount
</td>
<td>Число</td>
<td>[3.4] Количество участников операции</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/MerchTypes
</td>
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
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/MerchRegnfo
</td>
<td>Строка 50 символов</td>
<td>[3.2 (2.2)] Регистрационный номер имущества</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
MessageInformation/ReferCount
</td>
<td></td>
<td>Количество связей с иными формами ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ References</td>
<td></td>
<td>[1.1 (2)] Сведения о связях с иными формами ФМ-1 (при наличии)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ References/Reference</td>
<td></td>
<td>[1.1 (2)] Связь с иной формой ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ References/Reference/ReferenceId</td>
<td>Число</td>
<td>Порядковый номер связи с иной формой</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
References/ Reference /ReferenceOperationNumber
</td>
<td>Строка 50 символов</td>
<td>[1.1 (2.1)] Номер связанной формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
References/Reference /ReferenceDocOperationDate
</td>
<td>Текстовая строка в виде dd.​mm.​yyyy</td>
<td>[1.1 (2.2)] Дата связанной формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
References/Reference /ReferenceDocOperationNumber
</td>
<td>Строка 50 символов</td>
<td>Номер операции в связанной форме</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ Participants</td>
<td></td>
<td>[4] Сведения об участниках операции, подлежащей финан☐овому мониторингу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ Participants/ Participant</td>
<td></td>
<td>[4] Сведения об участнике операции, подлежащей финансовому мониторингу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/MemberId</td>
<td>Число</td>
<td>[4.1] Участник. Нумерация и описания соответствуют п.4. ☐ Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ParticipantsView</td>
<td>Число</td>
<td>[4.3] Вид участника. Нумерация и описания соответствуют Приложению 6 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
ParticipantsType
</td>
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
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/IsClientSubject
</td>
<td>Число</td>
<td>[4.2] Клиент субъекта финансового мониторинга. Нумерация и описания соответствуют п.4.2 Приложения 1 к Правилам**. Указывается число «1», если не является клиентом СФМ, число «2», если является клиентом</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/Residence
</td>
<td>Строка 2 символа (смвольный код страны)</td>
<td>[4.4] Резидентство. Нумерация и описания соответствуют Приложению 22 «Классификатор стран мира», утвержденным Решением КТС № 378.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/ForeignPerson
</td>
<td>Число</td>
<td>[4.6] Иностранное публичное должностное лицо. Нумерация и описания соответствуют п.4.6 Приложения 1 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/CorrespondentBank
</td>
<td></td>
<td>[4.7] Банк участника операции</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
CorrespondentBank/
AccountNumber
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.7 (1.4)] Номер счета участника</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
CorrespondentBank/Name
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.7 (1.2)] Наименование банка/филиала</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
CorrespondentBank/Code
</td>
<td>Текстовая строка 50 символов</td>
<td>[4.7 (1.3)] Код банка/филиала</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ CorrespondentBank/BankAddress</td>
<td></td>
<td></td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
CorrespondentBank/BankCountry
</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>[4.7 (1.1)] Местонахождение банка. Нумерация и описание соответствуют Приложению 22 «Классификатор стран мира», утвержденным Решением КТС № 378.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
CorrespondentBank/BankCity
</td>
<td>Текстовая строка 50 символов</td>
<td>[4.7 (1.1)] Местонахождение филиала – в случае местонахождения филиала на территории Республики Казахстан. Указывается населенный пункт, в кот☐ром инициируется/завершается операция</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/CorrespondentBank/ BankOffshoreAddr
</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>[4.7 (1.1)] Страна оффшора в случае, если реквизит 3.2 «Код вида операции» имеет значение 611-634. Указывается идентификатор оффшорной зоны в соответствии с Постановлением Правления Агентства Республики Казахстан по регулированию и развитию финансового рынка от 24 февраля 2020 года № 8 «Об установлении Перечня оффшорных зон для целей банковской и страховой деятельности, деятельности профессиональных участников рынка ценных бумаг и иных лицензируемых видов деятельности на рынке ценных бумаг, деятельности акционерных инвестиционных фондов и деятельности организаций, осуществляющих микрофинансовую деятельность».</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
CorrespondentBank/@IsOffshore
</td>
<td>
True
или
False
</td>
<td>Вспомогательный признак нахождения филиала в оффшорной зоне</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/CorrespondentBank/
CorrespondentsInformations
</td>
<td></td>
<td>[4.7 (1.5)] Сведения о корреспондентских счетах, участвующих в операции</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/CorrespondentBank/
CorrespondentsInformations/
CorrespondentInformation
</td>
<td></td>
<td>[4.7 (1.5)] Сведения о корреспондентском счете, участвующем в операции</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ CorrespondentBank/CorrespondentsInformations/
CorrespondentInformation/BankName
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.7 (1.5.2)] Наименование банка</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ CorrespondentBank/CorrespondentsInformations/
CorrespondentInformation/
BankCountry
</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>
[4.7 (1.5.1)] Местонахождение банка.
Нумерация и описание соответствуют Приложению 22 «Классификатор стран мира», утвержденным Решением КТС № 378.
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/IndividualIssue
</td>
<td>Текстовая строка 32 символа</td>
<td>[4.13] ИИН/БИН</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/OKED
</td>
<td>Текстовая строка 5 символов</td>
<td>[4.12] ОКЭД. Код ОКЭД указывается в соответствии «Номенклатурой видов экономической деятельности (ОКЭД 5-тизначный)» утвержденный приказом Председателя Агентства Республики Казахстан по статистике от 20 мая 2008 года № 67, размещенный на официальном сайте Комитета по статистике Министерства национальной экономики Республики Казахстан.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/PhoneNumber
</td>
<td>в формате код города/номер телефона/номер внутреннего телефона через запятую</td>
<td>[4.22] Номер контактного телефона</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/Email
</td>
<td>Текстовая строка 100 символов</td>
<td>[4.23] Электронная почта</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
AdditionalInformation
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.25] Дополнительная информация об участнике операции</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
MoneyTransSys
</td>
<td>Число</td>
<td>[4.7 (1.2.1)] Наименование системы денежных переводов.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/Founders</td>
<td></td>
<td>[4.9] Учредители участника операции (для юридических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/Founders/
Founder
</td>
<td></td>
<td>[4.9] Учредитель участника операции (для юридических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/
Participant/Founders/Founder/
FounderType
</td>
<td>Число</td>
<td>
Вспомогательный признак типа учредителя:
1 – Юридическое лицо
2 – Физическое лицо
3 – Индивидуальный предприниматель
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/Founders/
Founder/FounderOPF
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.9 (1.1)] Организационная форма учредителя участника (заполняется для юридического лица)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/Founders/
Founder/Name
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.9 (2.1)] Наименование учредителя участника (заполняется для юридического лица)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/Founders/
Founder/FirstName
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.9 (1.2.2)] Имя учредителя участника (заполняется для учредителя физического лица)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
Founders/Founder/SecondName
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.9 (1.2.1)] Фамилия учредителя участника (заполняется для учредителя физического лица)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
Founders/Founder/MiddleName
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.9 (1.2.3)] Отчество учредителя участника (заполняется для учредителя физического лица)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
Founders/Founder/Residence
</td>
<td>Строка 2 символа (символьный код страны)</td>
<td>[4.9 (2)] Резидентство учредителя участника операции. Нумерация и описания соответствуют Приложению 22 «Классификатор стран мира», утвержденным Решением № 378.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/AdditionalPersonInfo</td>
<td></td>
<td>Дополнительная информация по участникам операции. Разбиение на юридические, физические лица и индивидуальных предпринимателей</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationUr</td>
<td></td>
<td>Дополнительная информация по участнику - юридическому лицу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationUr/ URAddress</td>
<td>Составной типа Address</td>
<td>[4.21] Юридический адрес. Описание приведено ниже в описании составных типов элементов.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationUr/ ACAddress</td>
<td>Составной типа Address</td>
<td>[4.24] Фактический адрес. Описание приведено ниже в описании составных типов элементов.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/
AdditionalInformationUr/FullName
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.8 (1.2)] Наименование участника операции (для участников юридических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
AdditionalPersonInfo/AdditionalInformationUr/ FullName/
@IsFullNameSetup
</td>
<td>True или False</td>
<td>[4.8 (2)] Невозможно установить наименование участника операции - при значении True (для участников юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationUr/ FirstHead</td>
<td></td>
<td>[4.10] Первый руководитель (для участников юридических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
AdditionalPersonInfo/
AdditionalInformationUr/
FirstHead/FirstName
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.10 (2)] Имя первого руководителя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationUr/ FirstHead/SecondName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.10 (1)] Фамилия первого руководителя</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationUr/ FirstHead/MiddleName</td>
<td>Текстовая строка 300 символов</td>
<td>[4.10 (3)] Отчество первого руководителя (при наличии)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationUr/
ParticipantOPF
</td>
<td>Число</td>
<td>[4.8 (1.1)] Организационная форма участника операции (для участников юридических лиц)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationAc</td>
<td></td>
<td>Дополнительная информация по участнику - физическому лицу</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationAc/ URAddress</td>
<td>Составной типа Address</td>
<td>[4.21] Юридический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/
AdditionalInformationAc/
ACAddress
</td>
<td>Составной типа Address</td>
<td>[4.24] Фактический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationAc
/FIO
</td>
<td></td>
<td>[4.14] Ф.И.О. (для физических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationAc/
FIO/FirstName
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.2)] Имя</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationAc/FIO/SecondName
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.1)] Фамилия</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/
AdditionalInformationAc/
FIO/MiddleName
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.3)] Отчество (при наличии)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationAc/FIO
@IsFioNotSetup
</td>
<td>True или False</td>
<td>[4.14 (2.1)] Невозможно установить - при значении True</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationAc/
PlaceBirth
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.20] Место рождения (для физических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationAc/
DateBirth
</td>
<td>Текстовая строка в виде dd.​mm.​yyyy</td>
<td>[4.19] Дата рождения (для физических лиц)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
AdditionalPersonInfo/AdditionalInformationAc/ DocumentIdentity
</td>
<td>Число</td>
<td>[4.15] Документ, удостоверяющий личность. Нумерация и описания соответствуют Приложению 4 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/
AdditionalPersonInfo/AdditionalInformationAc/ SeriesDocIdentity
</td>
<td>Текстовая строка 10 символов</td>
<td>[4.16 (2)] Серия документа, удостоверяющего личность</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationAc/NumberDocIdentity
</td>
<td>Текстовая строка 20 символов</td>
<td>[4.16 (1)] Номер документа, удостоверяющего личность</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Participants/Participant/AdditionalPersonInfo/ AdditionalInformationAc/
DocumentIssued
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.17] Кем выдан документ, удостоверяющий личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationAc/ DateIssuance</td>
<td>Текстовая строка в виде dd.​mm.​yyyy</td>
<td>[4.18] Когда выдан документ, удостоверяющий личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/AdditionalInformationIp</td>
<td></td>
<td>Дополнительная информация по индивидуальному предпринимателю - состав тегов аналогичен физическому лицу, кроме тега «ParticipantOPF» приведенного ниже. Данный тег располагается между тегами «FIO» и «PlaceBirth».</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/ URAddress</td>
<td>Составной типа Address</td>
<td>[4.21] Юридический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/ ACAddress</td>
<td>Составной типа Address</td>
<td>[4.24] Фактический адрес. Описание приведено ниже.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO</td>
<td></td>
<td>[4.14] Ф.И.О. (для индивидуальных предпринимателей)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
FIO/FirstName
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.2)] Имя</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/
AdditionalPersonInfo/ AdditionalInformationIp/FIO/
SecondName
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.1)] Фамилия</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
FIO/MiddleName
</td>
<td>Текстовая строка 1000 символов</td>
<td>[4.14 (1.3)] Отчество (при наличии)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/FIO/
@IsFioNotSetup
</td>
<td>True или False</td>
<td>[4.14 (2.1)] Невозможно установить - при значении True</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
PlaceBirth
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.20] Место рождения (для индивидуальных предпринимателей)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
DateBirth
</td>
<td>Текстовая строка в виде dd.​mm.​yyyy</td>
<td>[4.19] Дата рождения (для индивидуальных предпринимателей)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
DocumentIdentity
</td>
<td>Число</td>
<td>[4.15] Документ, удостоверяющий личность. Нумерация и описания соответствуют Приложению 4 к Правилам**.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
SeriesDocIdentity
</td>
<td>Текстовая строка 10 символов</td>
<td>[4.16 (2)] Серия документа, удостоверяющего личность</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/ NumberDocIdentity</td>
<td>Текстовая строка 20 символов</td>
<td>[4.16 (1)] Номер документа, удостоверяющего личность</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
DocumentIssued
</td>
<td>Текстовая строка 300 символов</td>
<td>[4.17] Кем выдан документ, удостоверяющий личность</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/Participants/ Participant/ AdditionalPersonInfo/ AdditionalInformationIp/
DateIssuance
</td>
<td>Текстовая строка в виде dd.​mm.​yyyy</td>
<td>[4.18] Когда выдан документ, удостоверяющий личность</td>
</tr>
</table>

### 4. Описание составных типов элементов

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
<td>Код страны. Нумерация и описания соответствуют Приложению 22 «Классификатор стран мира», утвержденным Решением КТС № 378.</td>
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

2 В извещениях о непринятии вместо тега «Check» используется тег «Root».

### 5. Теги, применяемые для формирования извещения о принятии/непринятии формы сведений и информации об операции, подлежащей финансовому мониторингу ФМ-1

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
Description
</td>
<td>Текстовая строка 3000 символов</td>
<td>Пояснения (применяется при повторной отправке извещения)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
OriginalDocumentGuid
</td>
<td>Текстовая строка 36 символов: символы A –F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Сheck/ ErrorCode</td>
<td>Число</td>
<td>Код ошибки. В случае извещения с отказом отличен от 0</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
ErrorName
</td>
<td>Текстовая строка 3000 символов</td>
<td>Наименование ошибки\возникших затруднений</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
AcceptanceDateTime
</td>
<td>Дата в виде dd.​mm.​yyyy hh24:mi:ss</td>
<td>Дата и время принятия (непринятия) формы ФМ-1</td>
</tr>
</table>

### 6. Теги, применяемые для формирования запроса регистрации СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ OrganisationData</td>
<td></td>
<td>Данные об СФМ, его учредителях и ответственных лицах</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/SystemId
</td>
<td>Число</td>
<td>Идентификатор зарегистрированного СФМ. Указывается только при корректировке или изменении регистрационных сведений. Значение должно соответствовать тегу /ExportData/SignedData/Data/Root/SystemId из уведомления об одобрении запроса регистрации в КФМ.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/CfmCode
</td>
<td>Число</td>
<td>Код субъекта финансового мониторинга. Нумерация и описания соответствуют Приложению 3 к Правилам**. (При успешной регистрации данное значение указывается в поле [2.1] Формы ФМ-1.)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/OpfCode
</td>
<td>Число</td>
<td>Код ОПФ субъекта финансового мониторинга. Нумерация и описания соответствуют классификатору организационно-правовых форм. При успешной регистрации данное значение указывается в поле [2.2 (1.1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/OrgName
</td>
<td>Текстовая строка 300 символов</td>
<td>Название субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.2 (1.2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/IINBIN
</td>
<td>12 цифр</td>
<td>ИИН/БИН субъекта финансового мониторинга (При успешной регистрации данное значение указывается в поле [2.4] Формы ФМ-1.)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/PostalIndex
</td>
<td>Текстовая строка 30 символов</td>
<td>Почтовый индекс субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.5 (7)] Формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/Area/@code
</td>
<td>Число</td>
<td>Код области согласно справочнику КАТО. При успешной регистрации данное значение указывается в поле [2.5 (1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/District/@code
</td>
<td>Число</td>
<td>Код района согласно справочнику КАТО. При успешной регистрации данное значение указывается в поле [2.5 (2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/City/@code
</td>
<td>Число</td>
<td>Код населенного пункта (город/поселок/село) согласно справочнику КАТО. При успешной регистрации данное значение указывается в поле [2.5 (3)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/Street
</td>
<td>Текстовая строка 100 символов</td>
<td>Наименование улицы/проспекта/мр-на. При успешной регистрации данное значение указывается в поле [2.5 (4)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/House
</td>
<td>Текстовая строка 100 символов</td>
<td>№ дома. При успешной регистрации данное значение указывается в поле [2.5 (5)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/Office
</td>
<td>Текстовая строка 100 символов</td>
<td>№ квартиры/офиса. При успешной регистрации данное значение указывается в поле [2.5 (6)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ OrganisationData/
AdditionalAcData
</td>
<td></td>
<td>Дополнительная информация о физическом лице, являющемся субъектом финансового мониторинга</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OrganisationData/AdditionalAcData/
@IsAc
</td>
<td>True или False</td>
<td>Атрибут, показывающий является ли субъект финансового мониторинга, подающий отчет физическим лицом. Если нет, то теги в /ExportData/SignedData/ Data/Root/OrganisationData/ AdditionalAcData не указываются.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ OrganisationData/
AdditionalAcData/FirstName
</td>
<td>Текстовая строка 100 символов</td>
<td>Имя физического лица, являющегося субъектом финансового мониторинга При успешной регистрации данное значение указывается в поле [2.2 (1.2.2)] Формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData/
LastName
</td>
<td>Текстовая строка 100 символов</td>
<td>Фамилия физического лица, являющегося субъектом финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.2 (1.2.1)] Формы ФМ-1</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ OrganisationData/ AdditionalAcData/MiddleName</td>
<td>Текстовая строка 100 символов</td>
<td>Отчество физического лица, являющегося субъектом финансового мониторинга/ При успешной регистрации данное значение указывается в поле [2.2 (1.2.3)] Формы ФМ-1</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData/
DocumentIdentity
</td>
<td>Число</td>
<td>Код типа документа, удостоверяющего личность (для физических лиц). Нумерация и описания соответствуют Приложению 4 к Правилам**. При успешной регистрации данное значение указывается в поле [2.6] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData/
SeriesDocIdentity
</td>
<td>Текстовая строка 50 символов</td>
<td>Номер документа удостоверяющего личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.1 (1)] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData/
NumberDocIdentity
</td>
<td>Текстовая строка 50 символов</td>
<td>Серия документа удостоверяющего личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.1 (2)] Формы ФМ-1.</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData/ DateIssuance</td>
<td>Дата (в виде дд.мм.гггг)</td>
<td>
Когда выдан документ, удостоверяющий личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.3] Формы
ФМ-1.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ OrganisationData/AdditionalAcData/ DocumentIssued</td>
<td>Текстовая строка 300 символов</td>
<td>
Кем выдан документ, удостоверяющий личность (для физических лиц). При успешной регистрации данное значение указывается в поле [2.6.2] Формы
ФМ-1.
</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ OrganisationData/Persons</td>
<td></td>
<td>Информация об ответственных лицах субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ OrganisationData/Persons/Person</td>
<td></td>
<td>Информация об ответственном лице субъекта финансового мониторинга</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/ FirstName</td>
<td>Текстовая строка 100 символов</td>
<td>
Имя ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7(2)] Формы
ФМ-1.
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
LastName
</td>
<td>Текстовая строка 100 символов</td>
<td>
Фамилия ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7(1)] Формы
ФМ-1.
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
MiddleName
</td>
<td>Текстовая строка 100 символов</td>
<td>
Отчество ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7(3)] Формы
ФМ-1.
</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
JobName
</td>
<td>Текстовая строка 300 символов</td>
<td>Должность ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.7.1] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
Phone
</td>
<td>Текстовая строка 300 символов в формате код города/номер телефона/номер внутреннего телефона через запятую</td>
<td>Телефон ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.8] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
Email
</td>
<td>Текстовая строка 100 символов</td>
<td>Адрес электронной почты ответственного лица субъекта финансового мониторинга. При успешной регистрации данное значение указывается в поле [2.9] Формы ФМ-1.</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
Certificate
</td>
<td>До 32Кб</td>
<td>Сертификат открытого ключа ответственного лица субъекта финансового мониторинга</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
Certificate/@Name
</td>
<td>Текстовая строка 50 символов</td>
<td>Название сертификата открытого ключа ответственного лица субъекта финансового мониторинга</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/OrganisationData/ Persons/Person/
Certificate/@Size
</td>
<td>Число</td>
<td>Размер сертификата открытого ключа ответственного лица субъекта финансового мониторинга</td>
</tr>
</table>

### 7. Теги, применяемые для формирования квитанции о доставке запроса регистрации в АФМ

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

### 8. Теги, применяемые для формирования уведомления о положительном результате рассмотрения запроса регистрации СФМ

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
<td>Текстовая строка 36 cимволов: символы A–F, цифры от 0-9</td>
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

### 9. Теги, применяемые для формирования извещения об отрицательном результате рассмотрения запроса на регистрацию СФМ

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
<td>Текстовая строка 36 cимволов: символы A–F, цифры от 0-9</td>
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

### 10. Теги, применяемые для формирования запроса на получение дополнительной информации в СФМ

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
<td>
/ExportData/SignedData/Data/Root/
OriginalDocumentGuid
</td>
<td>Текстовая строка 36 cимволов: символы A–F, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
CountDays
</td>
<td>Число</td>
<td>Количество дней для предоставления ответа на запрос</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Description
</td>
<td>Текстовая строка 3000 символов</td>
<td>Текст запроса на дополнительную информацию в СФМ</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
RequestDateTime
</td>
<td>Дата в виде dd.​mm.​yyyy hh24:mi:ss</td>
<td>Дата и время направления запроса</td>
</tr>
</table>

### 11. Теги, применяемые для формирования извещения о принятии запроса дополнительной информации

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
<td>
/ExportData/SignedData/Data/Сheck/
OriginalDocumentGuid
</td>
<td>Текстовая строка 32 или 36 cимволов: символы A–F-a-f, цифры от 0-9</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
ErrorCode
</td>
<td>Число</td>
<td>Код ошибки. В случае извещения с отказом отличен от 0</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
ErrorName
</td>
<td>Текстовая строка 3000 символов</td>
<td>Наименование ошибки\возникших затруднений</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Сheck/
AcceptanceDateTime
</td>
<td>Дата в виде dd.​mm.​yyyy hh24:mi:ss</td>
<td>Дата и время принятия запроса</td>
</tr>
</table>

### 12. Теги, применяемые для формирования ответа на запрос дополнительной информации в СФМ

<table>
<tr>
<td>Расположение тега в документе</td>
<td>Тип элемента</td>
<td>Описание элемента</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
OriginalDocumentGuid
</td>
<td>
Текстовая строка
36 cимволов: символы A–F, цифры от 0-9
</td>
<td>GUID родительского сообщения в формате ХХХХХХХХ-ХХХХ-ХХХХ-ХХХХ-ХХХХХХХХХХХХ (шестнадцатеричное число в верхнем регистре с дефисами)</td>
</tr>
<tr>
<td>
/ExportData/SignedData/Data/Root/
Comment
</td>
<td>Текстовая строка 3000 символов</td>
<td>Текст ответа на запрос дополнительной информации в СФМ</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/ ResponseDateTime</td>
<td>Дата в виде dd.​mm.​yyyy hh24:mi:ss</td>
<td>Дата и время направления ответа</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/ Attachment/FileName</td>
<td>Текстовая строка 255 символов</td>
<td>Имя вложенного файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/ Attachment/Length</td>
<td>Число</td>
<td>Размер файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/ Attachment/BrokenFilesInfo/BrokenFileInfo/Name</td>
<td>Текстовая строка 255 символов</td>
<td>Имя порции вложенного файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/ Attachment/BrokenFilesInfo/BrokenFileInfo/Length</td>
<td>Число</td>
<td>Размер порции вложенного файла</td>
</tr>
<tr>
<td>/ExportData/SignedData/Data/Root/Attachments/ Attachment/BrokenFilesInfo/BrokenFileInfo/Buffer</td>
<td>Строка в кодировке Base64</td>
<td>Содержимое порции вложенного файла</td>
</tr>
</table>

Примечание:

* нумерация соответствует реквизитам формы ФМ-1 приложения 1 к настоящим Правилам;

** настоящие Правила.

Расшифровка аббревиатур:

КАТО – классификатор административно - территориальных объектов;

АФМ – Агентство Республики Казахстан по финансовому мониторингу;

СФМ – субъекты финансового мониторинга;

ЕКНП – единый классификатор назначения платежей;

ОПФ – организационно- правовая форма;

ОКЭД – общий классификатор экономической деятельности;

ЭЦП – электронная цифровая подпись.

> *Приложение 3*  
> *к Правилам представления*  
> *субъектами финансового*  
> *мониторинга сведений и*  
> *информации об операциях,*  
> *подлежащих финансовому*  
> *мониторингу*

> *Форма*

## Извещение о принятии или непринятии формы сведений и информации об операции, подлежащей финансовому мониторингу ФМ-1

```
___________________________________________________________________
                                                  (уполномоченный орган)
извещает_________________________________________________________
                     (наименование субъекта финансового мониторинга)
о ___________________________ формы ФМ-1 № ____ от _______________.
             (принятии/непринятии)
Причина непринятия (указывается только в случае непринятия формы ФМ-1)
____________________________________________________________________.
В связи с этим _________________________________________ необходимо:
                       (наименование субъекта финансового мониторинга)
          1. Устранить причины направления в ____________________________
                                                                                  (уполномоченный орган)
информации, представленной в искаженном виде или неполном объеме.
          2. В течение 1 рабочего дня со дня получения _______________________
                                                                         (субъект финансового мониторинга)
настоящего извещения исправить непринятое  _________________________
                                                                                    (уполномоченный орган)
сообщение об операции, подлежащей финансовому мониторингу, представить
его повторно в соответствии с положениями Порядка представления
субъектами финансового мониторинга сведений и информации по операциям,
подлежащим финансовому мониторингу.
```

```
__________________________           _____________       _____________________
 (Фамилия, имя, отчество (при                    (подпись)        (расшифровка подписи)
    наличии) уполномоченного
лица уполномоченного органа)
```

Дата и время принятия или непринятия формы ФМ-1:___________________

> *Приложение 4*  
> *к Правилам представления субъектами финансового мониторинга сведений и информации об операциях, подлежащих финансовому мониторингу*

## Справочник кодов видов субъектов финансового мониторинга

> *Сноска. Приложение 4 с изменениями, внесенными приказами Председателя Агентства РК по финансовому мониторингу от 30.03.2024 № 2 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования); от 24.09.2024 № 4 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования); от 01.04.2025 № 5 (вводится в действие с 10.07.2025).*

<table>
<tr>
<td>Код</td>
<td>Наименование</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>011</td>
<td>Банки</td>
</tr>
<tr>
<td>013</td>
<td>Обменные пункты</td>
</tr>
<tr>
<td>014</td>
<td>Дочерние организации национального управляющего холдинга в сфере агропромышленного комплекса</td>
</tr>
<tr>
<td>015</td>
<td>Ипотечные организации</td>
</tr>
<tr>
<td>016</td>
<td>Иные организации, осуществляющие отдельные виды банковских операций</td>
</tr>
<tr>
<td>022</td>
<td>Фондовые биржи</td>
</tr>
<tr>
<td>023</td>
<td>Товарные биржи</td>
</tr>
<tr>
<td>024</td>
<td>Биржевые брокеры, осуществляющие свою деятельность на товарной бирже и совершающие сделки с биржевыми товарами</td>
</tr>
<tr>
<td>025</td>
<td>Клиринговые центры товарных бирж</td>
</tr>
<tr>
<td>031</td>
<td>Страховые (перестраховочные) организации</td>
</tr>
<tr>
<td>032</td>
<td>Страховые брокеры</td>
</tr>
<tr>
<td>033</td>
<td>Общество взаимного страхования</td>
</tr>
<tr>
<td>034</td>
<td>Экспортно-кредитное агентство Казахстана</td>
</tr>
<tr>
<td>042</td>
<td>Единый накопительный пенсионный фонд</td>
</tr>
<tr>
<td>043</td>
<td>Добровольные накопительные пенсионные фонды</td>
</tr>
<tr>
<td>051</td>
<td>Профессиональные участники рынка ценных бумаг</td>
</tr>
<tr>
<td>052</td>
<td>Центральный депозитарий</td>
</tr>
<tr>
<td>061</td>
<td>Нотариусы, осуществляющие нотариальные действия с деньгами и (или) иным имуществом</td>
</tr>
<tr>
<td>071</td>
<td>Адвокаты</td>
</tr>
<tr>
<td>072</td>
<td>Независимые специалисты по юридическим вопросам</td>
</tr>
<tr>
<td>073</td>
<td>Юридические консультанты</td>
</tr>
<tr>
<td>081</td>
<td>Аудиторские организации</td>
</tr>
<tr>
<td>082</td>
<td>Бухгалтерские организации и профессиональные бухгалтеры, осуществляющие предпринимательскую деятельность в сфере бухгалтерского учета</td>
</tr>
<tr>
<td>092</td>
<td>Организаторы лотереи</td>
</tr>
<tr>
<td>093</td>
<td>Казино</td>
</tr>
<tr>
<td>094</td>
<td>Залы игровых автоматов</td>
</tr>
<tr>
<td>095</td>
<td>Букмекерские конторы</td>
</tr>
<tr>
<td>096</td>
<td>Тотализаторы</td>
</tr>
<tr>
<td>101</td>
<td>Операторы почты, оказывающие услуги по переводу денег</td>
</tr>
<tr>
<td>110</td>
<td>Микрофинансовые организации</td>
</tr>
<tr>
<td>111</td>
<td>Кредитные товарищества</td>
</tr>
<tr>
<td>130</td>
<td>Индивидуальные предприниматели и юридические лица, осуществляющие лизинговую деятельность в качестве лизингодателя без лицензии</td>
</tr>
<tr>
<td>140</td>
<td>Ломбарды</td>
</tr>
<tr>
<td>150</td>
<td>Индивидуальные предприниматели и юридические лица, осуществляющие операции с драгоценными металлами и драгоценными камнями, ювелирными изделиями из них</td>
</tr>
<tr>
<td>160</td>
<td>Индивидуальные предприниматели и юридические лица, оказывающие посреднические услуги при осуществлении сделок купли-продажи недвижимого имущества</td>
</tr>
<tr>
<td>171</td>
<td>Фонд социального медицинского страхования</td>
</tr>
<tr>
<td>172</td>
<td>Платежные организации</td>
</tr>
<tr>
<td>173</td>
<td>Участники Международного финансового центра «Астана»</td>
</tr>
<tr>
<td>174</td>
<td>Филиалы банков-нерезидентов Республики Казахстан</td>
</tr>
<tr>
<td>175</td>
<td>Филиалы страховых (перестраховочных) организаций-нерезидентов Республики Казахстан</td>
</tr>
<tr>
<td>176</td>
<td>Филиалы страховых брокеров- нерезидентов Республики Казахстан</td>
</tr>
<tr>
<td>177</td>
<td>Лица, осуществляющие выпуск и обращение обеспеченных цифровых активов</td>
</tr>
</table>

> *Приложение 5 к Правилам*  
> *предоставления субъектами*  
> *финансового мониторинга*  
> *сведений и информации об*  
> *операциях, подлежащих*  
> *финансовому мониторингу*

## Справочник кодов документов, удостоверяющих личность

> *Сноска. Приложение 5 в редакции приказа Председателя Агентства РК по финансовому мониторингу от 28.09.2023 № 6 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования).*

<table>
<tr>
<td>Код</td>
<td>Наименование документов, удостоверяющих личность</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>01</td>
<td>Удостоверение личности гражданина Республики Казахстан</td>
</tr>
<tr>
<td>02</td>
<td>Паспорт гражданина Республики Казахстан</td>
</tr>
<tr>
<td>03</td>
<td>Заграничный паспорт</td>
</tr>
<tr>
<td>04</td>
<td>Вид на жительство иностранца в Республике Казахстан</td>
</tr>
<tr>
<td>05</td>
<td>Удостоверение лица без гражданства</td>
</tr>
<tr>
<td>06</td>
<td>Дипломатический паспорт Республики Казахстан</td>
</tr>
<tr>
<td>07</td>
<td>Служебный паспорт Республики Казахстан</td>
</tr>
<tr>
<td>08</td>
<td>Удостоверение беженца</td>
</tr>
<tr>
<td>09</td>
<td>Удостоверение личности моряка Республики Казахстан</td>
</tr>
<tr>
<td>010</td>
<td>Свидетельство о рождении</td>
</tr>
<tr>
<td>011</td>
<td>Свидетельство на возвращение</td>
</tr>
<tr>
<td>012</td>
<td>Удостоверение личности, выданное иностранным государством</td>
</tr>
</table>

> *Приложение 6 к Правилам*  
> *предоставления субъектами*  
> *финансового мониторинга*  
> *сведений и информации об*  
> *операциях, подлежащих*  
> *финансовому мониторингу*

## Справочник кодов видов операций, подлежащих финансовому мониторингу

> *Сноска. Приложение 6 в редакции приказа Председателя Агентства РК по финансовому мониторингу от 28.09.2023 № 6 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования).*

<table>
<tr>
<td>Код</td>
<td>Наименование</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>0111</td>
<td>Получение выигрыша в наличной форме по результатам проведения пари</td>
</tr>
<tr>
<td>0112</td>
<td>Получение выигрыша в электронной форме по результатам проведения пари</td>
</tr>
<tr>
<td>0121</td>
<td>Получение выигрыша в наличной форме по результатам проведения азартной игры в игорных заведениях</td>
</tr>
<tr>
<td>0122</td>
<td>Получение выигрыша в электронной форме по результатам проведения азартной игры в игорных заведениях</td>
</tr>
<tr>
<td>0131</td>
<td>Получение выигрыша в наличной форме по результатам проведения лотереи</td>
</tr>
<tr>
<td>0132</td>
<td>Получение выигрыша в электронной форме по результатам проведения лотереи</td>
</tr>
<tr>
<td>0211</td>
<td>Покупка клиентом иностранной валюты через обменные пункты в наличной форме</td>
</tr>
<tr>
<td>0221</td>
<td>Продажа клиентом наличной иностранной валюты через обменные пункты в наличной форме</td>
</tr>
<tr>
<td>0311</td>
<td>Получение денег по чеку в наличной форме</td>
</tr>
<tr>
<td>0321</td>
<td>Получение денег по векселю в наличной форме</td>
</tr>
<tr>
<td>0511</td>
<td>Снятие с банковского счета клиента денег</td>
</tr>
<tr>
<td>0521</td>
<td>Зачисление на банковский счет клиента денег</td>
</tr>
<tr>
<td>0530</td>
<td>Выдача клиенту наличных денег</td>
</tr>
<tr>
<td>0540</td>
<td>Прием от клиента наличных денег</td>
</tr>
<tr>
<td>0623</td>
<td>Зачисление или перевод на банковский счет клиента денег, осуществляемые физическим или юридическим лицом, имеющим соответственно регистрацию, место жительства или место нахождения в оффшорной зоне, а равно владеющим счетом в банке, зарегистрированном в оффшорной зоне</td>
</tr>
<tr>
<td>0633</td>
<td>Зачисление или перевод денег клиентом в пользу физических или юридических лиц, имеющих регистрацию, место жительства или место нахождения в оффшорной зоне, а равно владеющих счетом в банке, зарегистрированном в оффшорной зоне</td>
</tr>
<tr>
<td>0640</td>
<td>Операции клиента с деньгами и (или) иным имуществом с физическими или юридическими лицами, имеющими регистрацию, место жительства или место нахождения в оффшорной зоне, а равно владеющими счетом в банке, зарегистрированном в оффшорной зоне</td>
</tr>
<tr>
<td>0711</td>
<td>Переводы денег за границу на счета (во вклады), открытые на анонимного владельца в наличной или безналичной форме</td>
</tr>
<tr>
<td>0721</td>
<td>Поступление денег из-за границы со счета (вклада), открытого на анонимного владельца в наличной или безналичной форме</td>
</tr>
<tr>
<td>0911</td>
<td>Платежи и переводы денег, осуществляемые клиентом в пользу другого лица на безвозмездной основе, в наличной или безналичной форме</td>
</tr>
<tr>
<td>1011</td>
<td>Приобретение в наличной форме культурных ценностей</td>
</tr>
<tr>
<td>1012</td>
<td>Продажа в наличной форме культурных ценностей</td>
</tr>
<tr>
<td>1021</td>
<td>Ввоз в Республику Казахстан культурных ценностей</td>
</tr>
<tr>
<td>1022</td>
<td>Вывоз из Республики Казахстан культурных ценностей</td>
</tr>
<tr>
<td>1111</td>
<td>Операции, совершаемые юридическими лицами, с момента государственной регистрации которых прошло менее трех месяцев, в наличной или безналичной форме</td>
</tr>
<tr>
<td>1211</td>
<td>Ввоз в Республику Казахстан наличной валюты, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1212</td>
<td>Ввоз в Республику Казахстан документарных ценных бумаг на предъявителя, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1213</td>
<td>Ввоз в Республику Казахстан векселей, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1214</td>
<td>Ввоз в Республику Казахстан чеков, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и Национальным оператором почты</td>
</tr>
<tr>
<td>1221</td>
<td>Вывоз из Республики Казахстан наличной валюты, за исключением вывоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1222</td>
<td>Вывоз из Республики Казахстан документарных ценных бумаг на предъявителя, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1223</td>
<td>Вывоз из Республики Казахстан векселей, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1224</td>
<td>Вывоз из Республики Казахстан чеков, за исключением ввоза, осуществляемого Национальным Банком Республики Казахстан, банками и национальным оператором почты</td>
</tr>
<tr>
<td>1311</td>
<td>Осуществление страховой выплаты в наличной форме</td>
</tr>
<tr>
<td>1321</td>
<td>Получение страховой премии в наличной форме</td>
</tr>
<tr>
<td>1411</td>
<td>Внесение добровольных пенсионных взносов в накопительные пенсионные фонды в наличной форме</td>
</tr>
<tr>
<td>1421</td>
<td>Перечисление добровольных пенсионных взносов в накопительные пенсионные фонды в наличной форме</td>
</tr>
<tr>
<td>1431</td>
<td>Осуществление пенсионных выплат из накопительных пенсионных фондов за счет добровольных пенсионных взносов в наличной форме</td>
</tr>
<tr>
<td>1511</td>
<td>Получение имущества по договору финансового лизинга в наличной и безналичной форме</td>
</tr>
<tr>
<td>1521</td>
<td>Предоставление имущества по договору финансового лизинга в наличной и безналичной форме</td>
</tr>
<tr>
<td>1611</td>
<td>Сделки по оказанию услуги подряда в наличной форме</td>
</tr>
<tr>
<td>1621</td>
<td>Сделки по оказанию услуги перевозки в наличной форме</td>
</tr>
<tr>
<td>1631</td>
<td>Сделки по оказанию услуги транспортной экспедиции в наличной форме</td>
</tr>
<tr>
<td>1641</td>
<td>Сделки по оказанию услуги хранения в наличной форме</td>
</tr>
<tr>
<td>1651</td>
<td>Сделки по оказанию услуги комиссии в наличной форме</td>
</tr>
<tr>
<td>1661</td>
<td>Сделки по оказанию услуги доверительного управления имуществом в наличной форме</td>
</tr>
<tr>
<td>1671</td>
<td>Сделки по оказанию иных услуг, за исключением услуг подряда, перевозки, транспортной экспедиции, хранения, комиссии и доверительного управления имуществом, в наличной форме</td>
</tr>
<tr>
<td>1711</td>
<td>Покупка клиентом драгоценных металлов и драгоценных камней, ювелирных изделий из них в наличной и безналичной форме</td>
</tr>
<tr>
<td>1721</td>
<td>Продажа клиентом драгоценных металлов и драгоценных камней, ювелирных изделий из них в наличной и безналичной форме</td>
</tr>
<tr>
<td>1811</td>
<td>Сделки с недвижимым имуществом, результатом совершения которой является переход права собственности на такое имущество</td>
</tr>
<tr>
<td>1911</td>
<td>Сделки с облигациями и государственными ценными бумагами, за исключением операций репо на организованном рынке методом открытых торгов, в наличной или безналичной форме</td>
</tr>
<tr>
<td>2020</td>
<td>Сделки с акциями и паями паевых инвестиционных фондов, за исключением операций репо на организованном рынке методом открытых торгов, в наличной или безналичной форме</td>
</tr>
<tr>
<td>2110</td>
<td>Совершение ломбардами операций с деньгами, ценными бумагами, драгоценными металлами и драгоценными камнями, ювелирными изделиями из них и иными ценностями (кроме монет национальной валюты, изготовленных из драгоценных металлов) в наличной или безналичной форме</td>
</tr>
<tr>
<td>2200</td>
<td>Операции клиентов, получивших заем по программам финансирования субъектов предпринимательства за счет средств Национального фонда Республики Казахстан в рамках облигационных займов субъектов квазиосударственного сектора, действующих на период совершения операции, в наличной или безналичной форме</td>
</tr>
<tr>
<td>2300</td>
<td>
Операции, относящиеся по своему характеру к трансграничному платежу и трансграничному переводу с банковского счета клиента денег в безналичной форме
Трансграничным является платеж или перевод между участниками, находящимся в разных странах
</td>
</tr>
<tr>
<td>2301</td>
<td>
Операции, относящиеся по своему характеру к трансграничному платежу и трансграничному переводу на банковский счет клиента денег в безналичной форме
Трансграничным является платеж или перевод между участниками, находящимся в разных странах
</td>
</tr>
<tr>
<td>2302</td>
<td>Операции, относящиеся по своему характеру к трансграничному платежу и переводу с банковского счета клиента денег в безналичной форме, ранее поступивших на счет клиента (в том числе, через счета третьих лиц) из иностранного государства</td>
</tr>
<tr>
<td>6010</td>
<td>Получение физическим лицом, включенным в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма, денег в виде оплаты трудового отпуска и заработной платы</td>
</tr>
<tr>
<td>6020</td>
<td>Получение физическим лицом, включенным в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма, денег в виде пенсии, расходов на служебные командировки, стипендии, пособия, иной социальной выплаты</td>
</tr>
<tr>
<td>6030</td>
<td>Платежи и переводы физического лица, включенного в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма, по уплате налогов, коммунальных и социальных платежей, других обязательных платежей в бюджет, пеней и штрафов</td>
</tr>
<tr>
<td>6040</td>
<td>Зачисление денег на банковский счет организации или физического лица, включенного в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма</td>
</tr>
<tr>
<td>6055</td>
<td>Зачисление денег на банковский счет организации, бенефициарным собственником которой является лицо, включенное в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма</td>
</tr>
<tr>
<td>6060</td>
<td>Операции с деньгами и (или) иным имуществом организаций и физических лиц, включенных в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма на основании решения суда за исключением операций, предусмотренных в следующих кодах: 6010,6020,6030,6040,6055</td>
</tr>
<tr>
<td>6061</td>
<td>Операции с деньгами и (или) иным имуществом организаций и физических лиц, включенных в перечень организаций и лиц, связанных с финансированием распространения оружия массового уничтожения</td>
</tr>
<tr>
<td>6062*</td>
<td>Операция, подлежащая финансовому мониторингу, не относящаяся ни к одному из кодов видов операции</td>
</tr>
<tr>
<td>6064</td>
<td>Частичная или полная отмена применяемых мер по замораживанию операций с деньгами и (или) иным имуществом в отношении физического лица, включенного в перечень организаций и лиц, связанных с финансированием терроризма и экстремизма по основаниям, предусмотренным подпунктом 7) пункта 4 статьи 12 Закона Республики Казахстан «О противодействии легализации (отмыванию) доходов, полученных преступным путем, и финансированию терроризма» (далее – Закон)</td>
</tr>
<tr>
<td>6065*</td>
<td>Частичная или полная отмена применяемых мер по замораживанию операций с деньгами и (или) иным имуществом в отношении физического лица, включенного в перечень организаций и лиц, связанных с финансированием распространения оружия массового уничтожения по основаниям, предусмотренным пунктом 5 статьи 12-1 Закона</td>
</tr>
</table>

*применяется для операции, которые признаны подозрительными.

> *Приложение 7 к Правилам*  
> *предоставления субъектами*  
> *финансового мониторинга*  
> *сведений и информации об*  
> *операциях, подлежащих*  
> *финансовому мониторингу*

## Справочник кодов видов участников и сделок с деньгами и (или) иным имуществом

> *Сноска. Приложение 7 в редакции приказа Председателя Агентства РК по финансовому мониторингу от 28.09.2023 № 6 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования).*

<table>
<tr>
<td>Код вида участника</td>
<td>Наименование вида участника</td>
<td>Код вида сделки</td>
<td>Наименование вида сделки</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
</tr>
<tr>
<td rowspan="2">01</td>
<td rowspan="2">Продавец</td>
<td>01</td>
<td>Договор купли-продажи недвижимости</td>
</tr>
<tr>
<td>02</td>
<td rowspan="2">Договор купли-продажи товара или услуги</td>
</tr>
<tr>
<td rowspan="2">02</td>
<td rowspan="2">Покупатель</td>
<td rowspan="2">03</td>
</tr>
<tr>
<td>Договор купли-продажи иного имущества</td>
</tr>
<tr>
<td>03</td>
<td>Даритель</td>
<td rowspan="2">04</td>
<td rowspan="2">Договор дарения</td>
</tr>
<tr>
<td>04</td>
<td>Одаряемый</td>
</tr>
<tr>
<td>05</td>
<td>Получатель ренты</td>
<td rowspan="4">05</td>
<td rowspan="4">Договор имущественного найма (аренды)</td>
</tr>
<tr>
<td>06</td>
<td>Плательщик ренты</td>
</tr>
<tr>
<td>07</td>
<td>Арендодатель</td>
</tr>
<tr>
<td>08</td>
<td>Арендатор</td>
</tr>
<tr>
<td>09</td>
<td>Лизингодатель</td>
<td rowspan="2">06</td>
<td rowspan="2">Договор лизинга</td>
</tr>
<tr>
<td>10</td>
<td>Лизингополучатель</td>
</tr>
<tr>
<td>11</td>
<td>Ссудодатель</td>
<td rowspan="2">07</td>
<td rowspan="2">Договор безвозмездного пользования имуществом</td>
</tr>
<tr>
<td>12</td>
<td>Ссудополучатель</td>
</tr>
<tr>
<td>13</td>
<td>Заказчик</td>
<td rowspan="5">08</td>
<td rowspan="5">Договор подряда</td>
</tr>
<tr>
<td>14</td>
<td>Подрядчик</td>
</tr>
<tr>
<td>15</td>
<td>Проектировщик</td>
</tr>
<tr>
<td>16</td>
<td>Изыскатель</td>
</tr>
<tr>
<td>17</td>
<td>Исполнитель</td>
</tr>
</table>

<table>
<tr>
<td>18</td>
<td>Отправитель (транспортная деятельность)</td>
<td rowspan="5">09</td>
<td rowspan="5">Договор перевозки транспортной экспедиции</td>
</tr>
<tr>
<td>19</td>
<td>Перевозчик</td>
</tr>
<tr>
<td>20</td>
<td>Получатель (транспортная деятельность)</td>
</tr>
<tr>
<td>21</td>
<td>Экспедитор</td>
</tr>
<tr>
<td>22</td>
<td>Заимодатель</td>
</tr>
<tr>
<td>23</td>
<td>Заемщик</td>
<td rowspan="2">10</td>
<td rowspan="2">Договор займа</td>
</tr>
<tr>
<td>24</td>
<td>Кредитор</td>
</tr>
<tr>
<td>25</td>
<td>Финансовый агент</td>
<td rowspan="2">11</td>
<td rowspan="2">Кредитный договор</td>
</tr>
<tr>
<td>26</td>
<td>Клиент (факторинг)</td>
</tr>
<tr>
<td>27</td>
<td>Бенефициар</td>
<td rowspan="3">12</td>
<td rowspan="3">Договор финансирования под уступку денежного требования (факторинг)</td>
</tr>
<tr>
<td>28</td>
<td>Принципал</td>
</tr>
<tr>
<td>29</td>
<td>Вкладчик</td>
</tr>
<tr>
<td rowspan="3">30</td>
<td rowspan="3">Эмитент</td>
<td>13</td>
<td>Договор банковского счета</td>
</tr>
<tr>
<td>14</td>
<td>Договор перевода денег</td>
</tr>
<tr>
<td rowspan="2">15</td>
<td rowspan="2">Договор банковского вклада</td>
</tr>
<tr>
<td rowspan="2">31</td>
<td rowspan="2">Владелец</td>
</tr>
<tr>
<td rowspan="2">16</td>
<td rowspan="2">Иной договор банковского обслуживания</td>
</tr>
<tr>
<td>32</td>
<td>Залогодатель</td>
</tr>
<tr>
<td>33</td>
<td>Залогодержатель</td>
<td rowspan="2">17</td>
<td rowspan="2">Договор залога</td>
</tr>
<tr>
<td>34</td>
<td>Хранитель</td>
</tr>
<tr>
<td>35</td>
<td>Поклажедатель</td>
<td rowspan="2">18</td>
<td rowspan="2">Договор хранения</td>
</tr>
<tr>
<td>36</td>
<td>Страховщик</td>
</tr>
<tr>
<td>37</td>
<td>Страхователь</td>
<td rowspan="3">19</td>
<td rowspan="3">Договор страхования</td>
</tr>
<tr>
<td>38</td>
<td>Застрахованный</td>
</tr>
<tr>
<td>39</td>
<td>Доверитель</td>
</tr>
<tr>
<td>40</td>
<td>Поверенный</td>
<td>20</td>
<td rowspan="2">Договор поручения</td>
</tr>
<tr>
<td rowspan="2">41</td>
<td rowspan="2">Комитент</td>
<td rowspan="2">21</td>
</tr>
<tr>
<td>Договор поручительства</td>
</tr>
<tr>
<td>42</td>
<td>Комиссионер</td>
<td rowspan="2">22</td>
<td rowspan="2">Договор комиссии</td>
</tr>
<tr>
<td>43</td>
<td>Учредитель управления</td>
</tr>
<tr>
<td>44</td>
<td>Доверительный управляющий</td>
<td rowspan="2">23</td>
<td rowspan="2">Договор доверительного управления имуществом</td>
</tr>
<tr>
<td>45</td>
<td>Правообладатель</td>
</tr>
<tr>
<td rowspan="3">46</td>
<td rowspan="3">Пользователь</td>
<td>24</td>
<td>Договор о передаче патентных прав</td>
</tr>
<tr>
<td>25</td>
<td>Договор о создании и использовании результатов интеллектуальной творческой деятельности</td>
</tr>
<tr>
<td rowspan="2">26</td>
<td rowspan="2">Лицензионный или сублицензионный договор на использование изобретения, полезной модели и/или промышленного образца</td>
</tr>
<tr>
<td>47</td>
<td>Лицензиат</td>
</tr>
<tr>
<td>48</td>
<td>Патентообладатель</td>
<td rowspan="3">27</td>
<td rowspan="3">Договор комплексной предпринимательской лицензии (франчайзинг)</td>
</tr>
<tr>
<td rowspan="2">49</td>
<td>Организатор лотереи,</td>
</tr>
<tr>
<td>тотализатора</td>
</tr>
<tr>
<td rowspan="2">50</td>
<td>Участник лотереи,</td>
<td rowspan="5">28</td>
<td rowspan="5">Иной договор, соглашение или контракт</td>
</tr>
<tr>
<td>тотализатора</td>
</tr>
<tr>
<td>51</td>
<td>Поставщик</td>
</tr>
<tr>
<td>52</td>
<td>Производитель</td>
</tr>
<tr>
<td rowspan="2">53</td>
<td rowspan="2">Наймодатель</td>
</tr>
<tr>
<td rowspan="3">29</td>
<td rowspan="3">Сделка без основополагающего документа</td>
</tr>
<tr>
<td>54</td>
<td>Наниматель</td>
</tr>
<tr>
<td>55</td>
<td>Иной участник</td>
</tr>
<tr>
<td>56</td>
<td>Вкладчик</td>
<td rowspan="2">30</td>
<td rowspan="2">Договор о пенсионном обеспечении за счет обязательных пенсионных взносов, обязательных профессиональных пенсионных взносов, добровольных пенсионных взносов</td>
</tr>
<tr>
<td>57</td>
<td>Получатель</td>
</tr>
<tr>
<td>58</td>
<td>Отправитель собственных средств</td>
<td rowspan="2">31</td>
<td rowspan="2">Перевод собственных средств</td>
</tr>
<tr>
<td>59</td>
<td>Получатель собственных средств</td>
</tr>
<tr>
<td>60</td>
<td>Инвестор</td>
<td rowspan="2">32</td>
<td rowspan="2">Инвестиционный договор</td>
</tr>
<tr>
<td>61</td>
<td>Получатель инвестиций</td>
</tr>
<tr>
<td>62</td>
<td>Головная компания</td>
<td rowspan="2">33</td>
<td rowspan="2">Переводы между головной компанией и филиалом</td>
</tr>
<tr>
<td>63</td>
<td>Филиал компании</td>
</tr>
</table>

> *Приложение 8*  
> *к Правилам представления*  
> *субъектами финансового*  
> *мониторинга сведений и*  
> *информации об операциях,*  
> *подлежащих финансовому*  
> *мониторингу*

> *Форма*

## Запрос на предоставление необходимой информации, сведений и документов

В соответствии с подпунктом 1) пункта 1 статьи 17 и пунктами 3-1 статьи 10 Закона Республики Казахстан «О противодействии легализации (отмыванию) доходов, полученных преступным путем, и финансированию терроризма»

```
 ____________________________________________________________________
                                                  (уполномоченный орган)
```

просит представить следующие информацию, сведения и документы об операциях клиентов и бенефициарных собственниках клиентов/ по международным переводам денег, проведенным через систему денежных переводов:

1. ________________;

2. ________________.

```
_________________________               __________             ____________________
(Фамилия, имя, отчество (при             (подпись)                 (расшифровка подписи)
  наличии) уполномоченного
лица уполномоченного органа)
```

Контактный телефон: __________________

Дата и время направления запроса: __________________

> *Приложение 9*  
> *к Правилам представления*  
> *субъектами финансового*  
> *мониторинга сведений и*  
> *информации об операциях,*  
> *подлежащих финансовому*  
> *мониторингу*

> *Форма*

## Извещение о принятии запроса на предоставление необходимой информации, сведений и документов

```
____________________________________________________________________
                    (наименование субъекта финансового мониторинга)
извещает ____________________________________________________________
                                                (уполномоченный орган)
```

о принятии запроса на предоставление необходимой информации, сведений

и документов по операциям, подлежащим финансовому мониторингу № ______

от __________.

```
_____________________________       _______________    ____________________
   (Фамилия, имя, отчество (при                 (подпись)           (расшифровка подписи)
    наличии) ответственного лица
субъекта финансового мониторинга)
```

Дата и время принятия запроса _________________________

> *Приложение 10*  
> *к Правилам представления*  
> *субъектами финансового*  
> *мониторинга сведений и*  
> *информации об операциях,*  
> *подлежащих финансовому*  
> *мониторингу*

> *Форма*

## Ответ на запрос на предоставление необходимых информации, сведений и документов

В соответствии с пунктами 3-1 и 3-2 статьи 10 Закона Республики Казахстан «О противодействии легализации (отмыванию) доходов, полученных преступным путем, и финансированию терроризма»

```
____________________________________________________________________
                         (наименование субъекта финансового мониторинга)
```

направляет следующие информацию, сведения* и документы на запрос № ______ от ______________:

1. ________________;

2. ________________.

Приложение на _________________ листах.

```
____________________________      ____________         _____________________
  (Фамилия, имя, отчество (при            (подпись)               (расшифровка подписи)
   наличии) ответственного лица
субъекта финансового мониторинга)
```

Контактный телефон: _____________________

Дата и время направления ответа: ____________________

*выписки по банковскому счету клиента предоставляются согласно приложению к настоящей форме в формате Microsoft Excel, иные сведения предоставляются по форме, определяемой субъектом финансового мониторинга самостоятельно.

> *Приложение*  
> *к форме «Ответ на запрос на*  
> *предоставление необходимых*  
> *информации, сведений и документов»*

> *Форма*

## Сведения, предоставляемые субъектами финансового мониторинга, в рамках запроса уполномоченного органа

<table>
<tr>
<th>Дата и время операции</th>
<th>Валюта операции</th>
<th>Виды операции (категория документа)</th>
<th>Наименование СДП (при наличии)</th>
<th>Сумма в валюте ее проведения</th>
<th>Сумма в тенге</th>
<th>Наименование/ФИО плательщика</th>
<th>ИИН/БИН плательщика</th>
<th>Резидентство плательщика</th>
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

Продолжение таблицы

<table>
<tr>
<th>Банк плательщика</th>
<th>Номер счета плательщика</th>
<th>Наименование/ФИО получателя</th>
<th>ИИН/БИН получателя</th>
<th>Резидентство получателя</th>
<th>Банк получателя</th>
<th>Номер счета получателя</th>
<th>Код назначения платежа</th>
<th>Назначение платежа</th>
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

Расшифровка аббревиатур:

ИИН/БИН – индивидуальный идентификационный номер/бизнес-идентификационный номер СДП – система денежных переводов

ФИО – фамилия, имя, отчество

> *Приложение 11*  
> *к Правилам представления*  
> *субъектами финансового*  
> *мониторинга сведений и*  
> *информации об операциях,*  
> *подлежащих финансовому*  
> *мониторингу*

> *Форма*

## Обращение о продлении срока по запросу на предоставление необходимой информации, сведений и документов

```
 ____________________________________________________________________
                    (наименование субъекта финансового мониторинга)
обращается в     ______________________________________________________
                                                            (уполномоченный орган)
о продлении срока, указанного в запросе на предоставление необходимой
информации, сведений и документов № _______, от ___________ до _________
рабочих дней.
____________________________________________________________________
                                        (обоснование продления срока)
```

```
__________________________             _____________           ___________________
(Фамилия, имя, отчество (при               (подпись)              (расшифровка подписи)
наличии) ответственного лица
субъекта финансового мониторинга)
```

> *Приложение 12*  
> *к Правилам представления*  
> *субъектами финансового*  
> *мониторинга сведений и*  
> *информации об операциях,*  
> *подлежащих финансовому*  
> *мониторингу*

> *Форма*

> *Наименование субъекта*  
> *финансового мониторинга*

## Уведомление №____ об отсутствии необходимости в приостановлении подозрительной операции

Агентством Республики Казахстан по финансовому мониторингу (далее – Агентство) в соответствии с пунктом 3 статьи 13 Закона Республики Казахстан «О противодействии легализации (отмыванию) доходов, полученных преступным путем, и финансированию терроризма» по сообщению № ___от «__» ________ 20__ года принято решение об отсутствии необходимости в приостановлении подозрительной операции.

Основание: приказ Агентства от «__» __________ 20__ года № ___.

```
__________________________        ___________             ____________________
(Фамилия, имя, отчество (при           (подпись)              (расшифровка подписи)
наличии) ответственного лица
уполномоченного органа)
```

«__» ________ 20__ г.
