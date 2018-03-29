# Об утверждении Правил подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан

> *Сноска. Заголовок приказа в редакции приказа и.о. Министра информации и коммуникаций РК от 29.03.2018 № 121 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования).*

В соответствии с подпунктом 13) пункта 1 статьи 5 Закона Республики Казахстан от 7 января 2003 года «Об электронном документе и электронной цифровой подписи», ПРИКАЗЫВАЮ:

> *Сноска. Преамбула в редакции приказа Министра по инвестициям и развитию РК от 09.12.2015 № 1186 (вводится в действие со дня его первого официального опубликования).*

1. Утвердить прилагаемые Правила подтверждения подлинности иностранной электронной цифровой подписи доверенной третьей стороной Республики Казахстан.

2. Комитету связи, информатизации и информации Министерства по инвестициям и развитию Республики Казахстан (Сарсенов С.С.) обеспечить:

   1) в установленном законодательством порядке государственную регистрацию настоящего приказа в Министерстве юстиции Республики Казахстан;

   2) в течение десяти календарных дней после государственной регистрации настоящего приказа в Министерстве юстиции Республики Казахстан направление его копии на официальное опубликование в периодических печатных изданиях и информационно-правовой системе «Әділет» республиканского государственного предприятия на праве хозяйственного ведения «Республиканский центр правовой информации Министерства юстиции Республики Казахстан»;

   3) размещение настоящего приказа на интернет-ресурсе Министерства по инвестициям и развитию Республики Казахстан и на интранет-портале государственных органов;

   4) в течение десяти рабочих дней после государственной регистрации настоящего приказа в Министерстве юстиции Республики Казахстан представление в Юридический департамент Министерства по инвестициям и развитию Республики Казахстан сведений об исполнении мероприятий, предусмотренных подпунктами 1), 2) и 3) пункта 2 настоящего приказа.

3. Контроль за исполнением настоящего приказа возложить на вице-министра по инвестициям и развитию Республики Казахстан Жумагалиева А.К.

4. Настоящий приказ вводится в действие со дня истечения десяти календарных дней после дня его первого официального опубликования.

**Исполняющий обязанности Министра по инвестициям и развитию Республики Казахстан**

**Ж. Касымбек**

> *Утверждены приказом*  
> *исполняющего обязанности*  
> *Министра по инвестициям и*  
> *развитию Республики Казахстан*  
> *от 23 февраля 2015 года № 149*

## Правила подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан

> *Сноска. Правила в редакции приказа и.о. Министра информации и коммуникаций РК от 29.03.2018 № 121 (вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования).*

### Глава 1. Общие положения

1. Настоящие Правила подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан (далее – Правила), разработаны в соответствии с подпунктом 13) пункта 1 статьи 5 Закона Республики Казахстан от 7 января 2003 года «Об электронном документе и электронной цифровой подписи» (далее – Закон) и определяют порядок подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан.

2. В настоящих Правилах используются следующие основные понятия:

   1) список отозванных регистрационных свидетельств (далее – СОРС) – часть регистра регистрационных свидетельств, содержащая сведения о регистрационных свидетельствах, действие которых прекращено, их серийные номера, дату и причину отзыва (аннулирования);

   2) удостоверяющий центр – юридическое лицо, удостоверяющее соответствие открытого ключа электронной цифровой подписи закрытому ключу электронной цифровой подписи, а также подтверждающее достоверность регистрационного свидетельства;

   3) доверенная третья сторона Республики Казахстан (далее – ДТС РК) информационная система, осуществляющая в рамках трансграничного взаимодействия подтверждение подлинности иностранной электронной цифровой подписи и электронной цифровой подписи, выданной на территории Республики Казахстан;

   4) регистрационное свидетельство – документ на бумажном носителе или электронный документ, выдаваемый удостоверяющим центром для подтверждения соответствия электронной цифровой подписи требованиям, установленным Законом;

   5) сервис подтверждения подлинности регистрационных свидетельств (Validation of Public Key Certificates) (далее – VPKC) – сервис ДТС РК осуществляющий проверку принадлежности и действительности открытого ключа электронной цифровой подписи одного или нескольких регистрационных свидетельств;

   6) доверенная третья сторона иностранного государства (далее – ДТС иностранного государства) – организация, наделенная в соответствии с законодательством иностранного государства правом осуществлять деятельность в автоматизированном режиме по проверке электронной цифровой подписи в электронных документах в фиксированный момент времени в отношении лица, подписавшего электронный документ;

   7) квитанция проверки электронной цифровой подписи (далее – квитанция) – электронный документ, удостоверенный ЭЦП ДТС РК и подтверждающий подлинность ЭЦП;

   8) электронная цифровая подпись (далее – ЭЦП) – набор электронных цифровых символов, созданный средствами электронной цифровой подписи и подтверждающий достоверность электронного документа, его принадлежность и неизменность содержания;

   9) сервис подтверждения подлинности документов подписанных электронной цифровой подписью (Validation of Digitally Signed Document) (далее – VSD) – сервис ДТС РК осуществляющий проверку подлинности ЭЦП.

   10) XML (eXtensible Markup Language (далее – XML) - расширяемый язык разметки) – расширяемый язык разметки, используемый для хранения и передачи данных в структурированном и машиночитаемом формате.

