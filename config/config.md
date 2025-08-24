# config

## 8. 服务器配置文件更改

- `biomeswevegone\world_generation.json5`

  ```json5
  {
    // Which biomes are enabled, if disabled the biome will default to its vanilla counterpart for the given region
    "enabled_biomes": {
      "biomeswevegone:zelkova_forest": true,
      "biomeswevegone:temperate_grove": true,
      "biomeswevegone:weeping_witch_forest": true,
      "biomeswevegone:sakura_grove": true,
      "biomeswevegone:eroded_borealis": false,
      "biomeswevegone:white_mangrove_marshes": true,
      "biomeswevegone:jacaranda_jungle": true,
      "biomeswevegone:dacite_ridges": true,
      "biomeswevegone:crimson_tundra": true,
      "biomeswevegone:firecracker_chaparral": true,
      "biomeswevegone:allium_shrubland": true,
      "biomeswevegone:forgotten_forest": true,
      "biomeswevegone:frosted_coniferous_forest": true,
      "biomeswevegone:basalt_barrera": true,
      "biomeswevegone:amaranth_grassland": true,
      "biomeswevegone:black_forest": true,
      "biomeswevegone:lush_stacks": true,
      "biomeswevegone:rugged_badlands": true,
      "biomeswevegone:mojave_desert": true,
      "biomeswevegone:aspen_boreal": true,
      "biomeswevegone:shattered_glacier": true,
      "biomeswevegone:redwood_thicket": true,
      "biomeswevegone:pumpkin_valley": true,
      "biomeswevegone:overgrowth_woodlands": true,
      "biomeswevegone:bayou": true,
      "biomeswevegone:prairie": true,
      "biomeswevegone:crag_gardens": true,
      "biomeswevegone:coconino_meadow": true,
      "biomeswevegone:fragment_jungle": true,
      "biomeswevegone:dacite_shore": true,
      "biomeswevegone:ebony_woods": true,
      "biomeswevegone:canadian_shield": true,
      "biomeswevegone:enchanted_tangle": true,
      "biomeswevegone:tropical_rainforest": true,
      "biomeswevegone:pale_bog": true,
      "biomeswevegone:red_rock_peaks": true,
      "biomeswevegone:atacama_outback": true,
      "biomeswevegone:araucaria_savanna": true,
      "biomeswevegone:rose_fields": true,
      "biomeswevegone:skyrise_vale": true,
      // ------------------------------------------------------------ 修改
      "biomeswevegone:dead_sea": false,
      "biomeswevegone:cypress_swamplands": true,
      "biomeswevegone:red_rock_valley": true,
      "biomeswevegone:ironwood_gour": true,
      "biomeswevegone:cika_woods": true,
      "biomeswevegone:howling_peaks": true,
      "biomeswevegone:frosted_taiga": true,
      "biomeswevegone:windswept_desert": true,
      "biomeswevegone:cypress_wetlands": true,
      "biomeswevegone:baobab_savanna": true,
      "biomeswevegone:sierra_badlands": true,
      "biomeswevegone:maple_taiga": true,
      "biomeswevegone:orchard": true,
      "biomeswevegone:coniferous_forest": true,
      "biomeswevegone:rainbow_beach": true,
    },
    // How much each BWG region weighs. This weight applies to all 3 BWG Regions
    // ------------------------------------------------------------ 修改
    "region_weight": 5,
    // Whether to add bwg flowers and features to Vanilla Biomes (Config Option for Fabric Only)
    "vanilla_additions": true,
    // BWG Features that we add to Vanilla Biomes
    "enabled_vanilla_additions": {
      "biomeswevegone:palm_trees": true,
      "biomeswevegone:vanilla/flower_warm": true,
      "biomeswevegone:vanilla/flower_plains": true,
      "biomeswevegone:vanilla/forest_flowers": true,
      "biomeswevegone:vanilla/flower_default": true,
    },
  }
  ```

- `incontrol\phases.json`

  ```json
  [
      {
          // 阶段名称, 全局唯一
          // spawner.json / spawn.json 里用 "phase": "xxx" 引用
          "name": "phase__monster_wave__0",
          /* 阶段激活条件（下面所有条件都满足才算激活） */
          "conditions": {
              // (注意从 0 开始, 即第一天序号为 0, {0, 1, 2, 3, 4,...})
              // 如果这里写 n, 意味着经过 n 天后生效,
              // 而非第 n 天生效, 实际上第 n+1 天生效
              // 比如说写 0 是指第一天就生效, 写 1 则是第二天才生效
              "mindaycount": 10,
              // 无结束日期
              // "maxdaycount": 2147483647,
              // 注意第二个和第三个参数也是从 0 开始的 repeat(p,a,b)
              // 算法大概是判断 (计数器 - mindaycount) % p 是否在区间 [a, b] 内
              "daycount": "repeat(7,1,2)",
              // 一天中的 tick 范围: 0 = 06:00, 12000 = 18:00
              "mintime": 13000,
              "maxtime": 23000
              // 也可以用表达式, 例如只在白天: time = "range(0,12000)"
              // 可选值: {"rain", "thunder"}
              // "weather": "rain",
              // 季节 (需要 Serene Seasons)
              // "winter": true,
              // "spring": true,
              // "summer": true,
              // "autumn": true
              // 自定义布尔变量 (需要 EnigmaScript)
              // state=hardmode 为 true 时阶段才激活
              // "state": "hardmode=true"
          }
      },
      {
          "name": "phase__monster_wave__1",
          "conditions": {
              "mindaycount": 10,
              // "maxdaycount": 2147483647,
              "daycount": "repeat(11,5,7)",
              "mintime": 14000,
              "maxtime": 22000
          }
      },
      {
          "name": "phase__monster_wave__2",
          "conditions": {
              "mindaycount": 20,
              // "maxdaycount": 2147483647,
              "daycount": "repeat(17,3,5)",
              "mintime": 16000,
              "maxtime": 21500
          }
      },
      {
          "name": "phase__boss__0",
          "conditions": {
              "mindaycount": 20,
              // "maxdaycount": 2147483647,
              "daycount": "repeat(7,2,4)"
              // "mintime": 0,
              // "maxtime": 23999
          }
      }
      // 自定义 EnigmaScript 状态示例: 当全局变量 count__mob_killed>20 时激活
      // {
      //     "name": "phase__monster_killed_a_lot",
      //     "conditions": {
      //         "state": "count__mob_killed>20"
      //     }
      // }
  ]
  ```

