- Activity像一个工匠（控制单元），Window像窗户（承载模型），View像窗花（显示视图） LayoutInflater像剪刀，Xml配置像窗花图纸。
- 1. 在Activity中调用attach，创建了一个Window
- 2. 创建的window是其子类PhoneWindow，在attach中创建PhoneWindow
- 3. 在Activity中调用setContentView([R.layout.xxx](http://R.layout.xxx))
- 4. 其中实际上是调用的getWindow().setContentView()
- 5. 调用PhoneWindow中的setContentView方法
- 6. 创建ParentView： 作为ViewGroup的子类，实际是创建的DecorView(作为FramLayout的子类）
- 7. 将指定的R.layout.xxx进行填充 通过布局填充器进行填充【其中的parent指的就是DecorView】
- 8. 调用到ViewGroup
- 9. 调用ViewGroup的removeAllView()，先将所有的view移除掉
- 10. 添加新的view：addView()