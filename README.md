Төслийн бүтэц ба зохион байгуулалт
Бие даалтын шаардлагын дагуу файлын бүтцийг дараах байдлаар зохион байгуулсан:

Plaintext
bie-daalt-14/
├── .github/
│   └── workflows/
│       └── api-tests.yml       # GitHub Actions CI тохиргооны файл
├── partA/
│   ├── SETUP.md                # Сонгосон API, brief, base URL, auth мэдээлэл
│   └── screenshot.png          # Эхний амжилттай request-ийн зураг
├── postman/
│   ├── collection.json         # Экспорт хийсэн 8+ request бүхий коллекц
│   ├── env.dev.json            # Хөгжүүлэлтийн орчны хувьсагчид (Placeholder-той)
│   └── env.ci.json             # CI орчны хувьсагчид (GitHub Secrets-д зориулсан)
├── reports/
│   └── api.html                # Newman-ээр үүсгэсэн HTML тестийн тайлан
├── server/
│   └── index.js                # Докал сервер (Хувилбар 3-ийг сонгосон үед)
├── README.md                   # Хэрхэн ажиллуулах заавар (Энэхүү файл)
└── REFLECTION.md               # Лабораторийн ажлын эргэцүүлэл (5 асуултын хариулт)
Тестийн хамралт (Test Coverage)
Нийт Request-үүд: 8-аас доошгүй request, хавтсаар (Folder) бүлэглэсэн (Жишээ нь: Users, Auth, Errors).

Хамрагдсан HTTP Төрлүүд: Happy GET, GET by id, POST create, PUT/PATCH, DELETE, болон Error case (4xx).

Request Chaining: Нэг request-ийн хариунаас (Response) дата аваад дараагийн request-ийн хувьсагч болгон ашиглах логик суурилуулсан.

Assertion-ы төрлүүд (15+ тест): - Status code (200, 201, 204, 400/404)

Response time / Latency (< 1000ms)

JSON schema / Property validation

Data type validation (string, number)

Business rules (Email format regex)

Headers validation (Content-Type)

CI/CD Integration (GitHub Actions)
Төсөл дээр шинэ commit очих (push) эсвэл pull_request үүсэх тоолонд .github/workflows/api-tests.yml автомат ажиллагаа идэвхжиж, Newman тестүүдийг Ubuntu орчинд ажиллуулна. Тест амжилттай болж дууссаны дараа үүссэн HTML тайланг Artifact хэлбэрээр татаж авах боломжтойгоор тохируулсан.