- `incontrol\spawner.json`

  ```json
  [
      {
          /* ─────────────── 必须字段 ─────────────── */
          // 指定要刷的怪物 (可以是单个或多个，也可以和 mobsfrombiome 二选一)
          "mob": [
              "minecraft:zombie", // 僵尸
              "minecraft:drowned", // 溺尸
              "minecraft:husk", // 尸壳
              "minecraft:skeleton", // 小白
              "minecraft:bogged", // 沼骸
              "minecraft:stray", // 流髑
              "minecraft:creeper" // 爬行者
          ],
          /* ─────────────── 可选: 权重系统 ─────────────── */
          // 与 mob 列表一一对应，控制每种怪物的权重(不写则权重相同)
          "weights": [
              15,
              3,
              2,
              5,
              2,
              1,
              2
          ],
          /* ─────────────── 可选: 不指定怪物，而用生物群系默认池 ─────────────── */
          // 与 mob 二选一. 可选值: monster / creature / ambient / water_creature / water_ambient / misc
          // "mobsfrombiome": "monster",
          /* ─────────────── 刷怪频率与数量 ─────────────── */
          // 每秒尝试执行该规则的概率 (0~1, 1=100%)
          "persecond": 0.5,
          // 每次尝试时，最多找多少个合法位置 (找不到就放弃)
          "attempts": 20,
          // 每次成功时，一次刷几只
          "amount": {
              "minimum": 20,
              "maximum": 30,
              // 1.18+ 专用: 生成的怪物之间的最大距离，形成“小群落”
              "groupdistance": 48
          },
          /* ─────────────── 全局阶段/数字控制 ─────────────── */
          // 只有当这些“阶段”处于激活状态时才生效(需在 phases.json 里定义)
          "phase": [
              "phase__monster_wave__0"
          ],
          // 基于自定义数字变量的条件 (需在 number 系统里定义)
          // "number": {
          //     "name": "rate__mob_killed",
          //     "expression": "rate__mob_killed=*0.9"
          // },
          /* ─────────────── 给刷出来的实体打标签 ─────────────── */
          "addscoreboardtags": [
              "phase__monster_wave__0"
          ],
          /* ─────────────── 刷怪条件区块 (只能出现下列键) ─────────────── */
          "conditions": {
              /* 维度(必填) */
              "dimension": "minecraft:overworld",
              /* ── 日期/天数限制 ── */
              //   "mindaycount": 10,
              //   "maxdaycount": 100,
              /* ── 与玩家的距离限制 ── */
              "mindist": 16,
              "maxdist": 48,
              "minverticaldist": 0,
              "maxverticaldist": 32,
              /* ── 高度限制 ── */
              //   "minheight": -64,
              //   "maxheight": 320,
              /* ── 群系相关 ── */
              //   "biome": ["minecraft:plains", "minecraft:desert"],
              /* ── 结构相关 ── */
              //   "structure": ["minecraft:village", "minecraft:mineshaft"],
              //   "structuretags": ["minecraft:is_village"],
              //   "hasstructure": true,
              /* ── Lost Cities(若装了该模组) ── */
              //   "incity": true,
              //   "inbuilding": true,
              //   "inmultibuilding": false,
              //   "building": ["lostcities:building1"],
              //   "multibuilding": ["lostcities:multibuilding1"],
              //   "instreet": false,
              //   "insphere": false,
              /* ── 刷怪环境 ── */
              "inliquid": false, // 允许在任意液体
              "inwater": false, // 允许在水中
              "inlava": false, // 允许在岩浆
              "inair": false, // 允许在空中
              "validspawn": false, // 强制做额外合法性检测(方块、光照等)
              "sturdy": false, // 必须站在完整方块(非半砖、地毯等)
              /* ── 全局数量上限(选填) ── */
              "maxthis": 200, // 该规则刷出的这种怪最多同时存在多少
              "maxtotal": 500, // 所有怪总和上限
              //   "maxpeaceful": 50,      // 被动生物上限
              //   "maxhostile": 200,      // 敌对生物上限
              //   "maxneutral": 30,       // 中立生物上限
              //   "maxlocal": 50,         // 以刷怪点为中心的局部上限(性能开销大)
              /* ── 忽略原版限制 ── */
              "norestrictions": true, // 跳过怪物自带的亮度/方块/碰撞检测
              /* ── 复合条件(and / not)────────────────── */
              // 所有 and 内的条件必须全部满足
              "and": {
                  // "biome": "minecraft:desert",
                  // "minlight": 10,
                  /* ── 光照限制(0~15) ── */
                  "minlight": 0,
                  "maxlight": 9,
                  "minlight_full": 0,
                  "maxlight_full": 9
                  // "seesky": false, // 必须能看到天空
                  // "cave": false, // 必须在洞穴内
                  // "biometags": [
                  //     "minecraft:is_overworld"
                  // ]
              },
              // not 内只要满足任意一条就禁止刷怪
              "not": {
                  "structuretags": [
                      "minecraft:is_village"
                  ],
                  "biometags": [
                      "minecraft:is_ocean"
                  ]
              }
          }
      },
      {
          "mob": [
              "minecraft:zombie", // 僵尸
              "minecraft:drowned", // 溺尸
              "minecraft:husk", // 尸壳
              "minecraft:skeleton", // 小白
              "minecraft:bogged", // 沼骸
              "minecraft:stray", // 流髑
              "minecraft:creeper" // 爬行者
          ],
          "weights": [
              3,
              2,
              2,
              5,
              1,
              2,
              15
          ],
          "persecond": 0.4,
          "attempts": 20,
          "amount": {
              "minimum": 20,
              "maximum": 30,
              "groupdistance": 48
          },
          "phase": [
              "phase__monster_wave__1"
          ],
          "addscoreboardtags": [
              "phase__monster_wave__1"
          ],
          "conditions": {
              "dimension": "minecraft:overworld",
              "mindist": 32,
              "maxdist": 128,
              "minverticaldist": 0,
              "maxverticaldist": 32,
              /* ── 刷怪环境 ── */
              "inliquid": false, // 允许在任意液体
              "inwater": false, // 允许在水中
              "inlava": false, // 允许在岩浆
              "inair": false, // 允许在空中
              "validspawn": false, // 强制做额外合法性检测(方块、光照等)
              "sturdy": false, // 必须站在完整方块(非半砖、地毯等)
              /* ── 全局数量上限(选填) ── */
              "maxthis": 150, // 该规则刷出的这种怪最多同时存在多少
              "maxtotal": 500, // 所有怪总和上限
              "norestrictions": true, // 跳过怪物自带的亮度/方块/碰撞检测
              "and": {
                  "minlight": 0,
                  "maxlight": 9,
                  "minlight_full": 0,
                  "maxlight_full": 9
              },
              "not": {
                  "structuretags": [
                      "minecraft:is_village"
                  ],
                  "biometags": [
                      "minecraft:is_ocean"
                  ]
              }
          }
      },
      {
          "mob": [
              "minecraft:zombie", // 僵尸
              "minecraft:drowned", // 溺尸
              "minecraft:husk", // 尸壳
              "minecraft:skeleton", // 小白
              "minecraft:bogged", // 沼骸
              "minecraft:stray", // 流髑
              "minecraft:creeper" // 爬行者
          ],
          "weights": [
              2,
              3,
              1,
              15,
              4,
              3,
              2
          ],
          "persecond": 0.4,
          "attempts": 20,
          "amount": {
              "minimum": 20,
              "maximum": 30,
              "groupdistance": 64
          },
          "phase": [
              "phase__monster_wave__2"
          ],
          "addscoreboardtags": [
              "phase__monster_wave__2"
          ],
          "conditions": {
              "dimension": "minecraft:overworld",
              "mindist": 32,
              "maxdist": 64,
              "minverticaldist": 0,
              "maxverticaldist": 32,
              /* ── 刷怪环境 ── */
              "inliquid": false, // 允许在任意液体
              "inwater": false, // 允许在水中
              "inlava": false, // 允许在岩浆
              "inair": false, // 允许在空中
              "validspawn": false, // 强制做额外合法性检测(方块、光照等)
              "sturdy": false, // 必须站在完整方块(非半砖、地毯等)
              /* ── 全局数量上限(选填) ── */
              "maxthis": 150, // 该规则刷出的这种怪最多同时存在多少
              "maxtotal": 500, // 所有怪总和上限
              "norestrictions": true, // 跳过怪物自带的亮度/方块/碰撞检测
              "and": {
                  "minlight": 0,
                  "maxlight": 9,
                  "minlight_full": 0,
                  "maxlight_full": 9
              },
              "not": {
                  "structuretags": [
                      "minecraft:is_village"
                  ],
                  "biometags": [
                      "minecraft:is_ocean"
                  ]
              }
          }
      },
      {
          "mob": [
              "born_in_chaos_v1:lord_pumpkinhead" // 南瓜领主
          ],
          // "weights": [
          //     1
          // ],
          "persecond": 0.00003,
          "attempts": 20,
          "amount": {
              "minimum": 1,
              "maximum": 3,
              "groupdistance": 64
          },
          "phase": [
              "phase__boss__0"
          ],
          "addscoreboardtags": [
              "phase__boss__0"
          ],
          "conditions": {
              "dimension": "minecraft:overworld",
              "mindist": 32,
              "maxdist": 64,
              "minverticaldist": 0,
              "maxverticaldist": 32,
              /* ── 刷怪环境 ── */
              "inliquid": false, // 允许在任意液体
              "inwater": false, // 允许在水中
              "inlava": false, // 允许在岩浆
              "inair": false, // 允许在空中
              "validspawn": false, // 强制做额外合法性检测(方块、光照等)
              "sturdy": false, // 必须站在完整方块(非半砖、地毯等)
              /* ── 全局数量上限(选填) ── */
              "maxthis": 10, // 该规则刷出的这种怪最多同时存在多少
              "maxtotal": 500, // 所有怪总和上限
              "norestrictions": true, // 跳过怪物自带的亮度/方块/碰撞检测
              "and": {
                  "minlight": 0,
                  "maxlight": 10,
                  "minlight_full": 0,
                  "maxlight_full": 10,
                  "seesky": true
              },
              "not": {
                  "structuretags": [
                      "minecraft:is_village"
                  ],
                  "biometags": [
                      "minecraft:is_ocean"
                  ]
              }
          }
      },
      {
          "mob": [
              "born_in_chaos_v1:sir_pumpkinhead" // 南瓜伯爵
          ],
          // "weights": [
          //     1
          // ],
          "persecond": 0.0005,
          "attempts": 20,
          "amount": {
              "minimum": 3,
              "maximum": 5,
              "groupdistance": 64
          },
          "phase": [
              "phase__boss__0"
          ],
          "addscoreboardtags": [
              "phase__boss__0"
          ],
          "conditions": {
              "dimension": "minecraft:overworld",
              "mindist": 32,
              "maxdist": 64,
              "minverticaldist": 0,
              "maxverticaldist": 32,
              /* ── 刷怪环境 ── */
              "inliquid": false, // 允许在任意液体
              "inwater": false, // 允许在水中
              "inlava": false, // 允许在岩浆
              "inair": false, // 允许在空中
              "validspawn": false, // 强制做额外合法性检测(方块、光照等)
              "sturdy": false, // 必须站在完整方块(非半砖、地毯等)
              /* ── 全局数量上限(选填) ── */
              "maxthis": 50, // 该规则刷出的这种怪最多同时存在多少
              "maxtotal": 500, // 所有怪总和上限
              "norestrictions": true, // 跳过怪物自带的亮度/方块/碰撞检测
              "and": {
                  "minlight": 0,
                  "maxlight": 10,
                  "minlight_full": 0,
                  "maxlight_full": 10,
                  "seesky": true
              },
              "not": {
                  "structuretags": [
                      "minecraft:is_village"
                  ],
                  "biometags": [
                      "minecraft:is_ocean"
                  ]
              }
          }
      }
  ]
  ```

