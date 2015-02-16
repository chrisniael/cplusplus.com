宏

# FE_DOWNWARD (C++11)

这个宏展开成一个 _int_ 型值，来为函数 [fegetround](fegetround.md) 和 [fesetround](fesetround.md) 表示 _向下取整方向模式_ 。

向下舍入 x 就是选择不大于 x 的最大的值。

可能的 _舍入方向模式_ 是：

宏值  | 描述
----- | ------
[FE_DOWNWARD](FE_DOWNWARD.md) | 向下舍入
[FE_TONEAREST](FE_TONEAREST.md) | 四舍五入
[FE_TOWARDZERO](FE_TOWARDZERO.md) | 向零舍入
[FE_UPWARD](FE_UPWARD.md) | 向上舍入


## 另请参阅

宏/函数                            | 描述
---------------------------------- | -------------------------
[FE\_TONEAREST](FE_TONEAREST.md)   | 四舍五入模式 (_宏_)
[FE\_TOWARDZERO](FE_TOWARDZERO.md) | 朝零舍入模式 (_宏_)
[FE\_UPWARD](FE_UPWARD.md)         | 向上舍入模式 (_宏_)
[fegetround](fegetround.md)        | 获得舍入方向模式 (_函数_)
[fesetround](fesetround.md)        | 设置舍入方向模式 (_函数_)
