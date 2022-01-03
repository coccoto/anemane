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

$dotcrud = new coccoto\dotcrud\CRUD();
$dotcrud->select('list', $data);
$result = $dotcrud->stmt->fetchAll();
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

$dotcrud = new coccoto\dotcrud\CRUD();
$dotcrud->select('list', $data);
$result = $dotcrud->stmt->fetchAll();
```

### Instructions executed by this operation

```sql
SELECT subject, score FROM list WHERE class=3
```