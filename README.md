# Low-Code Editor

This Demo implements [***Liquipedia***](https://liquipedia.net/honorofkings/)'s *Ban&Picks* formatting output, which reduces the increased inspection cost caused by output errors and improves certain writing efficiency.

#### Page Effect

![Main](images/01.png)

#### Output effect

##### 5Ban & 5Pick

``` yaml
        |team1side=blue|team2side=red|length=00:00|winner=1
        <!-- Hero picks -->
        |t1h1=|t1h2=|t1h3=|t1h4=|t1h5=
        |t2h1=|t2h2=|t2h3=|t2h4=|t2h5=
        <!-- Hero bans -->
        |t1b1=|t1b2=|t1b3=|t1b4=|t1b5=
        |t2b1=|t2b2=|t2b3=|t2b4=|t2b5=
```

##### 4Ban & 5Pick

``` yaml
        |team1side=blue|team2side=red|length=00:00|winner=1
        <!-- Hero picks -->
        |t1h1=|t1h2=|t1h3=|t1h4=|t1h5=
        |t2h1=|t2h2=|t2h3=|t2h4=|t2h5=
        <!-- Hero bans -->
        |t1b1=|t1b2=|t1b3=|t1b4=
        |t2b1=|t2b2=|t2b3=|t2b4=
```

##### Ultimate Battle

``` yaml
        |team1side=blue|team2side=red|length=00:00|winner=1
        <!-- Hero picks -->
        |t1h1=|t1h2=|t1h3=|t1h4=|t1h5=
        |t2h1=|t2h2=|t2h3=|t2h4=|t2h5=
```

##### Only Need 4Bans

```yaml
        <!-- Hero bans -->
        |t1b1=|t1b2=|t1b3=|t1b4=
        |t2b1=|t2b2=|t2b3=|t2b4=
```

##### Only Need 5Bans

```yaml
        <!-- Hero bans -->
        |t1b1=|t1b2=|t1b3=|t1b4=|t1b5=
        |t2b1=|t2b2=|t2b3=|t2b4=|t2b5=
```

#### Using Help

The BP input box supports prompt words. This Demo supports most alias prompts for ***Honor of Kings (including Global services)***. You can also modify them by modifying the ***dataArray*** array of  ***data.js*** . Support setting multiple  ***aliases*** for a hero, and the corresponding values are as follows:

| name  | value              |
| ----- | ------------------ |
| vulue | Final output value |
| text  | prompt words       |
| alias | alias (DIY)        |

You can also replace the corresponding relationships of other games. Maybe you can directly ask the [GPT](https://AI.com/) to obtain the target output in the corresponding format.

``` javascript
export const dataArray = [
	//Default null value
	{ "value": "", "text": "Null","alias":""},
	//Output example
	{ "value": "agudo", "text": "Agudo","alias":"aguduo"},
	{ "value": "agudo", "text": "Agudo","alias":"a gu duo"}
}
```

If you plan to run it locally, it is recommended to use [Visual Studio Code](https://code.visualstudio.com/)'s **Live Server** plug-in to deploy this Demo. Please understand the inconvenience caused.

#### Finally

Due to the rush of time, this Demo has many shortcomings. Welcome to raise them to me through Issue!