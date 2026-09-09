# Об утверждении Правил подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан

В соответствии с пунктом 3 статьи 57 Цифрового Кодекса Республики Казахстан, ПРИКАЗЫВАЮ:

<a id="p1"></a>

1. Утвердить прилагаемые Правила подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан.

<a id="p2"></a>

2. Признать утратившим силу некоторые приказы согласно приложению, к настоящему приказу.

<a id="p3"></a>

3. Департаменту цифровых решений Министерства искусственного интеллекта и цифрового развития Республики Казахстан в установленном законодательством Республики Казахстан порядке обеспечить:

   1) государственную регистрацию настоящего приказа в Министерстве юстиции Республики Казахстан;

   2) размещение настоящего приказа на интернет-ресурсе Министерства искусственного интеллекта и цифрового развития Республики Казахстан после его официального опубликования;

   3) в течение десяти рабочих дней после государственной регистрации настоящего приказа в Министерстве юстиции Республики Казахстан представление в Юридический департамент Министерства искусственного интеллекта и цифрового развития Республики Казахстан сведений об исполнении мероприятий, предусмотренных подпунктами 1) и 2) настоящего пункта.

<a id="p4"></a>

4. Контроль за исполнением настоящего приказа возложить на курирующего вице-министра искусственного интеллекта и цифрового развития Республики Казахстан.

<a id="p5"></a>

5. Настоящий приказ вводится в действие по истечении десяти календарных дней после дня его первого официального опубликования.

**Испоняющий обязанности министра искусственного интеллекта и цифрового развития Республики Казахстан**

**Р. Коняшкин**

> *Утверждены приказом*  
> *Испоняющий обязанности*  
> *министра искусственного*  
> *интеллекта и цифрового развития*  
> *Республики Казахстан*  
> *от 9 сентября 2026 года*  
> *№ 547/НҚ*

## Правила подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан

### Глава 1. Общие положения

<a id="an1_p1"></a>

1. Настоящие Правила подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан (далее – Правила), разработаны в соответствии с пунктом 3 статьи 57 Цифрового Кодекса Республики Казахстан (далее – Кодекс) и определяют порядок подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан.

<a id="an1_p2"></a>

2. В настоящих Правилах используются следующие основные понятия:

   1) доверенная третья сторона Республики Казахстан (далее – ДТС РК) – цифровая система, осуществляющая в рамках трансграничного взаимодействия подтверждение подлинности иностранной электронной цифровой подписи и электронной цифровой подписи, выданной на территории Республики Казахстан;

   2) расширяемый язык разметки XML (eXtensible Markup Language, далее – XML) – используемый для хранения и передачи данных в структурированном и машиночитаемом формате;

   3) удостоверяющий центр (далее – УЦ) – юридическое лицо, созданное в соответствии с законодательством Республики Казахстан, которое подтверждает достоверность сертификатов открытых ключей электронной цифровой подписи, принадлежность и действительность открытых ключей электронной цифровой подписи;

   4) иностранный удостоверяющий центр (далее – иностранный УЦ) – юридическое лицо, созданное в соответствии с законодательством иностранного государства, которое подтверждает достоверность сертификатов открытых ключей электронной цифровой подписи, принадлежность и действительность открытых ключей электронной цифровой подписи;

   5) доверенная третья сторона иностранного государства (далее – ДТС иностранного государства) – цифровая система, в соответствии с законодательством иностранного государства осуществляющая деятельность в автоматизированном режиме по проверке электронной цифровой подписи в электронных документах в фиксированный момент времени в отношении лица, подписавшего электронный документ;

   6) электронная цифровая подпись (далее – ЭЦП) – цифровая запись (набор цифровых данных), созданная с использованием закрытого ключа электронной цифровой подписи и средств электронной цифровой подписи, подтверждающая достоверность электронного документа, его принадлежность и неизменность содержания;

   7) сертификат открытого ключа электронной цифровой подписи (далее – сертификат) – цифровая запись, удостоверенная электронной цифровой подписью удостоверяющего центра, которая служит для подтверждения соответствия электронной цифровой подписи требованиям, установленным Кодексом.

   8) сервис подтверждения подлинности документов, подписанных электронной цифровой подписью (Validation of Digitally Signed Document, далее – VSD) – сервис доверенной третьей стороны Республики Казахстан, осуществляющий проверку подлинности электронной цифровой подписи, а также формат электронного запроса, направляемого в указанный сервис;

   9) квитанция проверки электронной цифровой подписи (далее – квитанция) – цифровая запись, удостоверенная электронной цифровой подписью доверенной третьей стороны Республики Казахстан, которая служит для подтверждения подлинности электронной цифровой подписи.

