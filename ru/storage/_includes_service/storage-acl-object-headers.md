Заголовок | Описание
--- | ---
`x-amz-acl` | Устанавливает [предопределенный ACL](../concepts/acl.md#predefined-acls) для объекта.
`x-amz-grant-read` | Устанавливает получателю доступа разрешение на чтение объекта.
`x-amz-grant-read-acp` | Устанавливает получателю доступа разрешение на чтение ACL объекта.
`x-amz-grant-write-acp` | Устанавливает получателю доступа разрешение на запись ACL объекта.
`x-amz-grant-full-control` | Устанавливает получателю доступа разрешения: `READ`, `WRITE`, `READ_ACP`, `WRITE_ACP` на объект.

Значение для заголовков `x-amz-grant-*` представляет собой разделенный запятыми список получателей доступа. Каждый получатель доступа идентифицируется структурой вида `<тип получателя доступа>:<идентификатор получателя доступа>`. {{ objstorage-name }} поддерживает следующие типы получателей:
* `id` — получатель доступа — пользователь облака.
* `uri` — получатель доступа — системная группа.

Пример:

```
x-amz-grant-read: uri="http://acs.amazonaws.com/groups/s3/AuthenticatedUsers"
```