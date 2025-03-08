# 适用于Liquipedia HoK Wiki的BP低代码编辑器

本Demo实现了Liquipedia的*Ban&Picks*格式化输出，降低了由于输出错误导致的增加检查成本，并提升了一定的编写效率。

#### 页面效果

![主界面](images/01.png)

#### 输出效果

##### 5Ban5Pick

```yaml
        |team1side=blue|team2side=red|length=00:00|winner=1
        <!-- Hero picks -->
        |t1h1=|t1h2=|t1h3=|t1h4=|t1h5=
        |t2h1=|t2h2=|t2h3=|t2h4=|t2h5=
        <!-- Hero bans -->
        |t1b1=|t1b2=|t1b3=|t1b4=|t1b5=
        |t2b1=|t2b2=|t2b3=|t2b4=|t2b5=
```

##### 4Ban5Pick

```yaml
        |team1side=blue|team2side=red|length=00:00|winner=1
        <!-- Hero picks -->
        |t1h1=|t1h2=|t1h3=|t1h4=|t1h5=
        |t2h1=|t2h2=|t2h3=|t2h4=|t2h5=
        <!-- Hero bans -->
        |t1b1=|t1b2=|t1b3=|t1b4=
        |t2b1=|t2b2=|t2b3=|t2b4=
```

##### 巅峰对决

```yaml
        |team1side=blue|team2side=red|length=00:00|winner=1
        <!-- Hero picks -->
        |t1h1=|t1h2=|t1h3=|t1h4=|t1h5=
        |t2h1=|t2h2=|t2h3=|t2h4=|t2h5=
```

#### 使用帮助

BP输入框支持提示词，本Demo支持了***Honor of Kings（包括国际服）***的绝大部分别名提示，您也可以通过修改***data.js***的***dataArray***数组进行修改。支持一个英雄设置多个**别名**，值对应如下：

| 名称  | 值           |
| ----- | ------------ |
| vulue | 最终的输出值 |
| text  | 提示词       |
| alias | 别名         |

您同样可以替换其他游戏的对应关系，或许您可以直接询问大语言模型将目标输出为对应格式获取。

```javascript
export const dataArray = [
    // 默认空值
    { "value": "", "text": "Null","alias":""},
    // 输出示例
    { "value": "agudo", "text": "Agudo (阿古朵)","alias":"aguduo"},
    { "value": "agudo", "text": "Agudo (阿古朵)","alias":"a gu duo"}
}
```

如果您计划在本地运行，推荐使用VS Code的***Live Server***插件部署此Demo，带来的诸多不便敬请谅解。

#### 最后

由于时间仓促，本Demo存在诸多不足，欢迎通过Issue向我提出！