# 介绍
公历转农历,整合日历,在原有的基础上增加了根据给定日期返回节日以及二十节气的时间

# 安装
```shell
composer require shijunjun/calendar
```

# 用法
```
// 根据制定日期查询农历相关信息
use shijunjun\Calendar\Calendar;
require_once __DIR__ . '/vendor/autoload.php';
$calendar = new Calendar();
var_export($calendar->solar2lunar(2019, 3, 6,10)); 	// 转农历不包扩阳历日期以及星座
var_export($calendar->solar(2019, 3, 6,10));		// 转农历包扩阳历日期以及星座

// 返回结果
array (
    'lunar_year' => '2019', 				// 农历数字年
    'lunar_month' => '01', 				// 农历数字月
    'lunar_day' => '30',					// 农历数字日
    'lunar_hour' => '10',				// 农历数字时
    'lunar_year_chinese' => '二零一九',		// 农历汉字年
    'lunar_month_chinese' => '正月',		// 农历汉字月
    'lunar_day_chinese' => '三十',			// 农历汉字日
    'lunar_hour_chinese' => '巳时',		// 农历汉字时
    'ganzhi_year' => '己亥',				// 干支年
    'ganzhi_month' => '丁卯',				// 干支月
    'ganzhi_day' => '壬寅',				// 干支日
    'ganzhi_hour' => '乙巳',				// 干支时
    'wuxing_year' => '土水',				// 五行年
    'wuxing_month' => '火木',				// 五行月
    'wuxing_day' => '水木',				// 五行日
    'wuxing_hour' => '木火',				// 五行时
    'color_year' => '黄',				// 干支转色彩年
    'color_month' => '红',				// 干支转色彩月
    'color_day' => '黑',					// 干支转色彩日
    'color_hour' => '青',				// 干支转色彩时
    'animal' => '猪',					// 生肖
    'term' => '惊蛰',					// 二十四节气&阴历节日&阳历节日
    'term_date' => '2019-03-06 05:08:53',	// 二十节气时间
    'is_leap' => false,					// 是否闰年
);
array (
    'lunar_year' => '2019', 				// 农历数字年
    'lunar_month' => '01', 				// 农历数字月
    'lunar_day' => '30',					// 农历数字日
    'lunar_hour' => '10',				// 农历数字时
    'lunar_year_chinese' => '二零一九',		// 农历汉字年
    'lunar_month_chinese' => '正月',		// 农历汉字月
    'lunar_day_chinese' => '三十',			// 农历汉字日
    'lunar_hour_chinese' => '巳时',		// 农历汉字时
    'ganzhi_year' => '己亥',				// 干支年
    'ganzhi_month' => '丁卯',				// 干支月
    'ganzhi_day' => '壬寅',				// 干支日
    'ganzhi_hour' => '乙巳',				// 干支时
    'wuxing_year' => '土水',				// 五行年
    'wuxing_month' => '火木',				// 五行月
    'wuxing_day' => '水木',				// 五行日
    'wuxing_hour' => '木火',				// 五行时
    'color_year' => '黄',				// 干支转色彩年
    'color_month' => '红',				// 干支转色彩月
    'color_day' => '黑',					// 干支转色彩日
    'color_hour' => '青',				// 干支转色彩时
    'animal' => '猪',					// 生肖
    'term' => '惊蛰',					// 二十四节气&阴历节日&阳历节日
    'term_date' => '2019-03-06 05:08:53',	// 二十节气时间
    'is_leap' => false,					// 是否闰年
    'gregorian_year' => '2019',			// 阳历年
    'gregorian_month' => '03',			// 阳历月
    'gregorian_day' => '06',				// 阳历日
    'gregorian_hour' => '10',				// 阳历时
    'week_no' => 3,						// 数字星期
    'week_name' => '星期三',				// 汉字星期
    'is_today' => false,					// 是否当日
    'constellation' => '双鱼',			// 星座
);
```

# 参考

- [公历转农历的计算代码采用的是(overtrue/chinese-calendar)](https://github.com/overtrue/chinese-calendar)
- [二十四节气的算法采用的是Re***@foxmail.com分享出来的代码](http://damigen.com/)
