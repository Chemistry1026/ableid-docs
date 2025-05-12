---
id: hooks
title: Хуки
---

## `Хук получения паспорта`

**Описание:** Получение паспорта

### Ответы

#### `Успешный ответ: 201`

```json
{
  "statusCode": 200,
  "type": "SUCCESS",
  "message": "Сообщение",
  "data": {
    "signature": "1BF41318DFA700936EC613BB8711DC4C68B23C7F",
    "attemptId": "RFJkzaealP6XF0CspiAoq",
    "data": {
      "address": null,
      "cadastre": null,
      "country": null,
      "countryId": null,
      "region": null,
      "regionId": null,
      "district": null,
      "districtId": null,
      "maxala": null,
      "maxalaId": null,
      "street": null,
      "streetId": null
    }
  }
}
```

**Описание полей:**

| Поле        | Тип данных       | Описание                          |
|-------------|------------------|-----------------------------------|
| `address`   | `string \| null` | Адрес                             |
| `cadastre`  | `string \| null` | Кадастровый номер                 |
| `country`   | `string \| null` | Данные о стране                   |
| `countryId` | `string \| null` | ID страны                         |
| `region`    | `string \| null` | Данные о регионе (области)        |
| `regionId`  | `string \| null` | ID региона (области)              |
| `district`  | `string \| null` | Данные о районе                   |
| `districtId`| `string \| null` | ID района                         |
| `maxala`    | `string \| null` | Данные о махалле                  |
| `maxalaId`  | `string \| null` | ID махалли                        |
| `street`    | `string \| null` | Данные о улице                    |
| `streetId`  | `string \| null` | ID улицы                          |


---
## `Хук получения прописки`

**Описание:** Получение прописки

### Ответы

#### `Успешный ответ: 201`

```json
{
  "statusCode": 200,
  "type": "SUCCESS",
  "message": "Сообщение",
  "data": {
    "hash": "1BF41318DFA700936EC613BB8711DC4C68B23C7F",
    "attemptId": "RFJkzaealP6XF0CspiAoq",
    "data": {
      "attemptId": "",
      "surname": "",
      "name": "",
      "lastName": "",
      "document": "",
      "sex": 0,
      "passportGivePlace": "",
      "passportGivePlaceId": 0,
      "passportDateBegin": "",
      "passportDateEnd": "",
      "passportType": ""
    }
  }
}
```

**Описание полей:**

| Поле                  | Тип данных        | Описание                                               |
|-----------------------|------------------|--------------------------------------------------------|
| `attemptId`           | `string`         | ID сессии                                              |
| `surname`             | `string`         | Фамилия                                                |
| `name`                | `string`         | Имя                                                    |
| `lastName`            | `string`         | Отчество                                               |
| `document`            | `string`         | Серия и номер паспорта                                 |
| `sex`                 | `number`         | Пол                                                    |
| `passportGivePlace`   | `string`         | Кем выдан документ                                     |
| `passportGivePlaceId` | `number`         | Кем выдан документ (из справочника)                   |
| `passportDateBegin`   | `string`         | Дата начала действия документа                         |
| `passportDateEnd`     | `string`         | Дата окончания действия документа                      |
| `passportType`        | `string \| null` | Тип документа (см. справочник ниже)                   |

### Справочник типов документов

| Код                                 | Наименование                                         |
|-------------------------------------|------------------------------------------------------|
| `IDMS_RECV_IP_DOCUMENTS`            | Загранпаспорт гражданина РУз                         |
| `IDMS_RECV_CITIZ_DOCUMENTS`         | Общегражданский биометрический паспорт              |
| `IDMS_RECV_LBG_DOCUMENTS`           | Проездной документ ЛБГ                               |
| `IDMS_RECV_MVD_IDCARD_CITIZEN`      | ID-карта гражданина Республики Узбекистан            |
| `IDMS_RECV_MVD_IDCARD_FOREIGN`      | ID-карта иностранного гражданина                     |
| `IDMS_RECV_MVD_IDCARD_LBG`          | ID-карта ЛБГ                                         |
| `IDMS_RECV_MVD_IDCARD_NEWBORN`      | ID-карта новорожденного                              |
| `IDMS_RECV_MJ_BIRTH_CERTS`          | Свидетельства о рождении                             |