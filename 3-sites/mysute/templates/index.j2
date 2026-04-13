<?php
// index.php - Главный файл приложения
require_once 'config.php';

// Создаем подключение к базе данных
$connection = new mysqli(DB_HOST, DB_USER, DB_PASS, DB_NAME);

// Проверяем подключение
if ($connection->connect_error) {
    die("Ошибка подключения к базе данных: " . $connection->connect_error);
}

// Устанавливаем кодировку UTF-8
$connection->set_charset("utf8");

// Выполняем запрос для получения данных из таблицы
// Замените 'users' на название вашей таблицы
$tableName = 'users';
$sql = "SELECT * FROM $tableName";
$result = $connection->query($sql);

// Проверяем, есть ли данные
if ($result === false) {
    die("Ошибка выполнения запроса: " . $connection->error);
}

?>
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Содержимое таблицы MySQL</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f5f5f5;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        h1 {
            color: #333;
            text-align: center;
        }
        .table-info {
            text-align: center;
            color: #666;
            margin-bottom: 20px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: left;
        }
        th {
            background-color: #4CAF50;
            color: white;
            font-weight: bold;
        }
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        tr:hover {
            background-color: #f5f5f5;
        }
        .no-data {
            text-align: center;
            color: #999;
            padding: 40px;
            font-style: italic;
        }
        .error {
            color: red;
            text-align: center;
            padding: 20px;
            background-color: #ffe6e6;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Содержимое таблицы: <?php echo htmlspecialchars($tableName); ?></h1>
        
        <?php if ($result->num_rows > 0): ?>
            <div class="table-info">
                Найдено записей: <?php echo $result->num_rows; ?>
            </div>
            
            <table>
                <thead>
                    <tr>
                        <?php 
                        // Получаем информацию о полях таблицы
                        $fields = $result->fetch_fields();
                        foreach ($fields as $field): 
                        ?>
                            <th><?php echo htmlspecialchars($field->name); ?></th>
                        <?php endforeach; ?>
                    </tr>
                </thead>
                <tbody>
                    <?php 
                    // Выводим данные
                    $result->data_seek(0); // Возвращаем указатель в начало
                    while ($row = $result->fetch_assoc()): 
                    ?>
                        <tr>
                            <?php foreach ($row as $value): ?>
                                <td><?php echo htmlspecialchars($value ?? 'NULL'); ?></td>
                            <?php endforeach; ?>
                        </tr>
                    <?php endwhile; ?>
                </tbody>
            </table>
            
        <?php else: ?>
            <div class="no-data">
                Таблица пуста. Нет данных для отображения.
            </div>
        <?php endif; ?>
        
    </div>
</body>
</html>
<?php
// Закрываем подключение
$connection->close();
?>
