# 佳明运动数据同步与采集工具

<a style="display:inline-block;background-color:#FC5200;color:#fff;padding:5px 10px 5px 30px;font-size:11px;font-family:Helvetica, Arial, sans-serif;white-space:nowrap;text-decoration:none;background-repeat:no-repeat;background-position:10px center;border-radius:3px;background-image:url('https://badges.strava.com/logo-strava-echelon.png')" href='https://strava.com/athletes/84396978' target="_clean">
  关注作者Strava
  <img src='https://badges.strava.com/logo-strava.png' alt='Strava' style='margin-left:2px;vertical-align:text-bottom' height=13 width=51 />
</a>


**自动 安全 省心**

此工具实现了佳明运动活动数据（生理数据如睡眠，身体电量，**步数**
等除外）的一次性迁移与日常运动数据同步，实现同步运动数据到到Strava [Strava全球热图](https://www.strava.com/heatmap) 。 额外还实现了RQ数据采集记录跑力的长期趋势及自动签到。

## 功能

### 迁移数据

- 支持佳明账号中已有的运动数据从中国区一次性迁移到国际区。对应 `Action`: `Migrate Garmin CN to Garmin Global`
- 支持佳明账号中已有的运动数据从国际区一次性迁移到中国区。对应 `Action`: `Migrate Garmin Global to Garmin CN`

### 同步数据

- 约每20分钟左右检查当前中国区账号中是否有新的运动数据，如有则自动下载上传到国际区，并同步到Strava。 对应 `Action`: `Sync Garmin CN to Garmin Global`
- 如果您常用的是国际区，想要在国内运动软件（悦跑圈/咕咚/keep/郁金香等等）同步运动数据及微信运动中显示 【Garmin手表 骑行xx分钟】（[微信运动效果](./assets/wx_sport.jpg)）
  此工具可以实现自动反向同步中国区。
  ~~因为使用人数很少，功能没有放出来，有需要可以单独联系我~~。 【2022-9-1】 已验证完成并开放出来，感谢 @南宫 支持开发！**
  如无特殊需求，强烈建议不要将两个同步脚本同时打开，按需开启一个即可！** 对应 `Action`: `Sync Garmin Global to Garmin CN`

### 采集数据

- 采集RQ统计数据到GoogleSheets，记录跑力的长期趋势。参见： [RQ数据采集到GoogleSheets教程](RQ_GoogleSheets.md)
- RQ自动签到。参见：[RQ自动签到](RQ_Sign.md)

## 说明

#### 免责声明：

本工具仅限用于学习和研究使用，不得用于商业或者非法用途。如有任何问题可联系本人删除。

#### 账号安全：

账号及密码保存在自己的 `github secrets` 中，不会泄露，运行代码均 **开放源码**，欢迎提交`PR`。

#### 进群讨论

为方便讨论，请加我绿色软件：`nononopass` （[二维码扫码](./assets/wechat_qr.png)） 我拉你进群。

#### 支持作者

如果帮助到了你，可以 [Buy Me a Coffee](#buy-me-a-coffee)，赞助者会在文章下方留下ID表示感谢🙏。

#### 关键更新日志

- 2022-09-01: 新增支持国际区同步新数据到中国区（ 特别感谢 @南宫 支持开发！）
  - 新增一个`action`：`Sync Garmin Global to Garmin CN`，开启后自动执行。与同步中国区到国际区操作一致。
- 2022-08-07: 支持国际区迁移数据到中国区
  - 新增一个`action`：`Migrate Garmin Global to Garmin CN`，手动执行。与迁移中国区到国际区操作一致。
- 2022-06-15: 增加佳明中国区迁移及同步国际区数据功能，同步strava
- 2022-06-06: 采集RQ统计数据到Google表格

<details>
<summary>

#### 在用这个工具的朋友们(点击展开) （[填写您的链接](https://wj.qq.com/s2/10633783/a1ef/)）

</summary>

| 名称            | Strava运动员链接                                 |           |
|:--------------|:--------------------------------------------|:----------|
| Zhitao Yan    | https://www.strava.com/athletes/84396978    | ‍💻Author |
| Clown jiang   | https://www.strava.com/athletes/105952743   | ✨Sponsor  |
| 老弟            | https://www.strava.com/athletes/91478457    | ✨Sponsor  |
| Zax Wen       | https://www.strava.com/athletes/91553718    | ✨Sponsor  |
| 李二牛           | https://www.strava.com/athletes/43684509    | ✨Sponsor  |
| 围脖B站@我是冯瑞恒    | https://www.strava.com/athletes/34349982    | ✨Sponsor  |
| 刘             | https://www.strava.com/athletes/67222235    | ✨Sponsor  |
| 狼朗            | https://www.strava.com/athletes/43107517    | ✨Sponsor  |
| 微醺漂移          | https://www.strava.com/athletes/19108713    | ✨Sponsor  |
| hua xu        | https://www.strava.com/athletes/40855048    |           |
| L.X           | https://www.strava.com/athletes/86727066    |           |
| 姜宁            | https://www.strava.com/athletes/54001163    |           |
| jogging tiger | https://www.strava.com/athletes/105416045   |           |
| Eph           | https://www.strava.com/athletes/8376311     |           |
| YunBond       | https://www.strava.com/athletes/33650658    |           |
| ygnnbpkn      | https://www.strava.com/athletes/107433069   |           |
| HY.Dong       | https://www.strava.com/athletes/8901566     |    ✨Sponsor       |
| 陆凡            | https://www.strava.com/athletes/48067019    |      ✨Sponsor     |
| JiaJian He    |     https://www.strava.com/athletes/13495215|     ✨Sponsor      |
| 生如胡杨          | https://www.strava.com/athletes/107773658   | ✨Sponsor          |
| doudouhuang   | https://www.strava.com/athletes/107830101   |           |
| 解凌曦           | https://www.strava.com/athletes/62080682    |   ✨Sponsor        |
| 欢乐铁三陈琨        | https://www.strava.com/athletes/107733443   |           |
| Fseeeee       | https://www.strava.com/athletes/45675087    |           |
| 神月            | https://www.strava.com/athletes/69135349    |           |
|清风故人 | https://www.strava.com/athletes/105799254| |
|lu_yuanyuan | https://www.strava.com/athletes/lu_yuanyuan| |
|axiuff | https://www.strava.com/athletes/107599333| |
|iceirislei | https://www.strava.com/athletes/84396978| |
|江小鱼 | https://www.strava.com/athletes/29648564| |
|作樂 | https://www.strava.com/athletes/102557902| |
|Ink Jiang | https://www.strava.com/athletes/107398383| |
|kk | https://www.strava.com/athletes/108302326| |
|Kailin Aogu | https://www.strava.com/athletes/108426264| |
|Jason | https://www.strava.com/athletes/78018552| |
|七叔uncle | https://www.strava.com/athletes/100219084| |
|lenmio | https://www.strava.com/athletes/23144564| |
|王冰 | https://www.strava.com/athletes/96827296| |
|AndrewRen | https://www.strava.com/athletes/47354232| |
|湖南吴彦祖 | https://www.strava.com/athletes/27560743| |

</details>

## 如何使用？

视频教程参考： [中国区佳明运动数据同步Strava视频教程](https://www.bilibili.com/video/BV1v94y1Q7oR/)

如果按照视频还是无法达到预期的效果(包括佳明国际区点不进去，跳转到com.cn、github 添加 secrets 没有反应等)，请自行解决不可描述的网络问题。 如果`github`
上的图片看不到，那大概率是被墙了，看图请移步 [知乎链接](https://zhuanlan.zhihu.com/p/543799435), 文档内容以`github` 版本为准，其他地方可能不是最新的。

### 迁移已有运动数据，并开启自动同步功能

流程：

`【运动】 🏃/🚴/🏊‍` --> GarminCN --> This Tool ⚡ --> Garmin Global --> Strava

思路：
> Strava仅支持关联国际区的佳明账号，所以需要提前自己创建国际区佳明账号，并用此账号关联绑定Strava


[佳明国际区网址](https://connect.garmin.com/signin/)

[佳明国区网址](https://connect.garmin.cn/signin/)

[Strava网址](https://www.strava.com/)

前置条件：**注册好佳明国际区的帐号及Strava账号，并已经将Strava与佳明国际区账号关联，并开启Strava数据权限（下图）**

![consent](./assets/consent.png)

如果是新注册的国际区账号，请确保账号隐私设置中的`存储和处理` 是 `同意`状态，`设备上传`是`已启用` 状态(下图)
，否则上传数据会报`412`错误码：`User explicity revoked consent for uploading files.`
![connect_permission](./assets/connect_permission.png)

如果你的中国区账号开启了两步验证，登录时需要验证码，请按照图中设置关闭

[https://www.garmin.cn/zh-CN/account/security/mfa](https://www.garmin.cn/zh-CN/account/security/mfa)
![mfa](./assets/mfa.jpg)

------

#### Step1: fork 此工程

点击【Fork】，**也请顺手点一下【Fork】旁边的【Star】，支持一下作者** ，fork到自己账号下。
![fork](./assets/fork.jpg)

#### Step2: 配置填入自己的佳明国内区、国际区账号及密码

如下图打开Secrets配置，点击 【New repository secret】
![settings](./assets/settings.jpg)

准备自己的帐号密码及要迁移的数据量

**佳明国内账号邮箱地址**：
GARMIN_USERNAME

**佳明国内账号密码**：
GARMIN_PASSWORD

**佳明国际账号邮箱地址**：
GARMIN_GLOBAL_USERNAME

**佳明国际账号密码**：
GARMIN_GLOBAL_PASSWORD

请先在connect网站看看要迁移的活动，写一个大概的数量： https://connect.garmin.cn/modern/activities

**要迁移的活动数量，先填1**:
GARMIN_MIGRATE_NUM

**从第几个活动开始迁移，先填 0**:
GARMIN_MIGRATE_START

![secrets](./assets/secrets.jpg)

填完后确保如下图红框内的都填上了, 红框外的不用管

![secrets](./assets/secrets_ok1.png)

#### Step3: 手动迁移已有数据

如下图，点击【Actions】--> 【 Migrate Garmin CN to Garmin 】 --> 【Run workflow】执行迁移数据
![migrate](./assets/migrate.jpg)
点击后刷新页面，可以看到正在执行的任务：
![migrating](./assets/migrating.jpg)
点进去后可以查看日志，如果 Run yarn migrate那一栏看到 userInfo cn 和 userInfo Global, 并且数据持续在滚动刷新，就说明正常运行
![test_migrate](./assets/test_migrate.png)
![log](./assets/log.jpg)

如果上面一切正常，运行结束后，前面会是一个绿色，代表运行完成。
![migrated](./assets/migrated.png)

这个时候，去佳明国际区和strava看看，是否有1条数据迁移过来，如果没有，代表有问题，请联系我咨询，如果有，代表正常运行。

(这一块如果看文字不是很清楚到话去看看文章开始部分的视频教程，参照看看)

上面正常的话开始迁移剩余数据

**回到 Step2 的地方，分别修改**

GARMIN_MIGRATE_NUM 为 100

GARMIN_MIGRATE_START 为 1

然后按照上面执行过的步骤，参照Step3再执行一次，执行成功后检查佳明国际区及Strava上是否迁移过来。如果成功，修改

GARMIN_MIGRATE_START 为 100，再次执行，确认成功后，每次 GARMIN_MIGRATE_START 的值 + 100，直到所有数据迁移完成。

> 迁移数据比较慢，请耐心等待，实测30分钟迁移100条左右

#### Step4: 自动同步新的运动数据

如图点击开启workflow
![enable_workflow](./assets/enable_workflow.jpg)
开启后无需额外配置，大约每20分钟左右自动同步一次数据，一段时间后可以查看同步记录
如果有问题，请发邮件联系我
![sync](./assets/sync.jpg)

#### FAQ:

##### 数据没有同步成功？

第一步请先检查手机connect，确保运动在connect看到才能进行后续的同步工作。

还有可能是定时执行没有执行，可以像执行MIGRATE那样手动执行SYNC脚本手动触发同步。

##### 数据同步为什么没有按计划执行，有的时候一小时才执行了2次？

参考： [Schedule every 5 mins but runs a bit randomly](https://github.community/t/schedule-every-5-mins-but-runs-a-bit-randomly/159355/2)

原因： github的定时计划任务以尽力而为的策略运行。

**我代码中写的是每10分钟执行一次，实际情况是大约每20分钟执行一次。**

尤其是早上8点左右，几乎都会延迟很久执行，原因是大概我们8点对应美国0点，其他很多程序的定时任务在0点执行，导致我们的任务抢不到计算资源，导致延迟执行。
着急的话上来手动执行一下就好。

文中建议改为每5分钟一次，但是如果这样的话会超出每月的免费可用额度。如果您急切的想同步数据，建议上来手动操作一下。

翻译：
>
> 欢迎来到 GitHub
> 支持社区！计划的操作工作流以尽力而为的策略运行。当您的计划到期时，您的工作流将添加到池中并在资源可用时运行。这意味着您可能会看到与您的计划时间和工作流运行的实际时间相比有所延迟，尽管这可能会导致更长的延迟，具体取决于当时可用的资源。
> 您可以安排工作流运行的最短时间为每 5 分钟一次。由于这种池化，如果在您的下一个计划设置为运行时，池中已经有运行等待，您可能会看到运行被“跳过”。
> 工程团队正在研究提高调度的可用性、扩展性和响应时间，但如果您需要精确的调度操作，那么您可能会更好地寻找替代解决方案，例如在您自己的
> VPS 上运行 cron。
>

##### 需要每天都来同步数据吗？

不用。上面的步骤执行过后，MIGRATE手动迁移已有数据，再有新跑的数据会在SYNC中大约每20分钟左右自动同步一次数据

##### 同步最新的代码库

代码可能有优化更新，如看到下图的情况，请点击下图红框更新到最新的代码，
![update_code](./assets/update_code.jpg)

## 数据同步到佳明国际区后，其他的一些可关联的运动分析平台

[https://app.trainingpeaks.com/#home](https://app.trainingpeaks.com/#home)

[https://runalyze.com/dashboard](https://runalyze.com/dashboard)

[https://intervals.icu/](https://intervals.icu/)

## 同步到佳明国际区，同步Strava

![garmin_global](./assets/garmin_global.png)
![strava](./assets/strava.png)

## 采集RQ数据教程：

点击跳转：[RQ数据采集到GoogleSheets教程](RQ_GoogleSheets.md)

## TODO

- [x] 采集RQ统计数据到Google表格
- [x] 一次性批量迁移已有活动数据到国际区
- [x] 自动同步新的活动数据到数据到国际区
- [x] 从国际区反向迁移同步到中国区功能
- [ ] Strava数据导出上传Garmin
- [ ] Connect API 异常出错时抛出`github actions`错误，避免内部运行失败但是外部显示成功的问题。
- [ ] Docker本地部署运行版本，不依赖GitHub Action，避免自动运行间隔不固定的问题。
- [ ] WebUI 管理同步及迁移任务
- [ ] 乳酸阈值长期趋势读取与分析页面
  - 参考帖子 https://www.reddit.com/r/Garmin/comments/x2mad3/lactate_threshold_accuracy_test_from_052019_to/

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=gooin/DailySync&type=Date)](https://star-history.com/#gooin/DailySync&Date)

## Buy Me a Coffee

如果你觉得我的工作帮到了你，可赠予我一杯咖啡，感谢~
![wechat](./assets/wechat.jpg)

### 支持者记录

|     姓名     | 金额(￥) |
|:----------:|:-----:|
| Monk****IN |  50   |
|   Cl**N    |  50   |
|   無敵**十    |  50   |
|     *弟     |  50   |
|   S**en    |  66   |
|    C**2    | 8.88  |
|    星**烂    |  30   |
|    李*牛     |  15   |
|     狼*     | 16.18 |
|     刘      |  50   |
|    A*w     |  50   |
|     *昱     |  20   |
|     *仔     | 8.88  |
|     *飞     |  50   |
|    ZKY     |  50   |
|    L**n    |  40   |
|    微**移    |  25   |
|     *宫     |  100  |
|    无**空    |  50   |
|    解*n     |  30   |
|     *亮     |  15   |
|    lr*s    |  50   |
|    S*e     |  8.8  |
