---
# title: "MC整合包.风林火山"
tags:
  - "风林火山"
  - "整合包"
html:
  toc: true
toc:
  depth_from: 1
  depth_to: 6
  ordered: false
print_background: true
---


# 风林火山

## 1. 简介

- 风林火山是一个适用于 `MC 1.21.1` `neoforge 21.1.197` 的整合包
- 该包:
  - 选择性添加了一些渲染和其它优化模组, 以期达到良好的性能
  - 添加了常见的科技模组, 如机械动力, MEK 等, 以及其实用附属
  - 添加了一些自定义配方
  - 对一些常见 TACZ 枪包的参数进行了平衡
  - 添加了 InControl 生成规则
  - 修改了键位预设, 尽可能降低按键冲突

## 2. 世界种子

- `-8759369869020725628`

## 3. 快捷键速览

|        功能         |       按键        |      分类       |                                      备注                                      |
| :-----------------: | :---------------: | :-------------: | :----------------------------------------------------------------------------: |
|        背包         |         E         |      基本       |                                                                                |
|        丢出         |         Q         |      基本       |                                                                                |
|      副手交换       |         F         |      基本       |                                                                                |
|  潜行 / 蹲 / 下降   |         C         |      基本       |                                                                                |
|        疾跑         |      L_SHIFT      |      基本       |                                                                                |
|       聊天栏        |    ` (反引号)     |      基本       |                          也可在创造背包快速聚焦搜索栏                          |
|      输入命令       |         /         |      基本       |                                                                                |
|    显示玩家列表     |        TAB        |      基本       |                                 小地图功能覆盖                                 |
|    HUD 显示切换     |        F1         |      基本       |                                                                                |
|        截图         |        F2         |      基本       |                                                                                |
|      切换视角       |        F5         |      基本       |                                                                                |
|      全屏切换       |        F11        |      基本       |                                                                                |
|                     |                   |                 |                                                                                |
|        进度         |       NP_*        |      杂项       |                                                                                |
|                     |                   |                 |                                                                                |
|    指向方块信息     |         I         |      未知       |                                                                                |
|   临时显示聊天栏    |         P         |      未知       |                                                                                |
|                     |                   |                 |                                                                                |
|      交换两行       |     L_ALR + R     |     快捷栏      |                                                                                |
|      循环单列       |   L_ALR + 滚轮    |     快捷栏      |                                                                                |
|   额外快捷栏开关    |         =         |     快捷栏      |                                                                                |
|                     |                   |                 |                                                                                |
|     打开饰品栏      |     CTRL + E      |      饰品       |                                  Accessories                                   |
|     打开饰品栏      |     SHIFT + E     |      饰品       |                                      天境                                      |
|     打开饰品栏      |      ALT + E      |      饰品       |                                     Curios                                     |
|     打开饰品栏      |     CTRL + =      |      饰品       |                                      汇流                                      |
|                     |                   |                 |                                                                                |
|  点击穿透功能开关   |        F9         |    穿牌开箱     |                                                                                |
|                     |                   |                 |                                                                                |
|      放大画面       |     BACKSPACE     |    Modern UI    |                                                                                |
|      打开设置       |     CTRL + K      |    Modern UI    |                                                                                |
|                     |                   |                 |                                                                                |
|   现代化修复设置    |       NP_9        |   现代化修复    |                                                                                |
|                     |                   |                 |                                                                                |
|      重载光影       |     SHIFT + K     |      IRIS       |                                                                                |
|    切换光影开关     |      ALT + K      |      IRIS       |                                                                                |
|                     |                   |                 |                                                                                |
|   tweakerge 配置    |       X + C       |    Tweakerge    |                                                                                |
|      相邻放置       |      L_SHIFT      |    Tweakerge    |                                                                                |
|      偏移放置       |      L_CTRL       |    Tweakerge    |                                                                                |
|      旋转放置       |       L_ALT       |    Tweakerge    |                                                                                |
|    开关灵活放置     |        F7         |    Tweakerge    |                                                                                |
|      灵魂出窍       |   R_SHIFT + F7    |    Tweakerge    |                                                                                |
|                     |                   |                 |                                                                                |
|    打开设置界面     |       K + C       |   TweakerMore   |                                                                                |
|                     |                   |                 |                                                                                |
|    minihud 配置     |       H + C       |     minihud     |                                                                                |
|      HUD 切换       |         H         |     minihud     |                                                                                |
|    光照信息开关     |    L_SHIFT + H    |     minihud     |                                                                                |
|    区块边界显示     |     L_ALT + H     |     minihud     |                                                                                |
|                     |                   |                 |                                                                                |
|   Litematica 配置   |       M + C       |   Litematica    |                                                                                |
|   Litematica 菜单   |         M         |   Litematica    |                                                                                |
|    选取设置界面     |     M + NP_*      |   Litematica    |                                                                                |
|    放置设置界面     |     M + NP_-      |   Litematica    |                                                                                |
|                     |                   |                 |                                                                                |
|      打开设置       |       Z + C       |     MaLiLib     |                                                                                |
|                     |                   |                 |                                                                                |
|      打开设置       |       R + C       |       IPN       |                                                                                |
|  设置覆盖按钮位置   |       R + G       |       IPN       |                                                                                |
|      扔出全部       |       R + M       |       IPN       |                                                                                |
| 输出物品 NBT 到聊天 |     CTRL + \      |       IPN       |                                                                                |
|      复制组件       |     CTRL + C      |       IPN       |                                                                                |
|     复制物品 ID     | CTRL + SHIFT + C  |       IPN       |                                                                                |
|                     |                   |                 |                                                                                |
|      TACZ 设置      |      ALT + T      |      TACZ       |                                                                                |
|       换弹匣        |         R         |      TACZ       |                                                                                |
|    开火模式切换     |         G         |      TACZ       |                                                                                |
|        爬行         |         X         |      TACZ       |                                                                                |
|        近战         |         V         |      TACZ       |                                                                                |
|      倍率切换       |         V         |      TACZ       |                                                                                |
|      改装界面       |     , (逗号)      |      TACZ       |                                                                                |
|      检视枪械       |     . (句号)      |      TACZ       |                                                                                |
|      持枪交互       |       ENTER       |      TACZ       |                                                                                |
|                     |                   |                 |                                                                                |
|    FTB 区块地图     |     R_ALT + M     |    FTB 区块     |                                                                                |
|      区块认领       |       左键        |    FTB 区块     |                                     认领页                                     |
|    区块取消认领     |       右键        |    FTB 区块     |                                     认领页                                     |
|    区块强制加载     |   SHIFT + 左键    |    FTB 区块     |                                     认领页                                     |
|    取消强制加载     |   SHIFT + 右键    |    FTB 区块     |                                     认领页                                     |
|    开启连锁破坏     |       L_ALT       |  FTB 连锁破坏   |                                                                                |
|  连锁破坏模式切换   |   SHIFT + 滚轮    |  FTB 连锁破坏   |                                                                                |
|     打开队伍页      |    SHIFT +  T     |    FTB 队伍     |                                                                                |
|                     |                   |                 |                                                                                |
|      打开设置       |       NP_/        |  可视性能侦测   |                                                                                |
|                     |                   |                 |                                                                                |
|      打开设置       |       NP_0        |      Jade       |                                                                                |
|     叠加层开关      | NP_. (小键盘点号) |      Jade       |                                                                                |
|      切换流体       |       NP_1        |      Jade       |                                                                                |
|      显示配方       |       NP_2        |      Jade       |                                                                                |
|      显示用途       |       NP_3        |      Jade       |                                                                                |
|                     |                   |                 |                                                                                |
|    轮盘动画选择     |        F4         |       YSM       |                                                                                |
|      模型选择       |      ALT + Y      |       YSM       |                                                                                |
|  模型渲染位置设置   |     SHIFT + Y     |       YSM       |                                                                                |
|                     |                   |                 |                                                                                |
|     快速路径点      |     ; (分号)      | XAERO mini map  |                                                                                |
|     路径点界面      |      ALT + P      | XAERO mini map  |                                                                                |
|   临时放大小地图    |        TAB        | XAERO mini map  |                                                                                |
|     小地图设置      |         [         | XAERO mini map  |                                                                                |
|     小地图放大      |       NP_+        | XAERO mini map  |                                                                                |
|     小地图缩小      |       NP_-        | XAERO mini map  |                                                                                |
|    世界地图设置     |         ]         | XAERO world map |                                                                                |
|      世界地图       |         N         | XAERO world map |                                                                                |
|     新建路径点      |    ' (单引号)     | XAERO world map |                                                                                |
|                     |                   |                 |                                                                                |
|      打开背包       |         B         |    精妙背包     |                                                                                |
|                     |                   |                 |                                                                                |
|      显示隐藏       |     CTRL + O      |       EMI       |                                                                                |
|      界面返回       |     BACKSPACE     |       EMI       |                     注意 ESC 直接回到背包而不是返回上一页                      |
|        配方         |         R         |       EMI       |                                                                                |
|        用途         |         U         |       EMI       |                                                                                |
|        搜索         |     CTRL + F      |       EMI       | EMI 搜索框可能和输入法冲突, 如果遇到语言切换键 (shift / ctrl) 卡住再按一下即可 |
|     清空搜索栏      | SHIFT + BACKSPACE |       EMI       |                                                                                |
|     添加到收藏      |     CTRL + A      |       EMI       |                                                                                |
|    设置默认配方     |    CTRL + 左键    |       EMI       |                                                                                |
|   查看物品配方树    |         T         |       EMI       |                    合成或配方界面生效, 背包和索引列表不生效                    |
|     查看配方树      |         C         |       EMI       |                                                                                |
|  取一个物品到光标   |    CTRL + 左键    |   EMI (作弊)    |                                                                                |
|  取一组物品到光标   |    CTRL + 右键    |   EMI (作弊)    |                                                                                |
|  删除光标处的物品   |       左键        |   EMI (作弊)    |                        左键物品索引列表任意位置即可删除                        |
|    填充单次配方     |       左键        | EMI (快捷合成)  |                              背包顶部的快捷合成栏                              |
|    填充批量配方     |       右键        | EMI (快捷合成)  |                                                                                |
|    单次合成配方     |   SHIFT + 左键    | EMI (快捷合成)  |                                                                                |
|    批量合成配方     |   SHIFT + 右键    | EMI (快捷合成)  |                                                                                |
|                     |                   |                 |                                                                                |
|  打开虚无世界页面   |        DEL        |    虚无世界     |                                                                                |
|    切换资源显示     |         O         |    虚无世界     |                                                                                |
|      激活技能       |         V         |    虚无世界     |                                                                                |
|                     |                   |                 |                                                                                |
|      开关 HUD       |        F12        |    通用机械     |                                                                                |
|                     |                   |                 |                                                                                |
|      刷新交易       |    SHIFT + F5     |    简易村民     |                                                                                |
|        拾取         |     - (减号)      |    简易村民     |                                                                                |
|                     |                   |                 |                                                                                |
|    打开超分设置     |        F6         |      超分       |                                                                                |
|                     |                   |                 |                                                                                |

- `NP_` 开头的为小键盘键位
- 如果鼠标有扩展按键并可配置, 建议添加 `ENTER` 和 `BACKSPACE` 键

## 4. 已知问题

- 汇流来世 (confluence) 的再生斧, 按住 CTRL 显示 NBT 时会导致游戏崩溃
  - 数组越界
- EMI 的搜索框聚焦时会导致按一下 ctrl 键之后 ctrl 键持续按住, 再按一下 ctrl 解决
  - 不知 shift 是否触发

## 5. 命令

- 时间和时刻停止

  ```mc
  /gamerule doDaylightCycle false
  /gamerule doDaylightCycle false

  /tick freeze
  /tick freeze
  ```

- 区块预生成

  ```chunky
  // 1000 区块
  /chunky start minecraft:overworld circle 0 0 16000 16000
  // 500 区块
  /chunky start minecraft:overworld circle 0 0 8000 8000
  ```

- 游戏运行

  ```shell
  -XX:+UseG1GC \
  -XX:MaxGCPauseMillis=200 \
  -XX:+UnlockExperimentalVMOptions \
  -XX:+UnlockDiagnosticVMOptions \
  -XX:+ExplicitGCInvokesConcurrent \
  -XX:+AlwaysPreTouch \
  -XX:G1NewSizePercent=28 \
  -XX:G1MaxNewSizePercent=50 \
  -XX:G1HeapRegionSize=16M \
  -XX:G1ReservePercent=15 \
  -XX:G1MixedGCCountTarget=3 \
  -XX:InitiatingHeapOccupancyPercent=20 \
  -XX:G1MixedGCLiveThresholdPercent=90 \
  -XX:SurvivorRatio=32 \
  -XX:G1HeapWastePercent=5 \
  -XX:MaxTenuringThreshold=1 \
  -XX:+PerfDisableSharedMem \
  -XX:G1SATBBufferEnqueueingThresholdPercent=30 \
  -XX:G1ConcMarkStepDurationMillis=5 \
  -XX:G1RSetUpdatingPauseTimePercent=0 \
  -XX:+UseNUMA \
  -XX:-DontCompileHugeMethods \
  -XX:MaxNodeLimit=240000 \
  -XX:NodeLimitFudgeFactor=8000 \
  -XX:ReservedCodeCacheSize=400M \
  -XX:NonNMethodCodeHeapSize=12M \
  -XX:ProfiledCodeHeapSize=194M \
  -XX:NonProfiledCodeHeapSize=194M \
  -XX:NmethodSweepActivity=1 \
  -XX:+UseFastUnorderedTimeStamps \
  -XX:+UseCriticalJavaThreadPriority \
  -XX:AllocatePrefetchStyle=3 \
  -XX:+AlwaysActAsServerClassMachine \
  -XX:+EagerJVMCI \
  -XX:+UseStringDeduplication \
  -XX:+UseAES \
  -XX:+UseAESIntrinsics \
  -XX:+UseFMA \
  -XX:+UseLoopPredicate \
  -XX:+RangeCheckElimination \
  -XX:+OptimizeStringConcat \
  -XX:+UseThreadPriorities \
  -XX:+OmitStackTraceInFastThrow \
  -XX:+RewriteBytecodes \
  -XX:+RewriteFrequentPairs \
  -XX:+UseFPUForSpilling \
  -XX:+UseFastStosb \
  -XX:+UseNewLongLShift \
  -XX:+UseVectorCmov \
  -XX:+UseXMMForArrayCopy \
  -XX:+UseXmmI2D \
  -XX:+UseXmmI2F \
  -XX:+UseXmmLoadAndClearUpper \
  -XX:+UseXmmRegToRegMoveAll \
  -XX:+EliminateLocks \
  -XX:+DoEscapeAnalysis \
  -XX:+AlignVector \
  -XX:+OptimizeFill \
  -XX:+EnableVectorSupport \
  -XX:+UseCharacterCompareIntrinsics \
  -XX:+UseCopySignIntrinsic \
  -XX:+UseVectorStubs \
  -XX:UseAVX=2 \
  -XX:UseSSE=4 \
  -XX:+UseFastJNIAccessors \
  -XX:+UseInlineCaches \
  -XX:+SegmentedCodeCache \
  -Djdk.nio.maxCachedBufferSize=262144 \
  -Dgraal.UsePriorityInlining=true \
  -Dgraal.Vectorization=true \
  -Dgraal.OptDuplication=true \
  -Dgraal.DetectInvertedLoopsAsCounted=true \
  \
  -Dgraal.LoopInversion=true \
  -Dgraal.VectorizeHashes=true \
  -Dgraal.EnterprisePartialUnroll=true \
  -Dgraal.VectorizeSIMD=true \
  -Dgraal.StripMineNonCountedLoops=true \
  \
  -Dgraal.SpeculativeGuardMovement=true \
  -Dgraal.TuneInlinerExploration=1 \
  -Dgraal.LoopRotation=true \
  -Dgraal.OptWriteMotion=true \
  -Dgraal.WriteableCodeCache=true \
  -Dgraal.CompilerConfiguration=enterprise \
  \
  @libraries/net/neoforged/neoforge/21.1.197/unix_args.txt "$@" nogui
  ```

- `start.sh`

  ```shell
  #!/bin/bash

  #启动变量说明，修改前务必查看
  #https://www.yuque.com/simpfun/sfe/startup
  #https://www.yuque.com/simpfox/simpdoc/default_start

  openjdk8="/usr/bin/jdk/jdk1.8.0_361/bin/java"
  openjdk11="/usr/bin/jdk/jdk-11.0.18/bin/java"
  openjdk17="/usr/bin/jdk/jdk-17.0.6/bin/java"
  openjdk19="/usr/bin/jdk/jdk-19.0.2/bin/java"
  openjdk21="/usr/bin/jdk/jdk-21.0.2/bin/java"

  # 自定义
  graalvm_jdk_21="/home/container/jdk/graalvm-jdk-21.0.8+12.1/bin/java"


  # while true; do

  maxmem=$((SERVER_MEMORY - 900))

  echo "<info> #[$(date '+%Y_%m_%d %H:%M:%S')] 准备启动服务器"
  echo "<info> #[$(date '+%Y_%m_%d %H:%M:%S')] 内存尺寸 = ${maxmem}miB"

  ${graalvm_jdk_21} \
      -XX:+UseG1GC \
      -XX:MaxGCPauseMillis=200 \
      -XX:+UnlockExperimentalVMOptions \
      -XX:+UnlockDiagnosticVMOptions \
      -XX:+ExplicitGCInvokesConcurrent \
      -XX:+AlwaysPreTouch \
      -XX:G1NewSizePercent=28 \
      -XX:G1MaxNewSizePercent=50 \
      -XX:G1HeapRegionSize=16M \
      -XX:G1ReservePercent=15 \
      -XX:G1MixedGCCountTarget=3 \
      -XX:InitiatingHeapOccupancyPercent=20 \
      -XX:G1MixedGCLiveThresholdPercent=90 \
      -XX:SurvivorRatio=32 \
      -XX:G1HeapWastePercent=5 \
      -XX:MaxTenuringThreshold=1 \
      -XX:+PerfDisableSharedMem \
      -XX:G1SATBBufferEnqueueingThresholdPercent=30 \
      -XX:G1ConcMarkStepDurationMillis=5 \
      -XX:G1RSetUpdatingPauseTimePercent=0 \
      -XX:+UseNUMA \
      -XX:-DontCompileHugeMethods \
      -XX:MaxNodeLimit=240000 \
      -XX:NodeLimitFudgeFactor=8000 \
      -XX:ReservedCodeCacheSize=400M \
      -XX:NonNMethodCodeHeapSize=12M \
      -XX:ProfiledCodeHeapSize=194M \
      -XX:NonProfiledCodeHeapSize=194M \
      -XX:NmethodSweepActivity=1 \
      -XX:+UseFastUnorderedTimeStamps \
      -XX:+UseCriticalJavaThreadPriority \
      -XX:AllocatePrefetchStyle=3 \
      -XX:+AlwaysActAsServerClassMachine \
      -XX:+EagerJVMCI \
      -XX:+UseStringDeduplication \
      -XX:+UseAES \
      -XX:+UseAESIntrinsics \
      -XX:+UseFMA \
      -XX:+UseLoopPredicate \
      -XX:+RangeCheckElimination \
      -XX:+OptimizeStringConcat \
      -XX:+UseThreadPriorities \
      -XX:+OmitStackTraceInFastThrow \
      -XX:+RewriteBytecodes \
      -XX:+RewriteFrequentPairs \
      -XX:+UseFPUForSpilling \
      -XX:+UseFastStosb \
      -XX:+UseNewLongLShift \
      -XX:+UseVectorCmov \
      -XX:+UseXMMForArrayCopy \
      -XX:+UseXmmI2D \
      -XX:+UseXmmI2F \
      -XX:+UseXmmLoadAndClearUpper \
      -XX:+UseXmmRegToRegMoveAll \
      -XX:+EliminateLocks \
      -XX:+DoEscapeAnalysis \
      -XX:+AlignVector \
      -XX:+OptimizeFill \
      -XX:+EnableVectorSupport \
      -XX:+UseCharacterCompareIntrinsics \
      -XX:+UseCopySignIntrinsic \
      -XX:+UseVectorStubs \
      -XX:UseAVX=2 \
      -XX:UseSSE=4 \
      -XX:+UseFastJNIAccessors \
      -XX:+UseInlineCaches \
      -XX:+SegmentedCodeCache \
      -Djdk.nio.maxCachedBufferSize=262144 \
      -Dgraal.UsePriorityInlining=true \
      -Dgraal.Vectorization=true \
      -Dgraal.OptDuplication=true \
      -Dgraal.DetectInvertedLoopsAsCounted=true \
      \
      -Dgraal.LoopInversion=true \
      -Dgraal.VectorizeHashes=true \
      -Dgraal.EnterprisePartialUnroll=true \
      -Dgraal.VectorizeSIMD=true \
      -Dgraal.StripMineNonCountedLoops=true \
      \
      -Dgraal.SpeculativeGuardMovement=true \
      -Dgraal.TuneInlinerExploration=1 \
      -Dgraal.LoopRotation=true \
      -Dgraal.OptWriteMotion=true \
      -Dgraal.WriteableCodeCache=true \
      -Dgraal.CompilerConfiguration=enterprise \
      \
      @libraries/net/neoforged/neoforge/21.1.197/unix_args.txt "$@" nogui


  sleep 10

  # done


  #谨慎更改启动命令，除非你知道你在做什么！
  # ${openjdk21} \
  #      -Xms1024M \
  #      -Xmx${maxmem}M \
  #      -server \
  #      -XX:+UseCompressedOops \
  #      -XX:+UseStringDeduplication \
  #      -XX:+ParallelRefProcEnabled \
  #      -XX:MaxGCPauseMillis=200 \
  #      -XX:+UnlockExperimentalVMOptions \
  #      -XX:+DisableExplicitGC \
  #      -XX:+AlwaysPreTouch \
  #      -XX:G1NewSizePercent=30 \
  #      -XX:G1MaxNewSizePercent=40 \
  #      -XX:G1HeapRegionSize=8M \
  #      -XX:G1ReservePercent=20 \
  #      -XX:G1HeapWastePercent=5 \
  #      -XX:G1MixedGCCountTarget=4 \
  #      -XX:InitiatingHeapOccupancyPercent=15 \
  #      -XX:G1MixedGCLiveThresholdPercent=90 \
  #      @libraries/net/neoforged/neoforge/21.1.197/unix_args.txt "$@" nogui

  # echo ======================================================
  # echo "服务器已关闭，如果服务器为非正常关闭可查看下方链接内的教程上传日志，并加入疑难解答群寻求帮助！疑难解答群：465468467"
  # echo "不要把报错截图发送到群内！请发送mclo.gs链接！"
  # echo "补充：现在你可以在实例的“文件”内打开logs/latest.log，并点击右下角的“AI日志分析”来让AI帮你分析报错日志了！"
  # echo "如何正确地使用mclo.gs发送报错日志/崩溃报告：https://www.simpbbs.com/threads/mclo-gs.8/"
  # echo "备用链接：https://www.wuye2004.top/archives/1"
  # echo ======================================================
  ```

## 6. 冲突表

|           | BoccHud | Jade  | Aether |  SFM  | 汇流来世 | l2library |
| :-------: | :-----: | :---: | :----: | :---: | :------: | :-------: |
|  BoccHud  |    /    |       |   X    |   X   |    X     |     X     |
|   Jade    |         |   /   |        |       |    -     |           |
|  Aether   |    X    |       |   /    |       |    X     |           |
|    SFM    |    X    |       |        |   /   |          |           |
| 汇流来世  |    X    |   -   |   X    |       |    /     |           |
| l2library |    X    |       |        |       |          |     /     |

**其它**

- "轻松建造" 与 "MaLiLib" 低版本不兼容
- BoccHud 冲突解决方法: 打开现代化 UI 设置, 关闭 "现代虚化"

## 7. 资源

- tacz 1.21.1
  - <https://pan.baidu.com/s/1i4b8fpm7SrCdnlhZq3sY6Q?pwd=tacz>




## 8. 正则

```regex
// 替换掉 forge, 应该改成 c
(?<=")forge(?=:[\w_/]+")

