# Chinese Conversion
PHP Chinese Conversion, Simple, Lightweight (v0.2 with WikiMedia Library < 400KB)

## Installation
### Composer
Run `composer require kivanfan/ChineseConverter`

### Manually
Clone this repo, run `composer dump-autoload` on root directory to 
generate `autoload.php`.

## Feature
- Use WikiMedia or OpenCC library
- 使用最長匹配規則

## Demo
```php
use SteelyWing\Chinese\Chinese;

$chinese = new Chinese();

// 转成简体中文
echo $chinese->to(Chinese::CHS, "轉成簡體中文\n");

// 轉成繁體中文
echo $chinese->to(Chinese::CHT, "转成繁体中文\n");
```

## Switch library
Switch to OpenCC, run the following in command line
```sh
cd dict
git clone https://github.com/BYVoid/OpenCC.git
php import_opencc.php
```

Switch to WikiMedia, run the following in command line
```sh
cd dict
php import_wikimedia.php
```

## License
MIT

[WikiMedia License](https://github.com/wikimedia/mediawiki/blob/master/COPYING)
[OpenCC License](https://github.com/BYVoid/OpenCC/blob/master/LICENSE)
