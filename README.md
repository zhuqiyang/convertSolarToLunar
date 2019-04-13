# convertSolarToLunar
公历转农历，Converting the Gregorian Calendar into the Lunar Calendar


## ThinkPHP中的使用方法：
    先将文件放入 ThinkPHP/Library/Org/Util 中，然后在控制器中使用 import 函数导入即可。
```php
public function demo()
{
	import('Org.Util.DateConvert');
	$DateConvert = new \DateConvert();

	$date = explode('-',date('Y-m-d'));
	$lunar = $DateConvert->convertSolarToLunar($date[0], $date[1], $date[2]);
	dump($lunar);
}
```

## 原生PHP的使用方法：
```php
require("DateConvert.class.php");
$DateConvert = new DateConvert();

$date = explode('-',date('Y-m-d'));
$lunar = $DateConvert->convertSolarToLunar($date[0], $date[1], $date[2]);
var_dump($lunar);
```