- `creeper_firework-common.toml`

  ```toml
  [explosion]
    #Will creeper's active-explosion turn into firework?
    CREEPER_EXPLODE_INTO_FIREWORK = true
    
    #Will the active-explosion firework effect hurt nearby creature?
    # ------------------------------------------------------------ 修改
    CREEPER_FIREWORK_HURT_CREATURE = true
    
    #Will the active-explosion firework destroy nearby environment just like creeper normally exploding?
    CREEPER_FIREWORK_DESTROY_BLOCK = false
    
    #The probability of creeper turning into firework when actively explodes.
    # Default: 1.0
    # Range: 0.0 ~ 1.0
    CREEPER_EXPLODE_INTO_FIREWORK_PROBABILITY = 1.0

  [death_explosion]
    #Will creeper explode into firework when die?
    CREEPER_EXPLODE_INTO_FIREWORK_WHEN_DIE = false
    
    #Will the death-explosion firework destroy nearby environment just like creeper normally exploding?
    CREEPER_DEATH_FIREWORK_DESTROY_BLOCK = false
    
    #Will the death-explosion firework effect hurt nearby creature?
    CREEPER_DEATH_FIREWORK_HURT_CREATURE = false
    
    #The probability of creeper turning into firework when die.
    # Default: 1.0
    # Range: 0.0 ~ 1.0
    CREEPER_EXPLODE_INTO_FIREWORK_PROBABILITY_WHEN_DIE = 1.0
  ```

