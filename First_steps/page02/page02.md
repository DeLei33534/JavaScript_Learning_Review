## 像程序员一样思考
学习编程，语法本身并不难，真正困难的是如何应用语言来解决现实世界的问题
  1. 运行程序的目的
  2. 为实现目的，选定的代码类型
  3. 如何使项目代码协同运行

## 猜数字游戏示例
1. 产品需求
   1. 开发一个猜数字游戏。游戏应随机选择一个 100 以内的自然数, 然后邀请玩家在 10 轮以内猜出这个数字
   2. 每轮后，都应告知玩家的答案正确与否
   3. 如果玩家猜测错误，应显示"你猜错了！"，并告知玩家，本次数字是低还是高
   4. 应显示出玩家前一轮所猜的数字
   5. 一旦玩家猜对，或者用尽所有机会，游戏将结束
   6. 成功猜对，显示"恭喜你！猜对了！";机会用尽仍为猜对，显示"!!!GAME OVER!!!"
   7. 游戏结束后，可以让玩家选择是否再次开始
2. 需求拆解
   1. 能够随机生成一个 100 以内的自然数
   2. 能够记录玩家当前的轮数，从 1 开始
   3. 应该为玩家提供一种猜测数字的方法
   4. 一旦有结果提交，先将其记录下来，以便用户可以看到他们先前的猜测
   5. 然后检查它是否正确
   6. 如果正确:
      1. 显示祝贺消息
      2. 阻止玩家继续猜测，游戏结束
      3. 展示控件，允许玩家重新开始游戏
   7. 如果出错，且玩家有剩余轮次:
      1. 告知玩家，他们错误类别(高或低)
      2. 允许玩家输入另一个猜测
      3. 轮数加 1
   8. 如果出错，并且玩家没有剩余轮次:
      1. 告诉玩家游戏结束
      2. 阻止玩家继续猜测
      3. 展示控件，允许玩家重新开始游戏
   9. 当游戏重启时，确保游戏的逻辑和UI完全重置，并返回步骤1
3. 代码实现(demo01-07)
   