2.0.0 / 2015-11-20
==================
 * 优化渲染效率
 * 添加G.GeomUtil类帮助操作几何对象，包含了判断几何类型geomType()、获取质心centroid()、获取标注点labelPoint()等方法
 * 添加fluid模块用于可视化流体场数据
 * 新增Graphic.Arrow类型，用于绘制箭头
 * 给maps模块添加Google中国地图的支持
 * 编辑Polyline和Polygon的时候在线段中点添加辅助节点，并可以点击删除节点
 * 给Point添加textAlign选项帮助控制文字的左右和居中对齐
 * 添加virtualclick事件帮助绘制等交互更实时地进行
 * 给Layer.Heat添加minOpacity和maxOpacity选项，废弃原来的opacity选项
 * 添加bind、unbind、fire分别为addListener、removeListener、fireEvent的别名
 * 给WebGL的Map添加双缓存
 * 修正有多个Layer.Graphic时鼠标移动到某些Graphic上还能拖动地图的问题
 * 修正WebGL模式下遮罩绘制错误的问题
 * 修正若干VML模式下的问题


1.9.1 / 2015-11-4
==================
 * 去除捏合操作的空程设置，防止在某些情况下导致旋转不同步


1.9.0 / 2015-11-3
==================
 * 给Graphic.Point增加可以指定文本对齐方式的功能
 * 修正Canvas对应的绘图尺寸有时候没有更新的问题
 * 修正Layer.Heat有时候会使用错误的画布尺寸进行绘制的问题
 * 避免记录地图状态操作在通过file:///方式访问页面时导致JavaScript报错
 * 改进连续滚动鼠标情况下的效率
 * 将缩放、平移、旋转动画的默认持续时间从0.5秒改为0.3秒，这样会让用户感觉更流畅一点
 * 避免鼠标在地图上移动时不必要的重绘


1.8.3 / 2015-10-23
==================
 * 修正某些特殊情况下试图触发已经被移除的Graphic的Mouse事件


1.8.2 / 2015-8-24
==================
 * 修正Layer.Html的clear()方法无效的问题
 * 添加百度街道地图的高清支持


1.8.1 / 2015-7-30
==================
 * 优化Canvas绘图效果，使其在Windows下显示更加清晰
 * 修正错误地关闭了CSS 3D加速的问题


1.8.0 / 2015-7-28
==================
 * 给Map添加打印成图片的功能
 * 修正移动设备上点击Logo链接无效的问题
 * 使捏合操作支持continuouslyZoom选项
 * 修正捏合操作触发不该触发的click事件的问题
 * 修正Layer.Graphic没有对象时调用calcDataExtent()方法报错的问题
 * 修正在移动设备上捏合操作时指定Layer.Html图层隐藏无效的问题


1.7.1 / 2015-7-20
==================
  * 改善draw模块绘制矩形功能在移动设备上的体验
  * 修复Layer.Html缩放时候位置错位的问题
  * 修复有些Layer的hide()方法不起作用的问题
  * 更改一些Layer的crossOrigin选项默认值为空字符串


1.7.0 / 2015-7-14
==================
  * 添加Layer.Image用于支持直接放置图片于地图中，并可随着地图缩放
  * 给draw模块中的Layer.Draw添加绘制矩形的方法
  * 修正按住shift从右侧向左侧画矩形框缩放到错误地点的问题
  * 给Map添加canvasAnimRedraw选项，用以改善canvas模式下地图动画效率


1.6.3 / 2015-6-8
==================
  * 添加关于云端使用的文档


1.6.2 / 2015-6-4
==================
  * 给Layer.Heat添加drawOnAnim选项，默认在动画时不进行重绘
  * 修复Graphic.Polyline初始化时候没有正确继承attrs和options的问题
  * 修复Map初始的minRes值精度不够的问题
  * 更新地图自带Logo
  * 给Map添加scrollPage选项，使页面滚动的事件可被选择性地使用


1.6.1 / 2015-5-29
==================
  * 修正ExtentUtils相交操作会返回不合法结果的问题
  * 修复Graphic.Polyline的样式没有正确更新的问题


1.6.0 / 2015-5-18
==================
  * 添加Layer.TiledService类用于通用地加载分片数据
  * 移除Layer.FeatureService构造函数中的url属性
  * 给Layer添加getOrder()和bringToOrder()方法用于调整图层顺序
  * 提升Layer.Heat的性能
  * 修正将Chrome浏览器判断为Safari的问题
  * 给Layer.Tile添加tileEnlarge选项，如果设置为false可以避免半透明瓦片相互重叠


1.5.0 / 2015-4-14
==================
  * 给Graphic添加allowPan选项，允许地图拖动操作发生在Graphic上
  * 给高端Android的chromelite核心浏览器打开Canvas能力
  * 更新Layer.Label的URL模式到最新的格式
  * 给Layer添加clear()方法


1.4.0 / 2015-3-9
==================
  * 修改Layer.Html的add(),remove(),get()方法为addHtml(),removeHtml(),getHtml()


1.3.1 / 2015-2-9
==================
  * 修正draw模块中如果绘制后将图形设置为clickable后，地图不能拖动的问题
  * 修正layer的remove()方法错误地移除若干事件监听的问题


1.3.0 / 2015-1-21
==================
  * 给Layer.Tile添加opacity选项用于设置透明度
  * 修正cluster模块中如果设置showRelRes参数会有绘制错误的问题
  * 给Map添加wrap选项，用以支持360度连续地图
  * 修正safari浏览器中有时瓦片图之间会出现空白细线的问题


1.2.1 / 2015-1-7
==================
  * 针对iPhone6 Plus进行性能优化
  * 修正某些移动设备上SVG的元素不能正确清除的问题
  * 给触摸设备添加双指轻按缩小地图的功能
  * 修复跨域图片在WebGL模式中不能加载的问题


1.2.0 / 2014-12-29
==================
  * 给geogrid添加一些属性
  * 给Logo添加网站超链接
  * 修正通过initStatus设置Map初始旋转角度时不显示罗盘的问题
  * 在某些不支持硬件加速的设备上关闭Canvas绘图模式
  * 修正SVG模式下第一次捏合操作会导致图形闪烁的问题


1.1.0 / 2014-12-9
==================
  * 增加geogrid模块，用于绘制地理网格
  * 修正draw模块中的Layer.Draw的endDraw()方法会导致触发两次drawEnd事件的问题
  * 修正多边形的hit判断，如果正好在顶点判断为true
  * 修正G.Layer.Graphic的all()和count()方法将编辑的节点也计入图形对象的问题


1.0.0 / 2014-11-26
==================
  * 发布第一个对外版本



0.0.1 - 0.15.2
==================
  * 内测版本