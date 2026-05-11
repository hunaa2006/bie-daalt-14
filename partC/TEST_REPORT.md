# Бие даалт 14: Integration & API Testing
**Хэрэглүүр:** Postman, JSONPlaceholder API

## 1. Төслийн зорилго
Энэхүү бие даалтаар Postman ашиглан REST API хүсэлтүүдийг зохион байгуулах, хүсэлт хооронд өгөгдөл дамжуулах (Chaining), болон автомат тестүүд (Assertions) бичиж сурах зорилготой.

## 2. Тест скриптүүд 

Бие даалтын хүрээнд нийт **24** assertion бичсэн. Үүнд дараах шалгуурууд багтсан:

### 2.1 Assertion-ий төрлүүд:
1. **Статус код:** `pm.response.to.have.status(200)`
2. **Хариу ирэх хугацаа:** `pm.expect(pm.response.responseTime).to.be.below(1000)`
3. **Өгөгдлийн төрөл:** `pm.expect(jsonData).to.be.an('array')`
4. **Өгөгдлийн бүтэц:** `pm.expect(firstUser).to.have.property('email')`
5. **Regex шалгалт:** `pm.expect(email).to.match(/@/)`

### 2.2 Автоматжуулалт ба Negative Test:
- **Pre-request Script:** `PUT Update` хүсэлт явахаас өмнө шинэчлэх өгөгдлийг (random/dynamic data) бэлтгэсэн.
- **Negative Test:** Байхгүй ID ашиглан хүсэлт явуулж, систем **404** алдааг зөв барьж байгааг шалгасан.

## 3. Гүйцэтгэлийн үр дүн
Postman-ийн "Collection Runner" ашиглан бүх тестүүдийг ажиллуулахад 100% амжилттай (Passed) гарсан.

![Test Results Screenshot]([result1.png])
![Test Results Screenshot]([result2.png])
![Test Results Screenshot]([result3.png])

---
**Огноо:** 2026.05.11