- `fluxnetworks-server.toml`

  ```toml
  [networks]
    #Maximum networks each player can have. Super admin can bypass this limit. -1 = no limit
    #Setting this to 0 will only allow super admins to create networks.
    # Default: 5
    # Range: > -1
    maximumPerPlayer = 5
    #Allows someone to be a network super admin. Otherwise, no one can access a flux device or delete a network without permission.
    enableSuperAdmin = true
    #See ops.json. If the player has permission level equal or greater to the value set here they will be able to activate Super Admin.
    #Setting this to 0 will allow anyone to active Super Admin. Single player can bypass this limit.
    #Players have permission level 3 or 4 can use commands to set others as Super Admin whether others have this permission level or not.
    # Default: 1
    # Range: 0 ~ 3
    superAdminRequiredPermission = 1

  [general]
    #Enables redstone being compressed with the bedrock and obsidian to get flux dusts.
    enableFluxRecipe = true
    #Allows flux devices to enable chunk loading.
    # ------------------------------------------------------------ 修改
    enableChunkLoading = false

  [blacklist]
    #A blacklist for blocks which flux devices shouldn't connect to, use format 'modid:registry_name'
    blockBlacklistStrings = ["actuallyadditions:block_phantom_energyface"]
    #A blacklist for items which wireless charging shouldn't charge to, use format 'modid:registry_name'
    itemBlackListStrings = [""]

  [energy]
    #The default transfer limit of a Flux Plug, Point and Controller
    # Default: 800000
    # Range: 0 ~ 9223372036854775807
    defaultLimit = 800000
    #The maximum energy storage of a Basic Flux Storage
    # Default: 2000000
    # Range: 0 ~ 9223372036854775807
    basicCapacity = 2000000
    #The default transfer limit of a Basic Flux Storage
    # Default: 20000
    # Range: 0 ~ 9223372036854775807
    basicTransfer = 20000
    #The maximum energy storage of a Herculean Flux Storage
    # Default: 16000000
    # Range: 0 ~ 9223372036854775807
    herculeanCapacity = 16000000
    #The default transfer limit of a Herculean Flux Storage
    # Default: 120000
    # Range: 0 ~ 9223372036854775807
    herculeanTransfer = 120000
    #The maximum energy storage of a Gargantuan Flux Storage
    # Default: 128000000
    # Range: 0 ~ 9223372036854775807
    gargantuanCapacity = 128000000
    #The default transfer limit of a Gargantuan Flux Storage
    # Default: 720000
    # Range: 0 ~ 9223372036854775807
    gargantuanTransfer = 720000
  ```

