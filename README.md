# games103
如题，games103的lab

# games103-Lab1

## 实现了lab1的刚体

​	其实本身这个lab不算很难写，重点在于看懂代码，以及熟悉一下unity。	

### start函数

在start函数中计算了转动惯量，同时示范了通过mesh取得点的做法，这个在之后也会用到



### Collision_Impulse函数

在这个函数中要完成碰撞，其实就是实现ppt上的流程

#### 需要注意的点

- 先计算出所有的和平面碰撞的点，接着再取一个平均的位置，对这个位置进行处理，也就是单独的对这个平均得到的点进行计算中间速度，来得到冲量
- 在计算的过程中要注意转动惯量在转动后也需要修改
-  **特别要注意的是除以0的情况，在没有碰撞的情况下，碰撞的点的计数值一直为0**
- **如果你碰到以下情况：**
  - 兔子看起来只和一面墙有碰撞，另外一面没有碰撞
    - 可以尝试：
      修改初速度，并观察一定的时间
    - 如果出现兔子的行为并不稳定，可能到处乱飞的情况
    - 请检查你计算角速度的线速度的时候使用的向量，
    - 这里要使用的是还是相对于质心的向量，而不是真实的向量（对不起我的物理老师，笑）

## 对于unity的吐槽

虽然，说明里面已经描述了unity的数学库的缺失，但是实际上用起来，还是很不习惯。

**不如eigen**

**不如eigen**

**不如eigen**

哼~

