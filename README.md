### 贪吃蛇

1. 游戏逻辑
    * 屏幕上随机出现一个点，表示“食物”，上下左右控制“蛇”的移动，吃到“食物”以后“蛇”的身体加长
    * “蛇”碰到边框或自己的身体
2. 游戏设计
    * 用一个列表来存放“蛇身”的坐标
    * 将下一格的坐标添加到列表开头，并移除列表的最后一个元素，就相当于蛇向前移动了一格
    * 我们的“蛇”是一个列表，那么只要判断下一格的坐标是否已经包含在“蛇”的列表中岂不就可以判断是否碰到自己了呢
3. 关键技术
    * pygame
    * 由于程序中要频繁的对“蛇”进行头尾的添加和删除操作，为了性能更好那么一点，我们用 deque 代替列表
4. 将要做
    * 加上自动寻找导航（就是接下来的任务了）