<a id="an1_p3"></a>

3. Участниками информационного обмена с ДТС РК являются:

   1) УЦ;

   2) иностранные УЦ;

   3) ДТС иностранных государств;

   4) пользователи цифровых систем, интегрированных с ДТС РК.

### Глава 2. Порядок подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан

<a id="an1_p4"></a>

4. Подлинность ЭЦП, сформированной с использованием сертификата, выданного УЦ осуществляющим свою деятельность на территории Республики Казахстан, проверяются цифровыми системами в соответствии с Правилами формирования и проверки подлинности электронной цифровой подписи согласно пункту 1 статьи 61 Кодекса. В случае если электронный документ направляется в цифровую систему иностранных государств, ДТС РК выдает квитанцию на основе запросов от цифровых систем Республики Казахстан, для подтверждения подлинности ЭЦП в иностранных государствах. ДТС РК перед выдачей квитанции осуществляет проверку подлинности ЭЦП и сертификата в соответствии с Правилами формирования и проверки подлинности электронной цифровой подписи.

<a id="an1_p5"></a>

5. Подлинность ЭЦП, сформированной с использованием сертификатов, выданных иностранным УЦ, проверяется в ДТС РК на основе запросов от пользователей и цифровых систем.

<a id="an1_p6"></a>

6. ДТС РК проверяет подлинность ЭЦП при выполнении следующих условий:

   1) проверяемый электронный документ удостоверен ЭЦП физического или юридического лица;

   2) в ДТС РК зарегистрирован ДТС иностранного государства или УЦ иностранного государства, выдавший проверяемый сертификат.

<a id="an1_p7"></a>

7. Для проверки подлинности ЭЦП пользователь или цифровая система отправляет в ДТС РК, один из следующих запросов:

   1) электронный запрос VSD – по форме согласно приложению 1 к настоящим Правилам;

   2) электронный запрос XML – по форме согласно приложению 2 к настоящим Правилам.

<a id="an1_p8"></a>

8. По результатам обработки запросов, указанных в пункте 7 настоящих Правил, ДТС РК формирует электронную квитанцию проверки ЭЦП согласно приложению 3 к настоящим Правилам. Схема данных основных реквизитов электронной квитанции проверки ЭЦП приведена в приложении 4 к настоящим Правилам.

<a id="an1_p9"></a>

9. Электронная квитанция проверки ЭЦП, сформированная на основании ответа УЦ, иностранного УЦ и (или) ДТС иностранного государства, подтверждает результат проверки подлинности ЭЦП и является необходимой и достаточной для подтверждения подлинности ЭЦП на территории Республики Казахстан.

<a id="an1_p10"></a>

10. Подтверждение подлинности ЭЦП и (или) сертификата ДТС РК осуществляется бесплатно.

<a id="an1_p11"></a>

11. Виды ответов от ДТС РК:

    1) квитанция со статусом «Проверено» («Подтверждено»), в случае положительной проверки;

    2) квитанция со статусом «Не проверено» («Не подтверждено»), в случае отрицательной проверки. При получении квитанции со статусом «Не проверено» пользователь цифровой системы получает соответствующее оповещение через средства цифровой системы;

    3) квитанция со статусом «Невозможно проверить» («нерасшифровано», «ошибка», «отказ»), в случае несоответствия структуры электронного запроса VSD, либо отсутствия регистрации УЦ иностранного государства либо ДТС иностранного государства в ДТС РК.

       Подлинность ЭЦП и (или) сертификата считается подтвержденной ДТС РК, в случае наличия квитанции со статусом «Проверено», полученной пользователем или цифровой системой от ДТС РК.