- `tacz-common.toml`

  ```toml
  [gun]
    #The default fire sound range (block)
    # Default: 64
    # Range: > 0
    DefaultGunFireSoundDistance = 64
    #The silencer default fire sound range (block)
    # Default: 16
    # Range: > 0
    DefaultGunSilenceSoundDistance = 16
    #The range (block) of other gun sound, reloading sound etc.
    # Default: 16
    # Range: > 0
    DefaultGunOtherSoundDistance = 16
    #Whether or not the player will consume ammo in creative mode
    CreativePlayerConsumeAmmo = true
    #Auto reload all the guns in player inventory, useful for pvp servers
    AutoReloadWhenRespawn = false

  [ammo]
    #Warning: Ammo with explosive properties can break blocks
    ExplosiveAmmoDestroysBlock = true
    #Warning: Ammo with explosive properties can set the surroundings on fire
    # ------------------------------------------------------------ 修改
    ExplosiveAmmoFire = true
    #Ammo with explosive properties can add knockback effect
    ExplosiveAmmoKnockBack = true
    #The distance at which the explosion effect can be seen
    # Default: 192
    # Range: > 0
    ExplosiveAmmoVisibleDistance = 192
    #Those blocks that the ammo can pass through
    PassThroughBlocks = []
    #Whether a ammo can break the glass
    # ------------------------------------------------------------ 修改
    DestroyGlass = false
    #Whether a ammo can ignite the block
    IgniteBlock = true
    #Whether a ammo can ignite the entity
    IgniteEntity = true
    #Global bullet speed modifier, the init speed of the bullet will be multiplied by this value, default is 2.0
    #This is to compensate the side effects introduced while fixing the shooter variable input issue
    # Default: 2.0
    # Range: 0.01 ~ 20.0
    # ------------------------------------------------------------ 修改
    GlobalBulletSpeedModifier = 1.0

  [other]
    #Deprecated: now move to .minecraft/tacz/tacz-pre.toml or <your version>/tacz/tacz-pre.toml
    #When enabled, the reload command will not overwrite the default model file under config
    DefaultPackDebug = false
    #The farthest sound distance of the target, including minecarts type
    # Default: 128
    # Range: > 0
    TargetSoundDistance = 128
    #DEV: Server hitbox offset (If the hitbox is ahead, fill in a negative number)
    # Default: 3.0
    # Range: -1.7976931348623157E308 ~ 1.7976931348623157E308
    ServerHitboxOffset = 3.0
    #Server hitbox latency fix
    ServerHitboxLatencyFix = true
    #The maximum latency (in milliseconds) for the server hitbox latency fix saved
    # Default: 1000.0
    # Range: 250.0 ~ 1.7976931348623157E308
    ServerHitboxLatencyMaxSaveMs = 1000.0
  ```

- `tacz-pre.toml`

  ```toml
  [gunpack]
    #When enabled, the mod will not try to overwrite the default pack under .minecraft/tacz
    #Since 1.0.4, the overwriting will only run when you start client or a dedicated server
    # ------------------------------------------------------------ 修改
    DefaultPackDebug = true
  ```

