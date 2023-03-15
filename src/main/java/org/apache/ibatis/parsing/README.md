xml 文件解析过程：

1.XML文件通过[XPathParser.java](XPathParser.java)对象解析成Document对象,内部的Properties对象存储动态变量的值

2.[PropertyParser.java](PropertyParser.java) 用于解析XML文件中的动态值,根据[GenericTokenParser.java](GenericTokenParser.java)获取动态属性的名称(例如${name} -> name)
,然后通过VariableTokenHandler根据PropertyParser对象动态获取到动态属性(name)对应的值
