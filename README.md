# NeoScout API

## Краткое описание

Ваш API ключ - это ваш уровень доступа. Используйте его с умом.

```
Authorization: Bearer your_api_key
```

## Зоны операций

### Информация о пользователе
```
GET /users/me
```
Получение данных вашего профиля. Чисто и точно.

### Разведка устройств
```
GET /devices
```
Полный инвентарь ваших операционных единиц.

```
GET /devices/{device_id}
```
Детальная информация о конкретном устройстве. Доступ ограничен вашими устройствами.

### Протокол подключения
```
POST /connection-codes
```
Генерация защищенных кодов подключения. Ваши устройства, ваши правила.

### Анализ отчетов
```
POST /reports
```
Отправка данных от устройств. Требуется уровень доступа устройства.

```
GET /reports
```
Доступ к полному журналу операций.

```
GET /reports/device/{device_id}
```
История операций конкретного устройства.

```
GET /reports/{report_id}
```
Получение детального отчета. Только для ваших глаз.

## Коды состояния

- 200: Миссия выполнена
- 401: Доступ запрещен
- 403: Доступ ограничен
- 404: Цель не найдена
- 500: Система скомпрометирована

Ответы с ошибками содержат критическую информацию в поле `detail`.

---

**NeoScout — Scan. Analyze. Take control** 
