# А хэсэг - Setup (Лабораторийн бэлтгэл)

[cite_start]Энэхүү лабораторийн ажлын хүрээнд API тестийн автоматжуулалтыг турших зорилгоор JSONPlaceholder нээлттэй API-г сонгон авсан[cite: 23, 25].

### 1. Сонгосон API-ийн мэдээлэл
* [cite_start]**Нэр:** JSONPlaceholder [cite: 25]
* [cite_start]**Тайлбар:** REST API-г турших, сургалтын зорилгоор ашигладаг "fake" онлайн сервер[cite: 25].
* [cite_start]**Base URL:** `https://jsonplaceholder.typicode.com` [cite: 25]
* [cite_start]**Authentication:** Энэхүү API нь нээлттэй тул ямар нэгэн токен эсвэл эрх шаардахгүй[cite: 25].
* [cite_start]**Rate Limit:** Нийтэд нээлттэй тул хэрэглээний тодорхой хязгаар байхгүй ч туршилтын зорилгоор ашиглана[cite: 47].

### 2. Postman тохиргоо
[cite_start]Багшийн зааврын дагуу Postman Desktop програм дээр дараах тохиргоог хийсэн[cite: 46]:
* [cite_start]**Workspace:** `F.CSM311 - Lab14` нэртэй ажлын орчин үүсгэв[cite: 48].
* [cite_start]**Collection:** `Төгөлдөр JSONPlaceholder` (Овог нэр + API нэр)[cite: 49].
* [cite_start]**Environments:** `dev`, `staging`, `prod` гэсэн 3 орчин үүсгэж, `dev` орчинд `baseUrl` хувьсагчийг тохируулж өгсөн[cite: 50].

### 3. Эхний амжилттай хүсэлт
[cite_start]API-тай холбогдсон эсэхийг шалгах зорилгоор `{{baseUrl}}/posts/1` хаяг руу `GET` хүсэлт илгээхэд серверээс `200 OK` хариу амжилттай ирсэн[cite: 51, 189].

### 4. Screenshot
Эхний амжилттай хүсэлтийн скриншотыг доорх байршилд хадгалсан:
[cite_start]`../partA/screenshot.png`