- `tectonic.json`

  ```json
  {
    "biomes": {
      "temperature_multiplier": 1.0,
      "temperature_offset": 0.0,
      "temperature_scale": 0.25,
      "vegetation_multiplier": 1.0,
      "vegetation_offset": 0.0,
      "vegetation_scale": 0.25
    },
    "continents": {
      // ------------------------------------------------------------ 修改
      "continents_scale": 0.30,
      "erosion_scale": 0.25,
      "flat_terrain_skew": 0.1,
      "jungle_pillars": true,
      "ocean_offset": -0.8,
      // ------------------------------------------------------------ 修改
      "ridge_scale": 0.35,
      "river_lanterns": true,
      "rolling_hills": true,
      "underground_rivers": true
    },
    "general": {
      "mod_enabled": true,
      "snow_start_offset": 128
    },
    "global_terrain": {
      "increased_height": false,
      "lava_tunnels": true,
      "ultrasmooth": false,
      "vertical_scale": 1.125
    },
    "islands": {
      "enabled": true,
      "noise_multiplier": 1.0,
      "noise_offset": 0.0,
      "noise_scale": 0.11
    },
    "minor_version": 1,
    "oceans": {
      "deep_ocean_depth": -0.45,
      "monument_offset": -30,
      "ocean_depth": -0.22,
      "remove_frozen_ocean_ice": false
    }
  }
  ```

- `ftbchunks-world.snbt`

  ```toml
  # Server-specific configuration for FTB Chunks
  # Modpack defaults should be defined in <instance>/config/ftbchunks-world.snbt
  #   (may be overwritten on modpack update)
  # Server admins may locally override this by copying into <instance>/world/serverconfig/ftbchunks-world.snbt
  #   (will NOT be overwritten on modpack update)

  {
    # Forced modes won't let players change their ally settings
    # Default: "default"
    # Valid values: "default", "forced_all", "forced_none"
    ally_mode: "default"
    
    # Disables all land protection. Useful for private servers where everyone is trusted and claims are only used for force-loading
    # Default: false
    disable_protection: false
    
    # Minimap for clients connecting to this server will be disabled
    # Default: false
    force_disable_minimap: false
    
    # If true, "Location Visibility" team settings are ignored, and all players can see each other anywhere on the map.
    # Default: false
    location_mode_override: false
    
    # Interval in ticks to send updates to clients with long-range player tracking data.
    # Lower values mean more frequent updates but more server load and network traffic; be careful with this, especially on busy servers.
    # Setting this to 0 disables long-range tracking.
    # Default: 20
    # Range: 0 ~ 2147483647
    long_range_tracker_interval: 20
    
    # Requires you to claim chunks in order to edit and interact with blocks
    # Default: false
    no_wilderness: false
    
    # Dimension ID's where the no_wilderness rule is enforced - building is only allowed in claimed chunks. If this is non-empty, it overrides the 'no_wilderness' setting.
    # Default: []
    no_wilderness_dimensions: [ ]
    
    # If true, pistons are prevented from pushing/pulling blocks across claims owned by different teams (unless the target claim has public 'edit block' permissions defined). If 'disable_protection' is set to true, this setting is ignored.
    # Default: true
    piston_protection: true
    
    # When true, standard FTB Chunk explosion protection is applied in protected chunks when the source of the explosion cannot be determined
    # (Ghast fireballs are a common case - vanilla supplies a null entity source)
    # Default: true
    protect_unknown_explosions: true
    
    # Should PvP combat be allowed in claimed chunks? Default is ALWAYS; NEVER prevents it in all claimed chunks; PER_TEAM allows teams to decide if PvP is allowed in their claims
    # Default: "always"
    # Valid values: "always", "never", "per_team"
    pvp_mode: "always"
    
    # If true, the player must have the 'ftbchunks_mapping' Game stage to be able to use the map and minimap.
    # Requires KubeJS and/or Gamestages to be installed.
    # Default: false
    require_game_stage: false
    claiming: {
      # Dimension ID's where chunks may not be claimed. Add "minecraft:the_end" to this list if you want to disable chunk claiming in The End, or "othermod:*" to disable chunk claiming in *all* dimensions added by "othermod"
      # Default: []
      claim_dimension_blacklist: [ ]
      
      # Dimension ID's where chunks may be claimed. If non-empty, chunks may be claimed *only* in these dimensions (and the dimension is not in "claim_dimension_blacklist"). Same syntax as for "claim_dimension_blacklist".
      # Default: []
      claim_dimension_whitelist: [ ]
      
      # Hard limit for the number of chunks a team can claim, regardless of how many members. Default of 0 means no hard limit.
      # Default: 0
      # Range: 0 ~ 2147483647
      hard_team_claim_limit: 0
      
      # Max claimed chunks.
      # You can override this with FTB Ranks 'ftbchunks.max_claimed' permission
      # Default: 500
      # Range: -∞ ~ +∞
      max_claimed_chunks: 500
      
      # Maximum time (in real-world days) where if no player in a team logs in, the team automatically loses their claims.
      # Prevents chunks being claimed indefinitely by teams who no longer play.
      # Default of 0 means no automatic loss of claims.
      # Default: 0.0
      # Range: 0.0 ~ 3650.0
      max_idle_days_before_unclaim: 0.0d
      
      # Method by which party claim & force-load limits are calculated.
      # LARGEST: use the limits of the member with the largest limits
      # SUM: add up all the members' limits
      # OWNER: use the party owner's limits only
      # AVERAGE: use the average of all members' limits.
      # Default: "largest"
      # Valid values: "largest", "owner", "sum", "average"
      party_limit_mode: "largest"
    }
    dev: {
      # Enable dev commands
      # Default: false
      commands: false
    }
    fake_players: {
      # Override to disable/enable fake players like miners and auto-clickers globally.
      # Default will check this setting for each team
      # Default: "check"
      # Valid values: "check", "deny", "allow"
      fake_players: "check"
      
      # Maximum time in days to keep logs of prevented fakeplayer access to a team's claims.
      # Default: 7
      # Range: 1 ~ 2147483647
      max_prevented_log_age: 7
    }
    force_loading: {
      # Control how force-loaded chunks work.
      # NEVER: only allow chunk force-loading if the owning team has at least one online player.
      # ALWAYS: always allow force-loading, even if no players are online.
      # DEFAULT: allow force-loading IF the team has at least one player with the 'ftbchunks.chunk_load_offline' FTB Ranks permission.
      # Default: "default"
      # Valid values: "default", "always", "never"
      force_load_mode: "default"
      
      # Hard limit for the number of chunks a team can force-load, regardless of how many members. Default of 0 means no hard limit.
      # Default: 0
      # Range: 0 ~ 2147483647
      hard_team_force_limit: 0
      
      # Max force loaded chunks.
      # You can override this with FTB Ranks 'ftbchunks.max_force_loaded' permission
      # Default: 25
      # Range: -∞ ~ +∞
      # ------------------------------------------------------------ 修改
      max_force_loaded_chunks: 500
      
      # Maximum time (in real-world days) where if no player in a team logs in, any forceloaded chunks owned by the team are no longer forceloaded.
      # Prevents chunks being forceloaded indefinitely by teams who no longer play.
      # Default of 0 means no automatic loss of forceloading.
      # Default: 0.0
      # Range: 0.0 ~ 3650.0
      max_idle_days_before_unforce: 0.0d
    }
    team_prop_defaults: {
      # Default explosion protection for claimed chunks
      # Default: false
      def_allow_explosions: false
      
      # Default mode for block breaking and placing in claimed chunks (NeoForge only)
      # Default: "allies"
      # Valid values: "allies", "private", "public"
      def_block_edit: "allies"
      
      # Default mode for block interaction, breaking and placing in claimed chunks (Fabric only)
      # Default: "allies"
      # Valid values: "allies", "private", "public"
      def_block_edit_interact: "allies"
      
      # Default mode for block interaction (right-click) in claimed chunks (NeoForge only)
      # Default: "allies"
      # Valid values: "allies", "private", "public"
      def_block_interact: "allies"
      
      # Default claim visibility for claimed chunks
      # Default: "public"
      # Valid values: "allies", "private", "public"
      def_claim_visibility: "public"
      
      # Default mode for left-clicking non-living entities (armor stands, item frames...) in claimed chunks
      # Default: "allies"
      # Valid values: "allies", "private", "public"
      def_entity_attack: "allies"
      
      # Default mode for entity interaction in claimed chunks
      # Default: "allies"
      # Valid values: "allies", "private", "public"
      def_entity_interact: "allies"
      
      # Default allow fake player IDs which are the same as real permitted players
      # Default: true
      def_fake_player_ids: true
      
      # Default allow-fake-player setting for team properties
      # Default: false
      def_fake_players: false
      
      # Default mob griefing protection for claimed chunks
      # Default: false
      def_mob_griefing: false
      
      # Default named fake players who should be allowed by default
      # Default: []
      def_named_fake_players: [ ]
      
      # Default long-range player visibility on map
      # Default: "allies"
      # Valid values: "allies", "private", "public"
      def_player_visibility: "allies"
      
      # Default PvP setting in claimed chunks
      # Default: true
      def_pvp: true
    }
    waypoint_sharing: {
      # Allow players to share waypoints with their party.
      # Default: true
      waypoint_sharing_party: true
      
      # Allow players to share waypoints with other players.
      # Default: true
      waypoint_sharing_players: true
      
      # Allow players to share waypoints with the entire server.
      # Default: true
      waypoint_sharing_server: true
    }
  }
  ```

