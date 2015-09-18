# xls2csv
Convert xls to csv

(将xls数据文件转化为csv)

use [python xlrd](https://pypi.python.org/pypi/xlrd)

(使用python xlrd模块)

Blog: http://www.luzexi.com

Email: jesse_luzexi@163.com

###What's this. (是什么)
This is a script to convert xls to csv.

(这是个脚本用于转化xls的数据到csv格式。)

### Example（例子xls表格）
example_building.xls  

<table>
    <tr>
        <td>id</td>
        <td>name</td>
        <td>use_money</td>
        <td>use_food</td>
        <td>is_init</td>
        <td>defense</td>
        <td>args1</td>
        <td>args2</td>
        <td>args3</td>
        <td>args4</td>
    </tr>
    <tr>
        <td>1</td>
        <td>house</td>
        <td>1000</td>
        <td>2.33</td>
        <td>TRUE</td>
        <td>100</td>
        <td>1;2;3</td>
        <td>1.23;2;3.23</td>
        <td>sdf;23e;s</td>
        <td>true;false;true</td>
    </tr>
    <tr>
        <td>2</td>
        <td>house2</td>
        <td>123</td>
        <td>336.2</td>
        <td>TRUE</td>
        <td></td>
        <td>1;2;3</td>
        <td>1;2.3445;3</td>
        <td>你好;你在哪</td>
        <td>true;false</td>
    </tr>
    <tr>
        <td>3</td>
        <td></td>
        <td>456</td>
        <td>222.33665</td>
        <td>FALSE</td>
        <td>130</td>
        <td>3;2;5;;</td>
        <td>3;2;2.5;;</td>
        <td>我在这里啊;你在那;呢</td>
        <td>false;true</td>
    </tr>
    <tr>
        <td>4</td>
        <td>farm</td>
        <td>100</td>
        <td>220</td>
        <td>FALSE</td>
        <td>200</td>
        <td>2;3;</td>
        <td>200.3;3;234.23;</td>
        <td>df;ssd;dd;dd</td>
        <td></td>
    </tr>
    <tr>
        <td>5</td>
        <td>house5</td>
        <td></td>
        <td>22.1</td>
        <td></td>
        <td>2343;6;6;;;7</td>
        <td>3;6.3;6;;;7</td>
        <td>ss;d;d;d</td>
        <td>true;true</td>
    </tr>
    <tr>
        <td>6</td>
        <td>horse3</td>
        <td>200</td>
        <td></td>
        <td>FALSE</td>
        <td>333</td>
        <td></td>
        <td></td>
        <td>2e;w;e;we</td>
        <td>false;false;false;false</td>
    </tr>
</table>

### Excute Example (举例执行命令)
python ./xls2csv.py example_building.xls ./data/

### NOTICE:(注意点)
> The sheet name must start with "output_" , the csv file name will be the name behind "output_". <br />
> (sheet名以"output_"开头的才会被识别转换，否则将被忽略) <br />

### csv file output (生成后的csv文件示例)
```csv
id,name,use_money,use_food,is_init,defense,args1,args2,args3,args4
1,house,1000,2,1,100,1;2;3,1.23;2;3.23,sdf;23e;s,true;false;true
2,house2,123,336,1,,1;2;3,1;2.3445;3,你好;你在哪,true;false
3,,456,222,0,130,3;2;5;;,3;2;2.5;;,我在这里啊;你在那;呢,false;true
4,farm,100,220,0,200,2;3;,200.3;3;234.23;,df;ssd;dd;dd,
5,house5,,22,,234,3;6;6;;;7,3;6.3;6;;;7,ss;d;d;d,true;true
6,horse3,200,,0,333,,,2e;w;e;we,false;false;false;false
```