3. Участниками информационного обмена с ДТС РК являются:

   1) удостоверяющие центры;

   2) ДТС иностранных государств;

   3) пользователи информационных систем, интегрированных с ДТС РК.

### Глава 2. Порядок подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан

4. ЭЦП сформированная с использованием регистрационных свидетельств, полученных в удостоверяющих центрах Республики Казахстан, проверяются информационными системами в соответствии с Правилами проверки подлинности электронной цифровой подписи, утвержденными приказом Министра по инвестициям и развитию Республики Казахстан от 9 декабря 2015 года № 1187 (зарегистрирован в Реестре государственной регистрации нормативных правовых актов за № 12864) (далее – Правила проверки подлинности ЭЦП).

   В случае если электронный документ направляется в информационную систему иностранных государств, ДТС РК выдает квитанцию на основе запросов от информационных систем Республики Казахстан, для подтверждения подлинности ЭЦП в иностранных государствах. ДТС РК перед выдачей квитанции осуществляет проверку ЭЦП и регистрационного свидетельства в соответствии с Правилами проверки подлинности ЭЦП, при этом ИС осуществляет проверки предусмотренные подпунктами 2), 3) и 4) пункта 1 статьи 10 Закона.

5. ЭЦП сформированная с использованием регистрационных свидетельств полученных в удостоверяющих центрах иностранных государств проверяются в ДТС РК, на основе запросов от иностранных информационных систем.

6. ДТС РК проверяет подлинность ЭЦП при выполнении следующих условий:

   1) проверяемый электронный документ удостоверен ЭЦП физического или юридического лица;

   2) в ДТС РК зарегистрирован ДТС иностранного государства или удостоверяющий центр, выдавший проверяемое регистрационное свидетельство.

7. Для проверки подлинности ЭЦП пользователь или ИС отправляет в ДТС РК, один из следующих запросов:

   1) электронный запрос VSD – согласно приложению 1 к настоящим Правилам;

   2) электронный запрос VPKC – согласно приложению 2 к настоящим Правилам;

   3) электронный запрос XML – согласно приложению 3 к настоящим Правилам.

      ДТС РК принимает запросы размером не более 100 мегабайт.

8. Формы электронного запроса, квитанции и схем данных основных реквизитов квитанции приведены в приложениях 1, 2, 3, 4 и 5 к настоящим Правилам.

9. На основании полученного ответа от удостоверяющего центра и (или) ДТС иностранного государства, ДТС РК формирует ответ в виде квитанции, являющейся необходимой и достаточной для подтверждения подлинности ЭЦП на территории Республики Казахстан.

10. Подтверждение подлинности ЭЦП и (или) регистрационного свидетельства ДТС РК осуществляется бесплатно.