// 修正 NBT 结构
"item"[\s\n]*:[\s\n]*"([\w/:\.]*)"[\s\n]*,[\s\n]*"nbt"[\s\n]*:[\s\n]*\{[\s\n]*"([\w _]+[iI][dD])"[\s\n]*:[\s\n]*"([\w/:\.]*)"[\s\n]*\}
"id": "$1", "components": { "minecraft:custom_data": { "$2": "$3" } }

// 匹配衰减段
(?<="damage_adjust"[\s\n]*:[\s\n]*[[\s\n]*)(\{"distance"[\s\n]*:[\s\n]*(?:[\d\.-]+|"infinite")[\s\n]*,[\s\n]*"damage"[\s\n]*:[\s\n]*[\d\.-]+\}[\s\n]*(?:,|\])[\s\n]*)+

// 0
(?<="damage_adjust"[\s\n]*:[\s\n]*[[\s\n]*)\{"distance"[\s\n]*:[\s\n]*([\d\.-]+)[\s\n]*,[\s\n]*"damage"[\s\n]*:[\s\n]*([\d\.-]+)\}

(?<="damage_adjust"[\s\n]*:[\s\n]*[[\s\n]*(?:\{"distance"[\s\n]*:[\s\n]*(?:[\d\.-]+)[\s\n]*,[\s\n]*"damage"[\s\n]*:[\s\n]*(?:[\d\.-]+)\}[\s\n]*,[\s\n]*){1,1})\{"distance"[\s\n]*:[\s\n]*([\d\.-]+|"infinite")[\s\n]*,[\s\n]*"damage"[\s\n]*:[\s\n]*([\d\.-]+)\}


("damage_adjust"[\s\n]*:[\s\n]*[[\s\n]*(?:\{"distance"[\s\n]*:[\s\n]*(?:[\d\.-]+)[\s\n]*,[\s\n]*"damage"[\s\n]*:[\s\n]*(?:[\d\.-]+)\}[\s\n]*,[\s\n]*){1}\{"distance"[\s\n]*:[\s\n]*)([\d\.-]+|"infinite")([\s\n]*,[\s\n]*"damage"[\s\n]*:[\s\n]*([\d\.-]+)\})


("extra_damage"[\s\n]*:[\s\n]*\{[\s\n]*"armor_ignore"[\s\n]*:[\s\n]*)([\d\.-]+)


("extra_damage"[\s\n]*:[\s\n]*\{[:\-,"\.\w\s\n]*"head_shot_multiplier"[\s\n]*:[\s\n]*)([\d\.-]+)



(?<=\w+)

```



