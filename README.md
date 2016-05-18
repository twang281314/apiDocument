# 打印模板表结构设计

## 打印模板主表

|字段|描述|数据类型|备注
|----|----|----|
|templateUkid|模板主键|double|模板主键|
|templateName|模板名称|string|模板名称|
|templateType|模板类型|string|快递单、装箱单、发货单、拣选单、贺卡、发票等|
|pageWidth|宽度|int||
|pageHeight|高度|int||
|pageTop|上偏移量|int||
|pageLeft|左偏移量|int||
|createTime|创建时间|datetime||
|creater|创建人|||
|modifyTime|编辑时间|datetime||
|modifyer|修改人|||
|isUse|是否使用|bool|模板是否在使用|


## 打印模板从表

|字段|描述|数据类型|备注|
|----|----|----|----|
|templateDetailUkid|模板从表主键|double|
|templateUkid|模板主表UKid|double|关联模板主表|
|itemCustomType|打印项类型|int|打印项类型|
|itemName|打印项中文名称||||
|itemTop|上边距|int|||
|itemLeft|左边距|int|||
|itemWidth|宽度|int||
|itemHeight|高度|int||
|itemFont|字体|string|字体|
|itemContent|打印项内容|string||||
|itemBold||||
|itemItalic||||
|itemUnderline||||
|item||||