11. Виды ответов от ДТС РК:

    1) квитанция со статусом «Проверено» («Подтверждено»), в случае положительной проверки;

    2) квитанция со статусом «Не проверено» («Не подтверждено»), в случае отрицательной проверки. При получении квитанции со статусом «Не проверено» пользователь информационной системы получает соответствующее оповещение через средства информационной системы;

    3) квитанция со статусом «Невозможно проверить» («Нерасшифровано», «ошибка», «отказ»), в случае несоответствия структуры электронного запроса VSD, либо отсутствия регистрации удостоверяющего центра, либо ДТС иностранного государства в ДТС РК.

       Подтверждение подлинности ЭЦП и (или) регистрационного свидетельства считается удостоверенной, в случае наличия квитанций со статусом «Проверено», полученной пользователем или ИС в ДТС РК.

12. ДТС РК хранит информацию о полученных запросах в базе данных, используя уникальные идентификаторы транзакций в течение пяти лет.

13. По истечении срока хранения информация о полученных запросах поступает на архивное хранение в ДТС РК.

> *Приложение 1*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной Республики Казахстан*

## Электронный запрос VSD

<table>
<tr>
<td>№ п/с</td>
<td>
Наименование
поля сообщения
</td>
<td>Тип поля сообщения</td>
<td>Смысловое содержание</td>
<td>Обязательность</td>
</tr>
<tr>
<td colspan="5">DVCSRequestInformation (запрос)</td>
</tr>
<tr>
<td>1.</td>
<td>requestInformation-&gt;version</td>
<td>integer</td>
<td>Версия запроса. По умолчанию 1</td>
<td>Нет</td>
</tr>
<tr>
<td>2.</td>
<td>requestInformation-&gt;service</td>
<td>ServiceType</td>
<td>
Тип сервиса.
VSD – 2
</td>
<td>Да</td>
</tr>
<tr>
<td>3.</td>
<td>requestInformation-&gt;nonce</td>
<td>integer</td>
<td>Зарезервированное поле (не используется)</td>
<td>Нет</td>
</tr>
<tr>
<td>4.</td>
<td>requestInformation-&gt;requestTime</td>
<td>DVCSTime</td>
<td>Может содержать одно из значений на выбор – время по UTC (genTime), метка времени (timeStampToken)</td>
<td>Нет</td>
</tr>
<tr>
<td>5.</td>
<td>requestInformation-&gt;requester</td>
<td>GeneralNames</td>
<td>Может содержать одно из значений на выбор – otherName, rfc822Name, dNSName, x400Address, directoryName, ediPartyName, uniformResourceIdentifier, iPAddress, registeredID</td>
<td>Нет</td>
</tr>
<tr>
<td>6.</td>
<td>requestInformation-&gt;requestPolicy</td>
<td>PolicyInformation</td>
<td>Политика запроса</td>
<td>Нет</td>
</tr>
<tr>
<td>7.</td>
<td>requestInformation-&gt;dvcs</td>
<td>GeneralNames</td>
<td>Может содержать одно из значений на выбор – otherName, rfc822Name, dNSName, x400Address, directoryName, ediPartyName, uniformResourceIdentifier, iPAddress, registeredID</td>
<td>Нет</td>
</tr>
<tr>
<td>8.</td>
<td>requestInformation-&gt;dataLocations</td>
<td>GeneralNames</td>
<td>Может содержать одно из значений на выбор – otherName, rfc822Name, dNSName, x400Address, directoryName, ediPartyName, uniformResourceIdentifier, iPAddress, registeredID</td>
<td>Нет</td>
</tr>
<tr>
<td>9.</td>
<td>requestInformation-&gt;extensions</td>
<td>Extensions</td>
<td>Дополнительная информация</td>
<td>Нет</td>
</tr>
<tr>
<td>10.</td>
<td>data</td>
<td>Data</td>
<td>Проверяемые данные</td>
<td>Да</td>
</tr>
<tr>
<td>11.</td>
<td>transactionIdentifier</td>
<td>GeneralName</td>
<td>Идентификатор транзакции</td>
<td>Да</td>
</tr>
</table>

> *Приложение 2*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной Республики Казахстан*

## Электронный запрос VPKC