- `constructionstick-server.toml`

  ```toml
  [wooden_stick]
    #Stick durability
    # Default: 59
    # Range: > 1
    # ------------------------------------------------------------ 修改
    durability = 64
    # Default: 5000
    # Range: > 1
    batteryStorage = 5000
    #Battery power storage
    # Default: 10
    # Range: > 1
    batteryUsage = 10
    #Battery power usage per block
    # Default: 3
    # Range: > 1
    # ------------------------------------------------------------ 修改
    limit = 8
    #Max placement distance with angel upgrade (0 to disable angel upgrade)
    # Default: 1
    # Range: > 0
    angel = 1
    #Stick destruction block limit (0 to disable destruction upgrade)
    # Default: 1
    # Range: > 0
    destruction = 1
    #Allow stick upgrading by putting the stick together with a stick upgrade in a smithing table.
    upgradeable = true

  [copper_stick]
    #Stick durability
    # Default: 131
    # Range: > 1
    # ------------------------------------------------------------ 修改
    durability = 256
    # Default: 10000
    # Range: > 1
    batteryStorage = 10000
    #Battery power storage
    # Default: 10
    # Range: > 1
    batteryUsage = 10
    #Battery power usage per block
    # Default: 9
    # Range: > 1
    # ------------------------------------------------------------ 修改
    limit = 32
    #Max placement distance with angel upgrade (0 to disable angel upgrade)
    # Default: 2
    # Range: > 0
    angel = 2
    #Stick destruction block limit (0 to disable destruction upgrade)
    # Default: 3
    # Range: > 0
    destruction = 3
    #Allow stick upgrading by putting the stick together with a stick upgrade in a smithing table.
    upgradeable = true

  [iron_stick]
    #Stick durability
    # Default: 250
    # Range: > 1
    # ------------------------------------------------------------ 修改
    durability = 1024
    # Default: 25000
    # Range: > 1
    batteryStorage = 25000
    #Battery power storage
    # Default: 10
    # Range: > 1
    batteryUsage = 10
    #Battery power usage per block
    # Default: 27
    # Range: > 1
    # ------------------------------------------------------------ 修改
    limit = 128
    #Max placement distance with angel upgrade (0 to disable angel upgrade)
    # Default: 4
    # Range: > 0
    angel = 4
    #Stick destruction block limit (0 to disable destruction upgrade)
    # Default: 9
    # Range: > 0
    destruction = 9
    #Allow stick upgrading by putting the stick together with a stick upgrade in a smithing table.
    upgradeable = true

  [diamond_stick]
    #Stick durability
    # Default: 1561
    # Range: > 1
    # ------------------------------------------------------------ 修改
    durability = 4096
    # Default: 100000
    # Range: > 1
    batteryStorage = 100000
    #Battery power storage
    # Default: 10
    # Range: > 1
    batteryUsage = 10
    #Battery power usage per block
    # Default: 128
    # Range: > 1
    # ------------------------------------------------------------ 修改
    limit = 512
    #Max placement distance with angel upgrade (0 to disable angel upgrade)
    # Default: 8
    # Range: > 0
    angel = 8
    #Stick destruction block limit (0 to disable destruction upgrade)
    # Default: 25
    # Range: > 0
    destruction = 25
    #Allow stick upgrading by putting the stick together with a stick upgrade in a smithing table.
    upgradeable = true

  [netherite_stick]
    #Stick durability
    # Default: 2031
    # Range: > 1
    # ------------------------------------------------------------ 修改
    durability = 16384
    # Default: 200000
    # Range: > 1
    batteryStorage = 200000
    #Battery power storage
    # Default: 10
    # Range: > 1
    batteryUsage = 10
    #Battery power usage per block
    # Default: 1024
    # Range: > 1
    # ------------------------------------------------------------ 修改
    limit = 2048
    #Max placement distance with angel upgrade (0 to disable angel upgrade)
    # Default: 16
    # Range: > 0
    angel = 16
    #Stick destruction block limit (0 to disable destruction upgrade)
    # Default: 81
    # Range: > 0
    destruction = 81
    #Allow stick upgrading by putting the stick together with a stick upgrade in a smithing table.
    upgradeable = true

  [misc]
    #Maximum placement range (0: unlimited). Affects all sticks and is meant for lag prevention, not game balancing.
    # Default: 100
    # Range: > 0
    MaxRange = 100
    #Number of operations that can be undone
    # Default: 3
    # Range: > 0
    UndoHistory = 3
    #Place blocks below you while falling > 10 blocks with angel upgrade (Can be used to save you from drops/the void)
    AngelFalling = false
    #Blocks to treat equally when in Similar mode. Enter block IDs separated by ;
    SimilarBlocks = ["minecraft:dirt;minecraft:grass_block;minecraft:coarse_dirt;minecraft:podzol;minecraft:mycelium;minecraft:farmland;minecraft:dirt_path;minecraft:rooted_dirt"]

  [blockentity]
    #White/Blacklist for Block Entities. Allow/Prevent blocks with BEs from being placed by stick.
    #You can either add block ids like minecraft:chest or mod ids like minecraft
    BEList = ["chiselsandbits", "mekanism", "waystones"]
    #If set to TRUE, treat BEList as a whitelist, otherwise blacklist
    BEWhitelist = false
  ```

