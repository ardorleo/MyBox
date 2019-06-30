# [User Guide in English](https://mararsh.github.io/MyBox/english_interface.html)

# MyBox：简易工具集

这是利用JavaFx开发的图形化界面程序，目标是提供简单易用的功能。免费开源。

## 下载
每个版本编译好的包已发布在[Releases](https://github.com/Mararsh/MyBox/releases?)目录下（点击上面的releases页签）。

可以下载exe包，在Windows上无需java环境、无需安装、解包可用：(请解包到纯英文目录下)
[MyBox-5.2-exe.zip](https://github.com/Mararsh/MyBox/releases/download/v5.2/MyBox-5.2-exe.zip) 。

在已安装JRE或者JDK（Java8/9/10）的环境下，可以下载jar包 
[MyBox-5.2-jar.zip](https://github.com/Mararsh/MyBox/releases/download/v5.2/MyBox-5.2-jar.zip) 

## 运行
在Windows上双击“MyBox.exe”即可运行MyBox。可以把图片/文本/PDF文件的打开方式关联到MyBox.exe，这样双击文件名就直接是用MyBox打开了。

在Linux和Mac上缺省有Java环境，因此只提供jar包而未制作平台安装包。执行以下命令来启动程序：
<PRE><CODE>     java   -jar   MyBox-5.2.jar</CODE></PRE>
程序可以跟一个文件名作为参数、以用MyBox直接打开此文件。例如以下命令是打开此图片：
<PRE><CODE>     java   -jar   MyBox-5.2.jar   /tmp/a1.jpg</CODE></PRE>

## 限制
在包含非英文字符的路径下无法启动MyBox.exe。请解包到纯英文目录下。Jar包的运行不受此限制。

Java 11变化了很多，因此不能保证MyBox在高于Java 10的平台可以运行。这是MyBox基于Java8的最后一个版本，下一版本（5.3）将迁移Java12上。

由于目前版本中内嵌的Derby数据库是单应用模式，因此只有首先运行的MyBox实例可读写数据库。
即：可以同时运行多个Mybox实例，但只有第一启动的实例可以保存和读取配置数据，其它实例可以执行除读写配置数据的大部分功能。


# 资源地址
[项目主页：https://github.com/Mararsh/MyBox](https://github.com/Mararsh/MyBox)

[源代码和编译好的包：https://github.com/Mararsh/MyBox/releases](https://github.com/Mararsh/MyBox/releases)

[在线提交软件需求和问题报告：https://github.com/Mararsh/MyBox/issues](https://github.com/Mararsh/MyBox/issues)

[云盘地址：https://pan.baidu.com/s/1fWMRzym_jh075OCX0D8y8A#list/path=%2F](https://pan.baidu.com/s/1fWMRzym_jh075OCX0D8y8A#list/path=%2F)

[在线帮助：https://mararsh.github.io/MyBox/mybox_help_zh.html](https://mararsh.github.io/MyBox/mybox_help_zh.html)


# 用户手册
[综述 https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-Overview-zh.pdf](https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-Overview-zh.pdf)

[图像工具 https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-ImageTools-zh.pdf](https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-ImageTools-zh.pdf)

[PDF工具 https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-PdfTools-zh.pdf](https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-PdfTools-zh.pdf)

[桌面工具 https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-DesktopTools-zh.pdf](https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-DesktopTools-zh.pdf)

[网络工具 https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-NetworkTools-zh.pdf](https://github.com/Mararsh/MyBox/releases/download/v5.0/MyBox-UserGuide-5.0-NetworkTools-zh.pdf)


# 当前版本
当前是版本5.2，已实现的特点概述如下。
## 跨平台
纯Java实现且基于开源库，因此MyBox可运行于所有支持Java 8/9/10的平台。

这是MyBox基于Java8的最后一个版本，下一版本（5.3）将迁移Java12上。
## 国际化
所有代码均国际化。可实时切换语言。目前支持中文、英文。扩展语言只需编辑资源文件。
## PDF工具
1. 以图像模式查看PDF文件，可以设置dpi以调整清晰度，可以把页面剪切保存为图片。
   可选显示标签（目录）和缩略图。
2. 将PDF文件的每页转换为一张图片，包含图像密度、色彩、格式、压缩、质量、色彩转换等选项。
3. 将多个图片合成PDF文件，可以设置压缩选项、页面尺寸、页边、页眉、作者等。
   支持中文，程序自动定位系统中的字体文件，用户也可以输入ttf字体文件路径。
4. 压缩PDF文件的图片，设置JPEG质量或者黑白色阈值。
5. 合并多个PDF文件。
6. 分割PDF文件为多个PDF文件，可按页数或者文件数来均分，也可以设置起止列表。
7. 将PDF中的图片提取出来。可以指定页码范围。
8. 将PDF文件中的文字提取出来，可以定制页的分割行。
9. PDF的批量处理。
10. 修改PDF的属性，如：标题、作者、版本、修改时间、用户密码、所有者密码、用户权限等
11. 可设置PDF处理的主内存使用量。

## 图像工具

### 查看图像
1. 设置加载宽度：原始尺寸或指定宽度。
2. “选择模式”：处于选择模式时，剪裁、复制、另存，都是针对选择的区域，否则是针对整个图像。
3. 旋转可保存。
4. 删除、重命名、恢复。
5. 可选显示：坐标、横标尺、纵标尺、数据。
6. 统计显示图像的数据：各颜色通道的均值/方差/斜率/中值/众数/最大/最小，以及直方图。直方图的颜色通道可多选。
7. 查看图像的元数据和属性。
8. 同目录下图像文件导览，多种文件排序方式。
### 浏览图像
1. 同屏显示多图，分别或者同步旋转和缩放。
2. 旋转可选保存。
3. 格栅模式：可选文件数、列数、加载宽度
4. 文件列表模式
5. 缩略图列表模式
6. 重命名、删除
### 图像处理
1. 大小：拖动锚点调整大小、按比例收缩、或设置像素。四种保持宽高比的选项。
2. 剪裁：按矩形、圆形、椭圆、多边形，剪切内部或外部。可设置背景色。
3. 颜色：针对红/蓝/绿/黄/青/紫通道、饱和度、明暗、色相、不透明度，进行增加、减少、设值、过滤、取反色的操作。可选是否预乘透明。
4. 效果：清晰、对比度、海报（减色）、阈值化、灰色、黑白色、褐色、浮雕、边沿检测、模糊、锐化。可选算法和参数。也可以通过定义和选择卷积核来制作效果。
5. 文字：设置字体、风格、大小、色彩、不透明度、阴影、角度，可选是否轮廓、是否垂直，点击图片定位文字。
6. 图片：添加内置/外选/粘贴图片，选择混合模式，设置不透明度、选择是否保持宽高比。
7. 形状：添加矩形、圆形、椭圆、多边形，设置画笔宽度和颜色，选择是否虚线，选择是否填充颜色。
8. 线条：多笔一线，设置画笔宽度和颜色，选择是否虚线。
9. 画笔：一笔一线，设置画笔宽度和颜色，选择是否虚线。
10. 马赛克：设置矩形、圆形、椭圆、多边形区域，填充为马赛克或者磨砂玻璃。可设置强度，区域可反选。
11. 圆角：把图像四角改为圆角，可设置背景色、圆角大小。
12. 阴影：可设置背景色、阴影大小、是否预乘透明。
13. 变形：斜拉、镜像、旋转，可设置参数。
14. 边沿：模糊边沿，可设置是否预乘透明；拖动锚点以调整边沿；按宽度加边；按宽度切边；按颜色切边。可选四边、颜色。
15. 图像操作的范围：全部、抠图、形状（矩形/圆形/椭圆/多边形）、颜色匹配、形状中颜色匹配。
    颜色匹配可以针对：红/蓝/绿通道、饱和度、明暗、色相，色距可定义。
	范围可作用于：颜色、效果、和卷积。可简单通过左右键点击来确定范围，范围的参数（如抠图的点集和颜色集合）可设置。均可反选。
16. 对上一步的撤销和重做。也可以随时恢复原图。修改历史可自动保存，以便退回到前面的修改；可设置修改历史的个数。
17. 选择是否显示对照图。可以选择其它图片为对照图。
18. 处理已有图片，或新建图片。
19. 复制（CTRL+c）/粘贴（CTRL+v）/弹出/参考。
### 多帧图像文件
1. 查看、提取多帧图像文件
2. 创建、编辑多帧tiff文件
3. 查看/提取/创建/编辑动画Gif文件。可设置间隔、是否循环、图片尺寸
### 多图合一
1. 图片的合并。支持排列选项、背景颜色、间隔、边沿、和尺寸选项。
2. 图片的混合。支持选择交叉区域、多种混合模式。
3. 将多个图片合成PDF文件
4. 添加透明通道
### 图像局部化
1. 图像的分割。支持按个数分割、按尺寸分割、和定制分割。可以保存为多个图像文件、多帧Tiff文件、或者PDF。
2. 图像的降采样。可以设置采样区域、采样比例。
3. 提取透明通道
### 大图片的处理
1. 评估加载整个图像所需内存,判断能否加载整个图像。
2. 若可用内存足够载入整个图像，则读取图像所有数据做下一步处理。尽可能内存操作而避免文件读写。
3. 若内存可能溢出，则采样读取图像数据做下一步处理。
4. 采样比的选择：即要保证采样图像足够清晰、又要避免采样数据占用过多内存。
5. 采样图像主要用于显示图像。已被采样的大图像，不适用于图像整体的操作和图像合并操作。
6. 一些操作，如分割图像、降采样图像，可以局部读取图像数据、边读边写，因此适用于大图像：显示的是采样图像、而处理的是原图像。
### 其它
1. 支持图像格式：png,jpg,bmp,tif,gif,wbmp,pnm,pcx。可读Adobe YCCK/CMYK的jpg图像。
2. 图像的批量处理。
3. 将图片转换为其它格式，包含色彩、长宽、压缩、质量等选项。
4. 调色盘
5. 像素计算器
6. 卷积核管理器

## 数据工具

### 矩阵计算
1. 矩阵数据的编辑：
	-  对于输入或粘贴的数据，过滤特殊字符，以适应带格式的数据。
	-  自动把当前矩阵数据转变为行向量、列向量、或指定列数的矩阵。
	-  自动生成单位矩阵、随机方阵、或随机矩阵，可设置行/列数。   
2. 矩阵的一元计算：转置、行阶梯形、简化行阶梯形、行列式值-用消元法求解、行列式值-用余子式求解
	、逆矩阵-用消元法求解、逆矩阵-用伴随矩阵求解、矩阵的秩、伴随矩阵、余子式、归一化、
	、设置小数位数、设为整型、乘以数值、除以数值、幂。
3. 矩阵的二元计算：加、减、乘、克罗内克积、哈达马积、水平合并、垂直合并。
	
### 色彩空间
1. 绘制色度图
	-  标准数据的轮廓线：CIE 1931 2度观察者（D50）、CIE 1964 10度观察者（D50）、CIE RGB色域、ECI RGB色域、sRGB色域、
	   Adobe RGB色域、Apple RGB色域、PAL RGB色域、NTSC RGB色域、ColorMath ProPhoto RGB色域、SMPTE-C RGB色域。
	-  标准光源（白点）：A、C、D50、D55、D65、E。
	-  用户可填写刺激值或色坐标、或选择色彩，工具自动计算各种色彩空间对应的色彩数值、并把计算值显示在色度图上。
	-  用户可输入或用文件导入光谱数据，工具自动过滤掉特殊字符、并把光谱数据显示在色度图上。
	-  用户可以选择在色度图上显示/不显示以上数据。
	-  用户可选色度图的背景为透明/白色/黑色，可选轮廓线的点尺寸或线尺寸，可选是否显示格栅和波值。
	-  工具以表格和文本显示标准数据：CIE 1931 2度观察者1nm、CIE 1931 2度观察者5nm、CIE 1964 10度观察者1nm、CIE 1964 10度观察者5nm，
	   用户可导出数据的文本。
2. 编辑ICC色彩特性文件
	-  预置标准ICC文件：Java内嵌的ICC文件（包括sRGB、XYZ、PYCC、GRAY、LINEAR_RGB）、
	   ECI提供的ICC文件（包括ECI_CMYK、ECI_RGB_v2）和Adobe提供的ICC文件（包括Adobe RGB、Apple RGB、及多种CMYK ICC文件）。
	-  头部所有字段可编辑。在保存ICC文件时，工具自动计算“profile id”字段（MD5摘要）。
	-  标签表：标签、名字、类型、偏移、大小、描述、解码后的数据、数据的原始值（十六进制字节）
	-  可编辑的标签类型：Text、MultiLocalizedUnicode、Signature、DateTime、XYZ、Curve、ViewingConditions、Measurement、S15Fixed16Array。
	   当前版本不支持编辑LUT类型的标签。
	-  选项：把LUT表中的数据归一化到0~1。
	-  整个ICC数据被解析显示为XML，并可导出。未被解码的数据显示为十六进制字节。
	-  读入的ICC数据可以修改另存为新的ICC文件。
3. RGB色彩空间
	-  用户选择或输入RGB色彩空间（基色和白点）、选择或输入要适应的参考白点，工具自动计算色适应后的基色值，并展示计算过程。
	-  可设置小数位数。
	-  色适应算法可选：Bradford、XYZ Scaling、Von Kries。
	-  预置的标准RGB色彩空间包括：CIE RGB、ECI RGB、sRGB、Adobe RGB、Apple RGB、PAL RGB、NTSC RGB、ColorMath ProPhoto RGB、SMPTE-C RGB
    -  预置的标准光源包括CIE 1931和CIE 1964的：A、B、C、D50、D55、D65、D75、E、F1~F12。 
	-  工具以表格和文本显示：不同的标准RGB色彩空间、不同的标准光源、不同的算法所计算出的色适应后的基色值。用户可导出数据的文本。
4. 线性RGB到XYZ的转换矩阵
	-  用户选择或输入RGB色彩空间（基色和白点）、选择或输入XYZ空间的参考白点，工具自动计算线性RGB到XYZ的转换矩阵，并展示计算过程。
	-  以表格和文本显示：不同的标准RGB色彩空间、不同的XYZ空间参考白点、不同的算法所计算出的转换矩阵。用户可导出数据的文本。
5. 线性RGB到线性RGB的转换矩阵
	-  用户选择或输入源和目标的RGB色彩空间（基色和白点），工具自动计算源线性RGB到目标线性RGB的转换矩阵，并展示计算过程。
	-  工具以表格和文本显示：不同的标准RGB色彩空间之间以不同的算法所计算出的转换矩阵。用户可导出数据的文本。
6. 光源
	-  用户输入源颜色（相对值/色度坐标/刺激值）、选择或输入源白点和目标白点，工具自动计算色适应后的颜色值，并展示计算过程。
	-  工具以表格和文本显示标准光源的数据值、色温和说明。用户可导出数据的文本。
7. 色度适应矩阵
	-  用户选择或输入源白点和目标白点，工具自动计算色度适应矩阵，并展示计算过程。
	-  工具以表格和文本显示不同标准光源之间不同的算法的色度适应矩阵。用户可导出数据的文本。
	
## 桌面工具

### 目录管理
1. 目录/文件重命名，包含文件名和排序的选项。被重命名的文件可以全部恢复或者指定恢复原来的名字。
2. 目录同步，包含复制子目录、新文件、特定时间以后已修改文件、原文件属性，以及删除源目录不存在文件和目录，等选项。
3. 整理文件，将文件按修改时间或者生成时间重新归类在新目录下。此功能可用于处理照片、游戏截图、和系统日志等需要按时间归档的批量文件。
### 编辑文本
1. 自动检测或手动设置文件编码；改变字符集实现转码；支持BOM设置。
2. 自动检测换行符；改变换行符。显示行号。
3. 支持LF（Unix/Linux）、 CR（Apple）、 CRLF（Windows）。
4. 查找与替换。可只本页查找/替换、或整个文件查找/替换。计数功能。
5. 定位。跳转到指定的字符位置或行号。
6. 行过滤。条件：“包含任一”、“不含所有”、“包含所有”、“不含任一”。
7. 可累加过滤。可保存过滤结果。可选是否包含行号。
8. 字符集对应的编码：字节的十六进制同步显示、同步滚动、同步选择。
9. 分页。可用于查看和编辑非常大的文件，如几十G的运行日志。
	-  可以设置页尺寸。
	-  页面导航。
	-  先加载显示首页，同时后端扫描文件以统计字符数和行数；统计期间部分功能不可用；统计完毕自动刷新界面。
	-  对于跨页字符串，确保查找、替换、过滤的正确性。
10. 通用的编辑功能（复制/粘贴/剪切/删除/全选/撤销/重做/恢复）及其快捷键。
### 编辑字节
1. 字节被表示为两个十六进制字符。所有空格、换行、非法值将被忽略。
2. 常用ASCII字符的输入选择框。
3. 换行。仅用于显示、无实际影响。显示行号。可按字节数换行、或按一组字节值来换行。
4. 查找与替换。可只本页查找/替换、或整个文件查找/替换。计数功能。
5. 定位。跳转到指定的字节位置或行号。
6. 行过滤。条件：“包含任一”、“不含所有”、“包含所有”、“不含任一”。可累加过滤。可保存过滤结果。可选是否包含行号。
7. 选择字符集来解码：同步显示、同步滚动、同步选择。非字符显示为问号。
8. 分页。可用于查看和编辑非常大的文件，如几十G的二进制文件。
	- 可以设置页尺寸。
	- 页面导航。
	- 先加载显示首页，同时后端扫描文件以统计字节数和行数；统计期间部分功能不可用；统计完毕自动刷新界面。
	- 对于跨页字节组，确保查找、替换、过滤的正确性。若按字节数换行，则行过滤时不考虑跨页。
9. 通用的编辑功能（复制/粘贴/剪切/删除/全选/撤销/重做/恢复）及其快捷键。
### 其它
1. 批量转换文件的字符集。
2. 批量转换文件的换行符
3. 切割文件。切割方式可以是：按文件数、按字节数、或按起止列表。
4. 合并文件。
5. 记录系统粘贴板中的图像：保存或查看粘贴板中的图像，可选无损图像或压缩类型。
6. 闹钟，包括时间选项和音乐选项，支持铃音“喵”、wav铃音、和MP3铃音，可以在后端运行。

## 网络工具

### 网页编辑器
1. 以富文本方式编辑本地网页或在线网页。（不支持FrameSet）
2. 直接编辑HTML代码。（支持FrameSet）
3. 网页浏览器显示编辑器内容、或在线网页。支持前后导览、缩放字体、截图页面为整图或者PDF文件。
4. 富文本页面、HTML代码、浏览器内容，这三者自动同步。
### 微博截图工具
1. 自动保存任意微博账户的任意月份的微博内容
2. 设置起止月份。
3. 确保页面完全加载，可以展开页面包含的评论、可以展开页面包含的所有图片。
4. 将页面保存为本地html文件。由于微博是动态加载内容，本地网页无法正常打开，仅供获取其中的文本内容。
5. 将页面截图保存为PDF。可以设置页尺寸、边距、作者、以及图片格式。
6. 将页面包含的所有图片的原图全部单独保存下来。
7. 实时显示处理进度。
8. 可以随时中断处理。程序自动保存上次中断的月份并填入作本次的开始月份。
9. 可以设置错误时重试次数。若超时错误则自动加倍最大延迟时间。

## 设置
1. 是否恢复界面上次尺寸、是否在新窗口中打开界面、是否弹出最近访问的文件/目录
2. 语言、字体大小、皮肤、按钮颜色、是否显示注释
3. 画笔/锚点的宽度和颜色、锚点是否实心
4. 图像是否显示坐标、横标尺、纵标尺。
5. 图像历史个数、图像最大显示宽度
6. 图像复制时是否去除Alpha通道、不支持Alpha时是否替换为白色
7. PDF可用最大主内存
8. 退出程序时是否关闭闹钟
9. 临时文件目录
10. 清除个人设置、查看用户目录。

## 窗口
1. 开/关内存监视条
2. 开/关CPU监视条
3. 显示JVM属性
4. 刷新/重置窗口
5. 关闭其它窗口
6. 最近访问的工具

# 开发日志
```
2019-6-30 版本5.2 图像解码：可读Adobe YCCK/CMYK的jpg图像；读取和显示多帧图像文件中所有图像的属性和元数据。
PDF工具：标签（目录）和缩略图；可修改PDF文件的属性，如作者、版本、用户密码、用户权限、所有者密码等。
编辑矩阵数据：适应带格式的输入数据；自动把当前矩阵数据转变为行向量、列向量、或指定列数的矩阵；
自动生成单位矩阵、随机方阵、或随机矩阵。
矩阵一元计算，包括转置、行阶梯形、简化行阶梯形、行列式值-用消元法求解、行列式值-用余子式求解、逆矩阵-用消元法求解、
逆矩阵-用伴随矩阵求解、矩阵的秩、伴随矩阵、余子式、归一化、设置小数位数、设为整型、乘以数值、除以数值、幂。
矩阵二元计算，包括加、减、乘、克罗内克积、哈达马积、水平合并、垂直合并。
色彩空间的工具：绘制色度图；编辑ICC色彩特性文件；RGB色彩空间基色的色适应；线性RGB与XYZ之间的转换矩阵；
线性RGB到线性RGB的转换矩阵；颜色值的色适应；标准光源；色度适应矩阵。
修正问题：微博截图工具经常“414 Request-URI Too Large”；按钮的提示在屏幕边沿闪烁；一些链接不可用。

2019-5-1 版本5.1 界面：控件显示为图片，5种颜色可选，可选是否显示控件文字。
简化小提示，以适应14英寸的笔记本屏幕。
图像工具：提取/添加透明通道。
修正若干问题，包括：图像处理中过滤透明像素的错误条件。
劳动节快乐！

2019-4-21 版本5.0 以拖拉锚点的方式选择图像操作的区域。
“涂鸦”：在图像上粘贴图片、添加形状（矩形/圆形/椭圆/多边形）的线条或填充形状、绘制多笔一线或一笔一线。
画笔的宽度、颜色、实虚可选。
查看图像：设置加载宽度；选择显示坐标和标尺；旋转可保存。
浏览图像：缩略图格栅模式、缩略图列表模式、文件列表模式；可设置加载宽度；旋转可保存。
图像处理：抖动处理扩展到除抠图以外的所有范围；利用预乘透明技术使不支持Alpha通道的格式也可展示透明效果；
模糊边沿；低层实现阴影效果；拖动锚点以修改大小或边沿；多种形状的剪裁；文字可垂直。
界面：只显示有用控件；足够但不叨扰的提示信息；快捷键/主键/缺省键；实时监视内存/CPU状态；
查看JVM属性；刷新/重置窗口；保存和恢复界面尺寸；弹出最近访问的文件/目录；记录最近使用的工具。
代码重构：以子类而不是分支语句来实现选择逻辑、把判断移至循环外；循环中避免浮点计算；理顺继承关系、减少重复代码；
统一管理窗口的打开和关闭、避免线程残留。

2019-2-20 版本4.9 图像对比度处理，可选算法。颜色量化时可选是否抖动处理。
图像的统计数据分析，包含各颜色通道的均值/方差/斜率/中值/众数以及直方图。
系统粘贴板内图像的记录工具。
随时修改界面字体。
查看图像：可选择区域来剪裁、复制、保存。

2019-1-29 版本4.8 以图像模式查看PDF文件，可以设置dpi以调整清晰度，可以把页面剪切保存为图片。
文本/字节编辑器的“定位”功能：跳转到指定的字符/字节位置、或跳转到指定的行号。
切割文件：按文件数、按字节数、或按起止列表把文件切割为多个文件。
合并文件：把多个文件按字节合并为一个新文件。
程序可以跟一个文件名作为参数，以用MyBox直接打开此文件。
在Windows上可以把图片/文本/PDF文件的打开方式缺省关联到MyBox.exe，可以在以双击文件时直接用MyBox打开。

2019-1-15 版本4.7  编辑字节：常用ASCII字符的输入选择框；按字节数、或按一组字节值来换行；查找与替换，本页或整个文件，计数功能；
行过滤，“包含任一”、“不含所有”、“包含所有”、“不含任一”，累加过滤，保存过滤结果，是否包含行号；
选择字符集来解码，同步显示、同步滚动、同步选择；
分页，可用于查看和编辑非常大的文件，如几十G的二进制文件，设置页尺寸，对于跨页字节组，确保查找、替换、过滤的正确性。
批量改变文件的换行符。
合并“文件重命名”和“目录文件重命名”。
图像模糊改为“平均模糊”算法，它足够好且更快。

2018-12-31 版本4.6  编辑文本：自动检测换行符；转换换行符；支持LF（Unix/Linux）、CR（iOS）、CRLF（Windows）。
查找与替换，可只本页查找、或整个文件查找。
行过滤，匹配类型：“包含字串之一”、“不包含所有字串”，可累加过滤，可保存过滤结果。
分页：可用于查看和编辑非常大的文件，如几十G的运行日志；可设置页尺寸；对于跨页字符串确保查找、替换、过滤的正确性。
先加载显示首页，同时后端扫描文件以统计字符数和行数；统计期间部分功能不可用；统计完毕自动刷新界面。
进度等待界面添加按钮“MyBox”和“取消”，以使用户可使用其它功能、或取消当前进程。

2018-12-15 版本4.5 文字编码：自动检测或手动设置文件编码；设置目标文件编码以实现转码；支持BOM设置；
十六进制同步显示、同步选择；显示行号。批量文字转码。
图像分割支持按尺寸的方式。
可将图像或图像的选中部分复制到系统粘贴板（Ctrl-c）。
在查看图像的界面可裁剪保存。

2018-12-03 版本4.4 多帧图像文件的查看、提取、创建、编辑。支持多帧Tiff文件。
对于所有以图像文件为输入的操作，处理多帧图像文件的情形。
对于所有以图像文件为输入的操作，处理极大图像（加载所需内存超出可用内存）的情形。自动评估、判断、给出提示信息和下一步处理的选择。
对于极大图像，支持局部读取、边读边写的图像分割，可保存为多个图像文件、多帧Tiff、或者PDF。
对于极大图像，支持降采样。可设置采样区域和采样比率。

2018-11-22 版本4.3 支持动画Gif。查看动画Gif：设置间隔、暂停/继续、显示指定帧并导览上下帧。
提取动画Gif：可选择起止帧、文件类型。
创建/编辑动画Gif：增删图片、调整顺序、设置间隔、是否循环、选择保持图片尺寸、或统一设置图片尺寸、另存，所见即所得。
更简洁更强力的图像处理“范围”：全部、矩形、圆形、抠图、颜色匹配、矩形中颜色匹配、圆形中颜色匹配；
颜色匹配可针对：红/蓝/绿通道、饱和度、明暗、色相；可方便地增减抠图的点集和颜色列表；均可反选。
归并图像处理的“颜色”、“滤镜”、“效果”、“换色”，以减少界面选择和用户输入。
多图查看界面：可调整每屏文件数；更均匀地显示图片。

2018-11-13 版本4.2 图像处理的“范围”：全部、抠图、矩形、圆形、色彩匹配、色相匹配、矩形/圆形累加色彩/色相匹配。
“抠图”如PhotoShop的魔术棒或者windows画图的油漆桶。
“范围”可应用于：色彩增减、滤镜、效果、卷积、换色。可简单通过左右键点击来确定范围。
卷积管理器：可自动填写高斯分布值；添加处理边缘像素的选项。
目录重命名：可设置关键字列表来过滤要处理的文件。
调整和优化图像处理的代码。
更多的快捷键。

2018-11-08 版本4.1 图像的“覆盖”处理。可在图像上覆盖：矩形马赛克、圆形马赛克、矩形磨砂玻璃、圆形磨砂玻璃、或者图片。
可设置马赛克或磨砂玻璃的范围和粒度；可选内部图片或用户自己的图片；可设置图片的大小和透明度。
图像的“卷积”处理。可选择卷积核来加工图像。可批量处理。
卷积核管理器。自定义（增/删/改/复制）图像处理的卷积核，可自动归一化，可测试。提供示例数据。
图像滤镜：新增黄/青/紫通道。

2018-11-04 版本4.0  图像色彩调整：新增黄/青/紫通道。尤其黄色通道方便生成“暖色”调图片。
图像滤镜：新增“褐色”。可以生成怀旧风格的图片。
图像效果：新增“浮雕”，可以设置方向、半径、是否转换为灰色。
图像的混合：可设置图像交叉位置、可选择多种常用混合模式。
在线帮助：新增一些关键信息。

2018-10-26 版本3.9  内嵌Derby数据库以保存程序数据；确保数据正确从配置文件迁移到数据库。
图像处理：保存修改历史，以便退回到前面的修改；用户可以设置历史个数。
用户手册的英文版。

2018-10-15 版本3.8 优化代码：拆分图像处理的大类为各功能的子类。
优化界面控件，使工具更易使用。设置快捷键。
图像处理添加三个滤镜：红/蓝/绿的单通道反色。水印文字可以设置为“轮廓”。

2018-10-09 版本3.7 微博截图工具：利用Javascript事件来依次加载图片，确保最小间隔以免被服务器判定为不善访问，
同时监视最大加载间隔以免因图片挂了或者加载太快未触发事件而造成迭代中断。
图像处理“效果”：模糊、锐化、边沿检测、海报（减色）、阈值化。

2018-10-04 版本3.6 微博截图工具：继续调优程序逻辑以确保界面图片全部加载；整理代码以避免内存泄露。
降低界面皮肤背景的明亮度和饱和度。
在文档中添加关于界面分辨率的介绍。

2018-10-01 版本3.5 微博截图工具：调优程序逻辑，以确保界面图片全部加载。
提供多种界面皮肤。

2018-09-30 版本3.4 修正问题：1）微博截图工具，调整页面加载完成的判断条件，以保证页面信息被完整保存。
2）关闭/切换窗口时若任务正在执行，用户选择“取消”时应留在当前窗口。
新增功能：1）可以设置PDF处理的最大主内存和临时文件的目录；2）可以清除个人设置。

2018-09-30 版本3.3 最终解决微博网站认证的问题。已在Windows、CentOS、Mac上验证。

2018-09-29 版本3.2 微博截图功能：1）在Linux和Windows上自动导入微博证书而用户无需登录可直接使用工具。
但在Mac上没有找到导入证书的途径，因此苹果用户只好登录以后才能使用。
2）可以展开页面上所有评论和所有图片然后截图。
3）可以将页面中所有图片的原图保存下来。（感觉好酷）

2018-09-26 版本3.1 所有图像操作都可以批量处理了。修正颜色处理算法。
设置缺省字体大小以适应屏幕分辨率的变化。用户手册拆分成各个工具的分册了。
提示用户：在使用微博截图功能之前需要在MyBox浏览器里成功登录一次以安装微博证书、
（正在寻求突破这一限制的办法。Mybox没有兴趣接触用户个人信息）。

2018-09-18 版本3.0 微博截图工具：可以只截取有效内容（速度提高一倍并且文件大小减小一半）、
可以展开评论（好得意这个功能！）、可以设置合并PDF的最大尺寸。
修正html编辑器的错误并增强功能。

2018-09-17 版本2.14 微博截图工具：设置失败时重试次数、以应对网络状况很糟的情况；
当某个月的微博页数很多时，不合并当月的PDF文件，以避免无法生成非常大的PDF文件的情况（有位博主一个月发了36页微博~）。。

2018-09-15 版本2.13 分开参照图和范围图。确保程序退出时不残留线程。批量PDF压缩图片。
微博截图工具：自动保存任意微博账户的所有微博内容，可以设置起止月份，可以截图为PDF、也可以保存html文件
（由于微博是动态加载内容，本地网页无法正常打开，仅供获取其中的文本内容）。
如果微博修改网页访问方式，此工具将可能失效。

2018-09-11 版本2.12 合并多个图片为PDF文件、压缩PDF文件的图片、合并PDF、分割PDF。 
支持PDF写中文，程序自动定位系统中的字体文件，用户也可以输入ttf字体文件路径。 
提示信息的显示更平滑友好。网页浏览器：字体缩放，设置截图延迟、截图可保存为PDF。

2018-09-06 版本2.11 图片的合并，支持排列选项、背景颜色、间隔、边沿、和尺寸选项。
网页浏览器，同步网页编辑器，把网页完整内容保存为一张图片。图片处理：阴影、圆角、加边。
确保大图片处理的正确性和性能。

2018-08-11 版本2.10 图像的分割，支持均等分割个和定制分割。使图像处理的“范围”更易用。
同屏查看多图不限制文件个数了。

2018-08-07 版本2.9 图像的裁剪。图像处理的“范围”：依据区域（矩形或圆形）和颜色匹配，可用于局部处理图像。

2018-07-31 版本2.8 图像的切边、水印、撤销、重做。Html编辑器、文本编辑器。

2018-07-30 版本2.7 图像的变形：旋转、斜拉、镜像。

2018-07-26 版本2.6 增强图像的换色：可以选择多个原色，可以按色彩距离或者色相距离来匹配。支持透明度处理。

2018-07-25 版本2.5 调色盘。图像的换色：可以精确匹配颜色、或者设置色距，此功能可以替换图像背景色、或者清除色彩噪声。

2018-07-24 版本2.4 完善图像处理和多图查看：平滑切换、对照图、像素调整。

2018-07-18 版本2.3 闹钟，包括时间选项和音乐选项，支持wav铃音和MP3铃音，可以在后端运行。感谢我家乖乖贡献了“喵”。

2018-07-11 版本2.2 修正线程处理逻辑的漏洞。整理文件，将文件按修改时间或者生成时间重新归类在新目录下。
此功能可用于处理照片、游戏截图、和系统日志等需要按时间归档的批量文件。

2018-07-09 版本2.1 完善图片处理的界面，支持导览。
目录同步，包含复制子目录、新文件、特定时间以后已修改文件、原文件属性，以及删除源目录不存在文件和目录，等选项。

2018-07-06 版本2.0 批量提取PDF文字、批量转换图片。
目录文件重命名，包含文件名和排序的选项，被重命名的文件可以全部恢复或者指定恢复原来的名字。

2018-07-03 版本1.9 修正问题。提取PDF文字时可以定制页分割行。
完善图像处理：参数化调整饱和度、明暗、色相；滤镜：灰色、反色、黑白色。

2018-07-01 版本1.8 将PDF文件中的文字提取出来。处理图片：调整饱和度、明暗，或者转换为灰色、反色。

2018-06-30 版本1.7 完善像素计算器。支持同屏查看最多十张图，可以分别或者同步旋转和缩放。

2018-06-27 版本1.6 将图片转换为其它格式，支持色彩、长宽、压缩、质量等选项。
提供像素计算器。新增图像格式：gif, wbmp, pnm, pcx。

2018-06-24 版本1.5 提取PDF中的图片保存为原格式。
支持批量转换和批量提取。感谢 “https://shuge.org/” 的帮助：书格提出提取PDF中图片的需求。

2018-06-21 版本1.4 读写图像的元数据,目前支持图像格式：png, jpg, bmp, tif。
感谢 “https://shuge.org/” 的帮助：书格提出图像元数据读写的需求。

2018-06-15 版本1.3 修正OTSU算法的灰度计算；优化代码：提取共享部件；支持PDF密码；使界面操作更友好。

2018-06-14 版本1.2 针对黑白色添加色彩转换的选项；自动保存用户的选择；优化帮助文件的读取。
感谢 “https://shuge.org/” 的帮助：书格提出二值化转换阈值的需求。

2018-06-13 版本1.1 添加：转换格式tiff和raw，压缩和质量选项，以及帮助信息。
感谢 “https://shuge.org/” 的帮助：书格提出tiff转换的需求。

2018-06-12 版本1.0 实现功能：将PDF文件的每页转换为一张图片，包含图像密度、类型、格式等选项，并且可以暂停/继续转换过程。
```

# 实现基础
MyBox使用NetBeans 8.2和JavaFX Scene Builder 2.0开发：

[https://netbeans.org/](https://netbeans.org/)

[https://www.oracle.com/technetwork/java/javafxscenebuilder-1x-archive-2199384.html](https://www.oracle.com/technetwork/java/javafxscenebuilder-1x-archive-2199384.html)


基于以下开源软件/开源库：

[JavaFx  https://docs.oracle.com/javafx/2/](https://docs.oracle.com/javafx/2/)
	
[PDFBox  https://pdfbox.apache.org/](https://pdfbox.apache.org/)
	
[jai-imageio  https://github.com/jai-imageio/jai-imageio-core](https://github.com/jai-imageio/jai-imageio-core)
	
[javazoom  http://www.javazoom.net/index.shtml](http://www.javazoom.net/index.shtml)
	
[log4j   https://logging.apache.org/log4j/2.x/](https://logging.apache.org/log4j/2.x/)
	
[Derby   http://db.apache.org/derby/](http://db.apache.org/derby/)

[GifDecoder   https://github.com/DhyanB/Open-Imaging/](https://github.com/DhyanB/Open-Imaging/)

[EncodingDetect  https://www.cnblogs.com/ChurchYim/p/8427373.html](https://www.cnblogs.com/ChurchYim/p/8427373.html)

[Free Icons  https://icons8.com/icons/set/home](https://icons8.com/icons/set/home)


# 主界面
![About](https://mararsh.github.io/MyBox/0.png)

![About](https://mararsh.github.io/MyBox/1.png)

![About](https://mararsh.github.io/MyBox/2.png)

![About](https://mararsh.github.io/MyBox/3.png)

![About](https://mararsh.github.io/MyBox/4.png)