<table>
<tr>
<td>№ п/с</td>
<td>
Наименование
поля сообщения
</td>
<td>Тип поля сообщения</td>
<td>Смысловое содержание</td>
<td>Обязательность</td>
</tr>
<tr>
<td colspan="5">DVCSRequestInformation (запрос)</td>
</tr>
<tr>
<td>1.</td>
<td>requestInformation-&gt;version</td>
<td>integer</td>
<td>Версия запроса. По умолчанию 1</td>
<td>Нет</td>
</tr>
<tr>
<td>2.</td>
<td>requestInformation-&gt;service</td>
<td>ServiceType</td>
<td>
Тип сервиса.
VPKC – 3
</td>
<td>Да</td>
</tr>
<tr>
<td>3.</td>
<td>requestInformation-&gt;nonce</td>
<td>integer</td>
<td>Зарезервированное поле (не используется)</td>
<td>Нет</td>
</tr>
<tr>
<td>4.</td>
<td>requestInformation-&gt;requestTime</td>
<td>DVCSTime</td>
<td>Может содержать одно из значений на выбор – время по UTC (genTime), метка времени (timeStampToken)</td>
<td>Нет</td>
</tr>
<tr>
<td>5.</td>
<td>requestInformation-&gt;requester</td>
<td>GeneralNames</td>
<td>Может содержать одно из значений на выбор – otherName, rfc822Name, dNSName, x400Address, directoryName, ediPartyName, uniformResourceIdentifier, iPAddress, registeredID</td>
<td>Нет</td>
</tr>
<tr>
<td>6.</td>
<td>requestInformation-&gt;requestPolicy</td>
<td>PolicyInformation</td>
<td>Политика запроса</td>
<td>Нет</td>
</tr>
<tr>
<td>7.</td>
<td>requestInformation-&gt;dvcs</td>
<td>GeneralNames</td>
<td>Может содержать одно из значений на выбор – otherName, rfc822Name, dNSName, x400Address, directoryName, ediPartyName, uniformResourceIdentifier, iPAddress, registeredID</td>
<td>Нет</td>
</tr>
<tr>
<td>8.</td>
<td>requestInformation-&gt;dataLocations</td>
<td>GeneralNames</td>
<td>Может содержать одно из значений на выбор – otherName, rfc822Name, dNSName, x400Address, directoryName, ediPartyName, uniformResourceIdentifier, iPAddress, registeredID</td>
<td>Нет</td>
</tr>
<tr>
<td>9.</td>
<td>requestInformation-&gt;extensions</td>
<td>Extensions</td>
<td>Дополнительная информация</td>
<td>Нет</td>
</tr>
<tr>
<td>10.</td>
<td>data</td>
<td>Data</td>
<td>Проверяемые данные</td>
<td>Да</td>
</tr>
<tr>
<td>11.</td>
<td>transactionIdentifier</td>
<td>GeneralName</td>
<td>Идентификатор транзакции</td>
<td>Да</td>
</tr>
</table>

> *Приложение 3*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной Республики Казахстан*

## Электронный запрос XML

<table>
<tr>
<td>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;xs:schema xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:doc=&quot;urn:EEC:SignedData:v1.0:
EDoc&quot; xmlns:ds=&quot;http://www.w3.org/2000/09/xmldsig#&quot; targetNamespace=
&quot;urn:EEC:SignedData:v1.0:EDoc&quot; elementFormDefault=&quot;qualified&quot; attributeFormDefault=&quot;unqualified&quot;&gt;
&lt;xs:import namespace=&quot;http://www.w3.org/2000/09/xmldsig#&quot; schemaLocation=
&quot;http://www.w3.org/TR/2002/REC-xmldsig-core-20020212/xmldsig-core-schema.xsd#&quot;/&gt;
&lt;xs:element name=&quot;SignedDoc&quot; type=&quot;doc:SignedDocType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Электронный документ&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;xs:complexType name=&quot;SignedDocType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Тип данных &quot;Электронный документ&quot;&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:sequence&gt;
&lt;xs:element name=&quot;Data&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Блок содержимого электронного документа&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexType&gt;
&lt;xs:complexContent&gt;
&lt;xs:extension base=&quot;doc:DataType&quot;&gt;
&lt;xs:attribute name=&quot;Id&quot; type=&quot;xs:ID&quot; use=&quot;required&quot;/&gt;
&lt;/xs:extension&gt;
&lt;/xs:complexContent&gt;
&lt;/xs:complexType&gt;
&lt;/xs:element&gt;
&lt;xs:element ref=&quot;ds:Signature&quot; minOccurs=&quot;0&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Квитанция доверенной третьей стороны&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;/xs:sequence&gt;
&lt;/xs:complexType&gt;
&lt;xs:complexType name=&quot;DataType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Тип блока содержимого электронного документа&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:sequence&gt;
&lt;xs:element ref=&quot;ds:Signature&quot; maxOccurs=&quot;unbounded&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Электронная цифровая подпись (электронная подпись)&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;xs:element name=&quot;SignedContent&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Блок подписываемых данных&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexType&gt;
&lt;xs:sequence&gt;
&lt;xs:any namespace=&quot;##any&quot; processContents=&quot;lax&quot; maxOccurs=&quot;unbounded&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Структура видов электронных документов (сведений)&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:any&gt;
&lt;/xs:sequence&gt;
&lt;xs:attribute name=&quot;Id&quot; type=&quot;xs:ID&quot; use=&quot;required&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Атрибут-идентификатор блока подписываемых данных&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:attribute&gt;
&lt;xs:attribute name=&quot;DocInstance&quot; type=&quot;xs:anyURI&quot; use=&quot;required&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Уникальный идентификатор электронного документа&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:attribute&gt;
&lt;/xs:complexType&gt;
&lt;/xs:element&gt;
&lt;/xs:sequence&gt;
&lt;/xs:complexType&gt;
&lt;/xs:schema&gt;
</td>
</tr>
</table>

