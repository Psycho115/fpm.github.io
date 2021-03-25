# 步长控制 `TIME`

- 除了`INITIAL`求解步之外，其余类型的求解步`TIME`参数必须设置

---

## 输入格式

> stepName, `TIME`, $t_{total}$, $h$, $b_{autoH}$

| 参数               | 说明                                                      |
| ------------------ | --------------------------------------------------------- |
| `KEYWORD` = `TYPE` |                                                           |
| $t_{total}$        | 求解步总时长，默认                                        |
| $h$                | 求解步初始时间步长                                        |
| $b_{autoH}$        | 是否开启自动时间步长，`ON` 为开启，`OFF` 为关闭，默认关闭 |

**注**：若开启自动时间步长，$h$ 参数为求解初始时刻的时间步长，否则为全程恒定步长

## 前置条件

- [求解步类型 `TYPE`](/step/GENERAL/TYPE.md) 已设置

## 示例

```c
step1, STEP_TYPE, STATIC
step1, TIME, 5.0, 1e-4, OFF
```