<a id="an1_p12"></a>

12. ДТС РК хранит информацию о полученных запросах, процессе их обработки и сформированные квитанции проверки электронной цифровой подписи (уникальные идентификаторы транзакций, сведения о проверенных ЭЦП, сертификаты, технические данные использованные для проверки, такие как сведения о статусе отзыва сертификатов, квитанции проверки ЭЦП, выданные ДТС иностранных государств, и другие данные достаточные для подтверждения результата проверки ЭЦП) в базе данных, используя уникальные идентификаторы транзакций в течение пяти лет. Проверявшиеся электронные документы и их содержимое, передаваемые в запросах (в поле data запроса VSD согласно Приложению 1 и в блоке подписываемых данных XML‑запроса согласно Приложению 2 к настоящим Правилам), не сохраняются.

<a id="an1_p13"></a>

13. По истечении срока хранения информация о полученных запросах, процессе их обработки и сформированные квитанции проверки ЭЦП поступает на архивное хранение в ДТС РК.

<a id="an1_p14"></a>

14. ДТС РК осуществляет проверку сертификатов, выданных удостоверяющими центрами, аккредитованными в Республике Казахстан для возможности предоставления квитанции с результатами проверки в ДТС иностранного государства.

<a id="an1_p15"></a>

15. ДТС РК осуществляет проверку сертификатов, выданных иностранными УЦ центрами, зарегистрированными в доверенной третьей стороне Республики Казахстан, а так же сертификатов, выданных другими иностранными УЦ, которые возможно проверять с помощью ДТС иностранных государств, зарегистрированных в ДТС РК, для предоставления квитанции с результатами проверки заинтересованным сторонам.

<a id="an1_p16"></a>

16. Цифровые системы, интегрированные с ДТС РК, при получении квитанции проверки ЭЦП сформированных ДТС РК должны выполнять, как минимум, следующие проверки:

    1) проверку подлинности ЭЦП ДТС РК, подтверждающую подлинность квитанции;

    2) проверку соответствия полученной квитанции заверяемому электронному документу и ЭЦП.

> *Приложение 1*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной*  
> *Республики Казахстан*

## Электронный запрос VSD

<table>
<tr>
<td>№ п/с</td>
<td>Наименование поля сообщения</td>
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
<td>Тип сервиса. VSD – 2</td>
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
> *третьей стороной*  
> *Республики Казахстан*

## Электронный запрос XML

<table>
<tr>
<td>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;xs:schema xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot;
xmlns:doc=&quot;urn:EEC:SignedData:v1.0:
EDoc&quot; xmlns:ds=&quot;http://www.w3.org/2000/09/xmldsig#&quot; targetNamespace=
&quot;urn:EEC:SignedData:v1.0:EDoc&quot; elementFormDefault=&quot;qualified&quot;
attributeFormDefault=&quot;unqualified&quot;&gt;
&lt;xs:import namespace=&quot;http://www.w3.org/2000/09/xmldsig#&quot; schemaLocation=
&quot;http://www.w3.org/TR/2002/REC-xmldsig-core-20020212/xmldsig-core-schema.xsd#&quot;/&gt;
&lt;xs:element name=&quot;SignedDoc&quot; type=&quot;doc:SignedDocType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Электронный документ&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt; &lt;/xs:element&gt; &lt;xs:complexType name=&quot;SignedDocType&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Тип данных &quot;Электронный документ&quot;&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt; &lt;xs:sequence&gt; &lt;xs:element name=&quot;Data&quot;&gt;
&lt;xs:annotation&gt;
&lt;xs:documentation&gt;Блок содержимого электронного документа&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;xs:complexType&gt;
&lt;xs:complexContent&gt;
&lt;xs:extension base=&quot;doc:DataType&quot;&gt;
&lt;xs:attribute name=&quot;Id&quot; type=&quot;xs:ID&quot; use=&quot;required&quot;/&gt;
&lt;/xs:extension&gt; &lt;/xs:complexContent&gt;
&lt;/xs:complexType&gt; &lt;/xs:element&gt;
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
&lt;/xs:annotation&gt; &lt;xs:sequence&gt; &lt;xs:element ref=&quot;ds:Signature&quot; maxOccurs=&quot;unbounded&quot;&gt;
&lt;xs:annotation&gt; &lt;xs:documentation&gt;Электронная цифровая подпись (электронная
подпись)&lt;/xs:documentation&gt;
&lt;/xs:annotation&gt;
&lt;/xs:element&gt;
&lt;xs:element name=&quot;SignedContent&quot;&gt; &lt;xs:annotation&gt;
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