> *Приложение 4*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной Республики Казахстан*

## Электронная квитанция

<table>
<tr>
<td>№ п/с</td>
<td>
Наименование
поля сообщения
</td>
<td>Тип поля сообщения</td>
<td>Смысловое содержание</td>
<td>Обязательность</td>
</tr>
<tr>
<td></td>
<td colspan="4">DVCSResponse(ответ), 1-й вариант ответа</td>
</tr>
<tr>
<td>1.</td>
<td>dvCertInfo-&gt;version</td>
<td>integer</td>
<td>
Версия запроса.
По умолчанию 1
</td>
<td>Нет</td>
</tr>
<tr>
<td>2.</td>
<td>dvCertInfo-&gt;dvReqInfo</td>
<td>DVCSRequestInformation</td>
<td>Информация о запросе</td>
<td>Да</td>
</tr>
<tr>
<td>3.</td>
<td>dvCertInfo-&gt;messageImprint</td>
<td>DigestInfo</td>
<td>Хэш-значение на данные из запроса</td>
<td>Да</td>
</tr>
<tr>
<td>4.</td>
<td>dvCertInfo-&gt;serialNumber</td>
<td>Integer</td>
<td>Уникальный идентификатор запроса</td>
<td>Да</td>
</tr>
<tr>
<td>5.</td>
<td>dvCertInfo-&gt;responseTime</td>
<td>DVCSTime</td>
<td>Может содержать одно из значений на выбор – время по UTC (genTime), метка времени (timeStampToken)</td>
<td>Да</td>
</tr>
<tr>
<td>6.</td>
<td>dvCertInfo-&gt;dvStatus</td>
<td>PKIStatusInfo</td>
<td>Статус ответа</td>
<td>Нет</td>
</tr>
<tr>
<td>7.</td>
<td>dvCertInfo-&gt;policy</td>
<td>PolicyInformation</td>
<td>Политика ответа</td>
<td>Нет</td>
</tr>
<tr>
<td>8.</td>
<td>dvCertInfo-&gt;reqSignature</td>
<td>SignerInfos</td>
<td>Подпись запроса</td>
<td>Нет</td>
</tr>
<tr>
<td>9.</td>
<td>dvCertInfo-&gt;certs</td>
<td>TargetEtcChain</td>
<td>Ргеистрационные свидетельства</td>
<td>Нет</td>
</tr>
<tr>
<td>10.</td>
<td>dvCertInfo-&gt;extensions</td>
<td>Extensions</td>
<td>Дополнительная информация</td>
<td>Нет</td>
</tr>
<tr>
<td colspan="5">DVCSResponse(ответ), 2-й вариант ответа</td>
</tr>
<tr>
<td>1.</td>
<td>dvErrorNote-&gt;transactionStatus</td>
<td>PKIStatusInfo</td>
<td>Статус ответа</td>
<td>Да</td>
</tr>
<tr>
<td>2.</td>
<td>dvErrorNote-&gt;transactionIdentifier</td>
<td>GeneralName</td>
<td>Идентификатор транзакции</td>
<td>Нет</td>
</tr>
</table>

