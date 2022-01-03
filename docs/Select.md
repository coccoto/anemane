# Select

## Example

- 1

```php
$data = [
    'columns' => [
        'subject',
        'score',
    ],
];

$selectdb = new coccoto\selectdb\CRUD();
$selectdb->select('list', $data);
$result = $selectdb->stmt->fetchAll();
```

### Instructions executed by this operation

```sql
SELECT subject, score FROM list
```

- 2

```php
$data = [
    'columns' => [
        'subject',
        'score',
    ],
    'where' => [
        'class' => 3,
    ],
];

$selectdb = new coccoto\selectdb\CRUD();
$selectdb->select('list', $data);
$result = $selectdb->stmt->fetchAll();
```

### Instructions executed by this operation

```sql
SELECT subject, score FROM list WHERE class=3
```