> *Приложение 3*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной*  
> *Республики Казахстан*

## Электронная квитанция проверки электронной цифровой подписи

<table>
<tr>
<td>№ п/с</td>
<td>Наименование поля сообщения</td>
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
<td>Версия запроса. По умолчанию 1</td>
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
<td>Сертификат</td>
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

> *Приложение 4*  
> *к Правилам подтверждения*  
> *подлинности электронной*  
> *цифровой подписи доверенной*  
> *третьей стороной*  
> *Республики Казахстан*

## Схема данных основных реквизитов электронной квитанции проверки электронной цифровой подписи

<table>
<tr>
<td>
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;
&lt;xs:schema xmlns:xs=&quot;http://​www.​w3.​org/​2001/​XML​Sche​ma
&amp;​quot; xmlns:rcpt=&quot;urn:EEC:TTP:v1.0:receipt&quot; targetNamespace=&quot;urn:EEC:TTP:v1.0:receipt&quot;
elementFormDefault=&quot;qualified&quot; attributeFormDefault=&quot;unqualified&quot;&gt;
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
&lt;xs:documentation&gt;Тип элемента, указывающего, что проверка ДТС выполнена
успешно&lt;/xs:documentation&gt;
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
&lt;xs:sequence&gt; &lt;xs:element name=&quot;ReasonCode&quot;&gt;
&lt;xs:annotation&gt; &lt;xs:documentation&gt;Код ошибки&lt;/xs:documentation&gt;
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

> *Приложение к приказу*  
> *Испоняющий обязанности*  
> *министра искусственного*  
> *интеллекта и цифрового*  
> *развития*  
> *Республики Казахстан*  
> *от 9 сентября 2026 года*  
> *№ 547/НҚ*

## Перечень утративших силу некоторых приказов

<a id="an2_p1"></a>

1. Приказ исполняющего обязанности Министра по инвестициям и развитию Республики Казахстан от 23 февраля 2015 года № 149 «Об утверждении Правил подтверждения подлинности электронной цифровой подписи доверенной третьей стороной Республики Казахстан» (зарегистрированный в Реестре государственной регистрации нормативных правовых актов под № 10615).

<a id="an2_p2"></a>

2. Приказ Министра по инвестициям и развитию Республики Казахстан от 9 декабря 2015 года № 1186 «О внесении изменений в приказ исполняющего обязанности Министра по инвестициям и развитию Республики Казахстан от 23 февраля 2015 года № 149 «Об утверждении Правил подтверждения подлинности иностранной электронной цифровой подписи доверенной третьей стороной Республики Казахстан» (зарегистрированный в Реестре государственной регистрации нормативных правовых актов под № 12591).

<a id="an2_p3"></a>

3. Приказ исполняющего обязанности Министра информации и коммуникаций Республики Казахстан от 29 марта 2018 года № 121 «О внесении изменений в приказ исполняющего обязанности Министра по инвестициям и развитию Республики Казахстан от 23 февраля 2015 года № 149 «Об утверждении Правил подтверждения подлинности иностранной электронной цифровой подписи доверенной третьей стороной Республики Казахстан» (зарегистрированный в Реестре государственной регистрации нормативных правовых актов под № 16776).