> *Приложение 5*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной Республики Казахстан*

## Схема данных основных реквизитов квитанции

<table>
<tr>
<td>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;xs:schema xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:rcpt=&quot;urn:EEC:TTP:v1.0:receipt&quot; targetNamespace=&quot;urn:EEC:TTP:v1.0:receipt&quot; elementFormDefault=&quot;qualified&quot; attributeFormDefault=&quot;unqualified&quot;&gt;
&lt;xs:element name=&quot;Receipt&quot; type=&quot;rcpt:ReceiptType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Блок основных реквизитов квитанции&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;xs:complexType name=&quot;ReceiptType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Тип блока основных реквизитов квитанции&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:sequence&gt;
&lt;xs:element name=&quot;ReceiptId&quot; type=&quot;xs:anyURI&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Уникальный идентификатор сформированной квитанции&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;xs:element name=&quot;DocId&quot; type=&quot;xs:anyURI&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Идентификатор электронного документа&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;xs:element name=&quot;Report&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Блок сведений о результатах проверки&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexType&gt;
&lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
&lt;xs:element name=&quot;Success&quot; type=&quot;rcpt:SuccessType&quot;/&gt;
&lt;xs:element name=&quot;Error&quot; type=&quot;rcpt:ErrorType&quot;/&gt;
&lt;/xs:choice&gt;
&lt;/xs:complexType&gt;
&lt;/xs:element&gt;
&lt;xs:element name=&quot;AttachedData&quot; minOccurs=&quot;0&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Блок дополнительных сведений в формате XML&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexType&gt;
&lt;xs:sequence&gt;
&lt;xs:any namespace=&quot;##any&quot; processContents=&quot;lax&quot; maxOccurs=&quot;unbounded&quot;/&gt;
&lt;/xs:sequence&gt;
&lt;/xs:complexType&gt;
&lt;/xs:element&gt;
&lt;/xs:sequence&gt;
&lt;xs:attribute name=&quot;Id&quot; type=&quot;xs:ID&quot; use=&quot;required&quot;/&gt;
&lt;/xs:complexType&gt;
&lt;xs:complexType name=&quot;BaseReportType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Базовый тип элемента-отчета о проверке&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:attribute name=&quot;Reference&quot; type=&quot;xs:anyURI&quot; use=&quot;optional&quot;/&gt;
&lt;/xs:complexType&gt;
&lt;xs:complexType name=&quot;SuccessType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Тип элемента, указывающего, что проверка ДТС выполнена успешно&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexContent&gt;
&lt;xs:extension base=&quot;rcpt:BaseReportType&quot;/&gt;
&lt;/xs:complexContent&gt;
&lt;/xs:complexType&gt;
&lt;xs:complexType name=&quot;ErrorType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Тип контейнера описания ошибки&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexContent&gt;
&lt;xs:extension base=&quot;rcpt:BaseReportType&quot;&gt;
&lt;xs:sequence&gt;
&lt;xs:element name=&quot;ReasonCode&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Код ошибки&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:simpleType&gt;
&lt;xs:restriction base=&quot;xs:string&quot;&gt;
&lt;xs:enumeration value=&quot;Signature.Error&quot;/&gt;
&lt;xs:enumeration value=&quot;Signature.BadCertificate&quot;/&gt;
&lt;xs:enumeration value=&quot;Document.AuthenticityError&quot;/&gt;
&lt;/xs:restriction&gt;
&lt;/xs:simpleType&gt;
&lt;/xs:element&gt;
&lt;xs:element name=&quot;ReasonText&quot; type=&quot;xs:string&quot; &gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Текстовое описание ошибки&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;/xs:sequence&gt;
&lt;/xs:extension&gt;
&lt;/xs:complexContent&gt;
&lt;/xs:complexType&gt;
&lt;/xs:schema&gt;
</td>
</tr>
</table>
