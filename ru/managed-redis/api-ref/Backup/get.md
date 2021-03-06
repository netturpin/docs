---
editable: false
---

# Метод get
Возвращает указанную резервную копию Redis.
 
Чтобы получить список доступных резервных копий Redis, используйте запрос [list](/docs/managed-redis/api-ref/Backup/list).
 
## HTTP-запрос {#https-request}
```
GET https://mdb.api.cloud.yandex.net/managed-redis/v1alpha/backups/{backupId}
```
 
## Path-параметры {#path_params}
 
Параметр | Описание
--- | ---
backupId | Обязательное поле. Идентификатор резервной копии Redis, информацию о которой нужно запросить. Чтобы получить идентификатор резервной копии, используйте запрос [listBackups](/docs/managed-redis/api-ref/Cluster/listBackups).
 
## Ответ {#responses}
**HTTP Code: 200 - OK**

```json 
{
  "id": "string",
  "folderId": "string",
  "createdAt": "string",
  "sourceClusterId": "string",
  "startedAt": "string"
}
```
Описание резервной копии Redis. Подробнее смотрите в [документации](/docs/managed-redis/concepts/backup) Managed
Service for Redis.
 
Поле | Описание
--- | ---
id | **string**<br><p>Идентификатор резервной копии.</p> 
folderId | **string**<br><p>Идентификатор каталога, которому принадлежит резервная копия.</p> 
createdAt | **string** (date-time)<br><p>Время создания в формате <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> (т. е. когда операция резервного копирования была завершена).</p> <p>Строка в формате <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a>.</p> 
sourceClusterId | **string**<br><p>Идентификатор кластера Redis, для которого была создана резервная копия.</p> 
startedAt | **string** (date-time)<br><p>Время запуска операции резервного копирования в формате <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a>.</p> <p>Строка в формате <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a>.</p> 