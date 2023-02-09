# Производственный календарь
Производственные календари, актуальные для Российской Федерации. Первый доступный год — 2023, последний — 2024.

## Примеры использования

### /api/calendar/2023
```js
curl -H "Content-Type:application/json" -X GET "https://holidays-calendar-ru.vercel.app/api/calendar/2023"
```
Вернет объект с годом и массивом месяцев.
```json
{
  "year": 2023,
  "months": [...],
  "status": 200
}
```

### /api/calendar/2023/1/
```js
curl -H "Content-Type:application/json" -X GET "https://holidays-calendar-ru.vercel.app/api/calendar/2023/1"
```
Вернет объект месяца. Нумерация месяцев начинается с 1, а не с 0. Январь — месяц под номером 1.
```json
{
  "year": 2023,
  "month": {
    "id": 0,
    "name": "January",
    "workingDays": 17,
    "notWorkingDays": 14,
    "shortDays": 0,
    "workHours": 0
  },
  "status": 200
}
```
### /api/calendar/2023/1/1
```js
curl -H "Content-Type:application/json" -X GET "https://holidays-calendar-ru.vercel.app/api/calendar/2023/1"
```
Вернет объект конкретного дня.
```json
{
  "year": 2023,
  "month": {
    "name": "January",
    "id": 0
  },
  "date": "2023-01-01T00:00:00.000Z",
  "isWorkingDay": false,
  "holiday": "Новый год",
  "status": 200
}
```

## Локальная установка
```bash
$ git clone https://github.com/iposho/holidays-calendar-ru.git
$ cd holidays-calendar-ru/
$ npm i
[...]
$ npm run dev
```

## Лицензия
Это проект с открытым кодом, распространяющийся под лицензией [MIT License](LICENSE).