# pygame-pgGoGo
简易的pygame游戏开发框架，分享学习

2021/1/26 1.9版本更新
- 新增OnMouseEnter 当鼠标进入到对象的矩形区域内事件
- 新增OnMouseOut 当鼠标离开对象的矩形区域内事件
- Resource类新增name属性，保存对象名字
- Resource类新增collideList属性，保存所有被碰撞到的角色，每次Move移动前都会被清空
- Resource类新增Move函数，可以移动对象到偏移的坐标，可以选择不能移动到屏幕外，
并且移动完毕后可以得到碰撞到的所有对象列表，保存在collideList中
- Resource类新CollidelistCheck(self, group_list:list), 跟所有列表组内的精灵组依次检测碰撞并
得到所有被碰撞到的对象
- Resource类新Home()，坐标重置到初始化创建对象的原始坐标
- 新增Label组件类，用于显示文字
- 新增新的bat快速创建组件

2021/1/25 1.8版本更新
-  修正了MultiFrameImage类的渲染动画帧的问题
现在创建动态图不提供动图组的序列帧文件夹，就默认用框架自带的

-  在框架内增加有files文件，内置快速创建组件bat
点击你需要创建的组件bat，输入类的名称即可自动生成脚本

2021/1/24 1.7版本更新
- Resource类添加新属性visible
用于控制这个组件是否显示，所有组件的默认为True
可用SetVisible来设为False，不显示(不参与绘制并且不在任何精灵组内)
