# PeriodicalExecutor设计

## 添加任务

* 当前没有未执行的任务
  * 添加并启动定时器
* 已有未执行的任务
  * 添加并检查是否到达最大缓存数
    * 如到，执行所有缓存任务
    * 未到，只添加

## 定时器到期

* 清除并执行所有缓存任务
* 再等待N个定时周期，如果等待过程中一直没有新任务，则退出