- ~~`moveslikemafuyu_config.toml`~~ (废弃)

  ```toml
  [slide_setting]
    enable_slide = true
    enable_dap = true
    enable_slide_repeat = true
    enable_slide_knock = true

  [climb_setting]
    enable_climb = true
    enable_climb_jump = true
    enable_falling_rescue = true

  [swimming_setting]
    enable_shallow_swimming = true
    enable_swimming_boost = true
    enable_free_style = true
    enable_swimming_push = true

  [craw_setting]
    enable_craw = true
    enable_craw_slide = true
    enable_leap = true
    enable_jump_cancel_crawl = false

  [attribute_setting]
    # Default: 25
    # Range: > 0
    slide_duration = 25
    # Default: 2
    # Range: > 0
    # ------------------------------------------------------------ 修改
    slide_air_duration = 30
    # Default: 2
    # Range: > 0
    dap_times = 2
    # Default: 60
    # Range: > 0
    # ------------------------------------------------------------ 修改
    slide_cooldown = 20
    # Default: 60
    # Range: > 0
    # ------------------------------------------------------------ 修改
    climb_jump_cooldown = 20
    # Default: 60
    # Range: > 0
    # ------------------------------------------------------------ 修改
    swimming_boost_cooldown = 20
    # Default: 30
    # Range: 0 ~ 300
    swimming_boost_air_cost = 30
  ```






