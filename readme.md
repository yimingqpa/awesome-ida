# ida


跟IDA Pro有关的资源收集。当前包括的工具个数450左右，并根据功能进行了粗糙的分类。部分工具添加了中文描述。


# 目录
- [工具](#f11ab1ff46aa300cc3e86528b8a98ad7)
    - [未分类](#c39a6d8598dde6abfeef43faf931beb5)
    - [结构体&&类的检测&&创建&&恢复](#fb4f0c061a72fc38656691746e7c45ce)
        - [未分类](#fa5ede9a4f58d4efd98585d3158be4fb)
        - [C++类&&虚表](#4900b1626f10791748b20630af6d6123)
    - [收集](#a7dac37cd93b8bb42c7d6aedccb751b3)
    - [外观&&主题](#fabf03b862a776bbd8bcc4574943a65a)
    - [固件&&嵌入式设备](#a8f5db3ab4bc7bc3d6ca772b3b9b0b1e)
    - [签名(FLIRT等)&&比较(Diff)&&匹配](#02088f4884be6c9effb0f1e9a3795e58)
        - [未分类](#cf04b98ea9da0056c055e2050da980c1)
        - [FLIRT签名](#19360afa4287236abe47166154bc1ece)
            - [FLIRT签名收集](#1c9d8dfef3c651480661f98418c49197)
            - [FLIRT签名生成](#a9a63d23d32c6c789ca4d2e146c9b6d0)
        - [Diff&&Match工具](#161e5a3437461dc8959cc923e6a18ef7)
        - [Yara](#46c9dfc585ae59fe5e6f7ddf542fb31a)
    - [IDB操作](#5e91b280aab7f242cbc37d64ddbff82f)
    - [协作逆向&&多人操作相同IDB文件](#206ca17fc949b8e0ae62731d9bb244cb)
    - [与调试器同步&&通信&&交互](#f7d311685152ac005cfce5753c006e4b)
    - [导入导出&与其他工具交互](#6fb7e41786c49cc3811305c520dfe9a1)
        - [未分类](#8ad723b704b044e664970b11ce103c09)
        - [Ghidra](#c7066b0c388cd447e980bf0eb38f39ab)
        - [BinNavi](#11139e7d6db4c1cef22718868f29fe12)
        - [BinaryNinja](#d1ff64bee76f6749aef6100d72bfbe3a)
        - [Radare2](#21ed198ae5a974877d7a635a4b039ae3)
        - [Frida](#a1cf7f7f849b4ca2101bd31449c2a0fd)
        - [IntelPin](#dd0332da5a1482df414658250e6357f8)
    - [针对特定分析目标](#004c199e1dbf71769fbafcd8e58d1ead)
        - [未分类](#5578c56ca09a5804433524047840980e)
        - [GoLang](#1b17ac638aaa09852966306760fda46b)
        - [Windows驱动](#4c158ccc5aee04383755851844fdd137)
        - [PS3&&PS4](#315b1b8b41c67ae91b841fce1d4190b5)
        - [Loader&Processor](#cb59d84840e41330a7b5e275c0b81725)
        - [PDB](#f5e51763bb09d8fd47ee575a98bedca1)
        - [Flash&&SWF](#7d0681efba2cf3adaba2780330cd923a)
        - [特定样本家族](#841d605300beba45c3be131988514a03)
        - [CTF](#ad44205b2d943cfa2fa805b2643f4595)
    - [IDAPython本身](#ad68872e14f70db53e8d9519213ec039)
        - [未分类](#2299bc16945c25652e5ad4d48eae8eca)
        - [cheatsheets](#c42137cf98d6042372b1fd43c3635135)
    - [指令参考&文档](#846eebe73bef533041d74fc711cafb43)
    - [辅助脚本编写](#c08ebe5b7eec9fc96f8eff36d1d5cc7d)
        - [未分类](#45fd7cfce682c7c25b4f3fbc4c461ba2)
        - [Qt](#1a56a5b726aaa55ec5b7a5087d6c8968)
        - [控制台&&窗口界面](#1721c09501e4defed9eaa78b8d708361)
        - [插件模板](#227fbff77e3a13569ef7b007344d5d2e)
        - [其他语言](#8b19bb8cf9a5bc9e6ab045f3b4fabf6a)
    - [古老的](#dc35a2b02780cdaa8effcae2b6ce623e)
    - [调试&&动态运行&动态数据](#e3e7030efc3b4de3b5b8750b7d93e6dd)
        - [未分类](#2944dda5289f494e5e636089db0d6a6a)
        - [DBI数据](#0fbd352f703b507853c610a664f024d1)
        - [调试数据](#b31acf6c84a9506066d497af4e702bf5)
    - [反编译器&&AST](#d2166f4dac4eab7fadfe0fd06467fbc9)
    - [反混淆](#7199e8787c0de5b428f50263f965fda7)
    - [效率&&导航&&快速访问&&图形&&图像&&可视化 ](#fcf75a0881617d1f684bc8b359c684d7)
        - [其他](#c5b120e1779b928d860ad64ff8d23264)
        - [显示增强](#03fac5b3abdbd56974894a261ce4e25f)
        - [图形&&图像](#3b1dba00630ce81cba525eea8fcdae08)
        - [搜索](#8f9468e9ab26128567f4be87ead108d7)
    - [Android](#66052f824f5054aa0f70785a2389a478)
    - [Apple&&macOS&&iXxx&&Objective-C&&SWift&&Mach-O](#2adc0044b2703fb010b3bf73b1f1ea4a)
        - [未分类](#8530752bacfb388f3726555dc121cb1a)
        - [内核缓存](#82d0fa2d6934ce29794a651513934384)
        - [Mach-O](#d249a8d09a3f25d75bb7ba8b32bd9ec5)
        - [Swift](#1c698e298f6112a86c12881fbd8173c7)
    - [ELF](#e5e403123c70ddae7bd904d3a3005dbb)
    - [Microcode](#7a2977533ccdac70ee6e58a7853b756b)
    - [模拟器集成](#b38dab81610be087bd5bc7785269b8cc)
    - [新添加的](#c39dbae63d6a3302c4df8073b4d1cdc8)
    - [作为辅助&&构成其他的一环](#83de90385d03ac8ef27360bfcdc1ab48)
    - [漏洞](#1ded622dca60b67288a591351de16f8b)
        - [未分类](#385d6777d0747e79cccab0a19fa90e7e)
        - [ROP](#cf2efa7e3edb24975b92d2e26ca825d2)
    - [补丁&&Patch](#7d557bc3d677d206ef6c5a35ca8b3a14)
    - [其他](#7dfd8abad50c14cd6bdc8d8b79b6f595)
    - [函数相关](#90bf5d31a3897400ac07e15545d4be02)
        - [未分类](#347a2158bdd92b00cd3d4ba9a0be00ae)
        - [重命名&&前缀&&标记](#73813456eeb8212fd45e0ea347bec349)
        - [导航&&查看&&查找](#e4616c414c24b58626f834e1be079ebc)
        - [demangle](#cadae88b91a57345d266c68383eb05c5)
    - [污点分析&&符号执行](#34ac84853604a7741c61670f2a075d20)
    - [字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24)
    - [加密解密](#06d2caabef97cf663bd29af2b1fe270c)
- [TODO](#35f8efcff18d0449029e9d3157ac0899)
- [文章](#18c6a45392d6b383ea24b363d2f3e76b)


# <a id="f11ab1ff46aa300cc3e86528b8a98ad7"></a>工具


- 以Github开源工具为主



***


## <a id="c39a6d8598dde6abfeef43faf931beb5"></a>未分类


- [**1033**星][2mo] [Python][fireeye/flare-ida](https://github.com/fireeye/flare-ida) 多工具
    - [StackStrings](https://github.com/fireeye/flare-ida/blob/master/plugins/stackstrings_plugin.py) 自动恢复手动构造的字符串
    - [Struct Typer](https://github.com/fireeye/flare-ida/blob/master/plugins/struct_typer_plugin.py) 
    - [ApplyCalleeType](https://github.com/fireeye/flare-ida/blob/master/python/flare/apply_callee_type.py) This plugin allows you to specify or choose a function type for indirect calls as described here: [Flare-Ida-Pro-Script](https://www.fireeye.com/blog/threat-research/2015/04/flare_ida_pro_script.html)
    - [argtracker](https://github.com/fireeye/flare-ida/blob/master/python/flare/argtracker.py) 识别函数使用的静态参数
    - [idb2pat](https://github.com/fireeye/flare-ida/blob/master/python/flare/idb2pat.py) FLIRT签名生成
    - [objc2_analyzer](https://github.com/fireeye/flare-ida/blob/master/python/flare/objc2_analyzer.py) 在目标Mach-O可执行文件的与Objective-C运行时相关的部分中定义的选择器引用及其实现之间创建交叉引用
    - [MSDN Annotations](https://github.com/fireeye/flare-ida/tree/master/python/flare/IDB_MSDN_Annotator) 从XML文件中提取MSDN信息，添加到IDB数据库中
    - [ironstrings](https://github.com/fireeye/flare-ida/tree/master/python/flare/ironstrings) 使用代码模拟执行（flare-emu）, 恢复构造的字符串
    - [Shellcode Hashes](https://github.com/fireeye/flare-ida/tree/master/shellcode_hashes) 生成Hash数据库
- [**729**星][5mo] [Python][devttys0/ida](https://github.com/devttys0/ida) 多工具
    - [wpsearch](https://github.com/devttys0/ida/blob/master/scripts/wpsearch.py) 查找在MIPS WPS checksum实现中常见的立即数
    - [md5hash](https://github.com/devttys0/ida/tree/master/modules/md5hash) 纯Python版的MD5 hash实现（IDA的hashlib有问题）
    - [alleycat](https://github.com/devttys0/ida/tree/master/plugins/alleycat) 查找向指定的函数内代码块的路径、查找两个或多个函数之间的路径、生成交互式调用图、可编程
    - [codatify](https://github.com/devttys0/ida/tree/master/plugins/codatify) 定义IDA自动化分析时miss的ASCII字符串、函数、代码。将data段的所有未定义字节转换为DWORD（于是IDA可识别函数和跳转表指针）
    - [fluorescence](https://github.com/devttys0/ida/tree/master/plugins/fluorescence) 高亮函数调用指令
    - [leafblower](https://github.com/devttys0/ida/tree/master/plugins/leafblower) 识别常用的POSIX函数：printf, sprintf, memcmp, strcpy等
    - [localxrefs](https://github.com/devttys0/ida/tree/master/plugins/localxrefs) 在当前函数内部查找所有对任意选择文本的引用
    - [mipslocalvars](https://github.com/devttys0/ida/tree/master/plugins/mipslocalvars) 对栈上只用于存储寄存器的变量进行命名，简化栈数据分析（MISP）
    - [mipsrop](https://github.com/devttys0/ida/tree/master/plugins/mipsrop) 在MIPS可执行代码中搜寻ROP。查找常见的ROP
    - [rizzo](https://github.com/devttys0/ida/tree/master/plugins/rizzo) 对2个或多个IDB之间的函数进行识别和重命名，基于：函数签名、对唯一字符串/常量的引用、模糊签名、调用图
- [**305**星][3w] [C][ohjeongwook/darungrim](https://github.com/ohjeongwook/darungrim) 软件补丁分析工具
    - [IDA插件](https://github.com/ohjeongwook/darungrim/tree/master/Src/IDAPlugin) 
    - [DGEngine](https://github.com/ohjeongwook/darungrim/tree/master/Src/DGEngine) 
- [**269**星][2mo] [Python][jpcertcc/aa-tools](https://github.com/jpcertcc/aa-tools) 多脚本（还有的没列出在子工具）
    - [apt17scan.py](https://github.com/jpcertcc/aa-tools/blob/master/apt17scan.py) Volatility插件, 检测APT17相关的恶意代码并提取配置
    - [emdivi_postdata_decoder](https://github.com/jpcertcc/aa-tools/blob/master/emdivi_postdata_decoder.py) 解码Emdivi post的数据
    - [emdivi_string_decryptor](https://github.com/jpcertcc/aa-tools/blob/master/emdivi_string_decryptor.py) IDAPython脚本, 解密Emdivi内的字符串
- [**110**星][1y] [Python][vallejocc/reverse-engineering-arsenal](https://github.com/vallejocc/Reverse-Engineering-Arsenal) 逆向脚本收集
    - [WinDbg](https://github.com/vallejocc/Reverse-Engineering-Arsenal/blob/master/WinDbg) Windbg脚本收集
    - [IDA-set_symbols_for_addresses](https://github.com/vallejocc/Reverse-Engineering-Arsenal/blob/master/IDA/set_symbols_for_addresses.py) 遍历所有区段查找与指定的（地址，符号）匹配的DWORD地址，并将对应地址的值命名
    - [IDA-stack_strings_deobfuscator_1](https://github.com/vallejocc/Reverse-Engineering-Arsenal/blob/master/IDA/stack_strings_deobfuscator_1.py) 反混淆栈字符串
- [**79**星][2mo] [Python][takahiroharuyama/ida_haru](https://github.com/takahiroharuyama/ida_haru) 多工具
    - [bindiff](https://github.com/takahiroharuyama/ida_haru/blob/master/bindiff/README.org) 使用BinDiff对多个二进制文件进行对比，可多达100个
    - [eset_crackme](https://github.com/takahiroharuyama/ida_haru/blob/master/eset_crackme/README.org) ESET CrackMe driver VM loader/processor
    - [fn_fuzzy](https://github.com/takahiroharuyama/ida_haru/blob/master/fn_fuzzy/README.org) 快速二进制文件对比
    - [stackstring_static](https://github.com/takahiroharuyama/ida_haru/blob/master/stackstring_static/README.org) 静态恢复栈上的字符串
- [**73**星][9mo] [Python][secrary/ida-scripts](https://github.com/secrary/ida-scripts) 多脚本
    - [dumpDyn](https://github.com/secrary/ida-scripts/blob/master/dumpDyn/README.md) 保存动态分配并执行的代码的相关信息：注释、名称、断点、函数等，之后此代码在不同基址执行时使保存内容依然可用
    - [idenLib](https://github.com/secrary/ida-scripts/blob/master/idenLib/README.md) 库函数识别
    - [IOCTL_decode](https://github.com/secrary/ida-scripts/blob/master/IOCTL_decode.py) Windows驱动的IO控制码
    - [XORCheck](https://github.com/secrary/ida-scripts/blob/master/XORCheck.py) 
- [**60**星][2y] [Python][tmr232/idabuddy](https://github.com/tmr232/idabuddy) 逆向滴好盆友??
- [**59**星][2y] [C++][alexhude/loadprocconfig](https://github.com/alexhude/loadprocconfig) 加载处理器配置文件
- [**57**星][4w] [Python][williballenthin/idawilli](https://github.com/williballenthin/idawilli) IDA Pro 资源、脚本和配置文件等
    - [hint_calls](https://github.com/williballenthin/idawilli/blob/master/plugins/hint_calls/readme.md) 以Hint的形式战士函数引用的call和字符串
    - [dynamic_hints](https://github.com/williballenthin/idawilli/blob/master/plugins/dynamic_hints/readme.md) 演示如何为动态数据提供自定义hint的示例插件
    - [add_segment](https://github.com/williballenthin/idawilli/tree/master/scripts/add_segment) 将已存在文件的内容添加为新的segment
    - [color](https://github.com/williballenthin/idawilli/tree/master/scripts/color) 对指令进行着色
    - [find_ptrs](https://github.com/williballenthin/idawilli/tree/master/scripts/find_ptrs) 扫描.text区段查找可能为指针的值,并进行标记
    - [yara_fn](https://github.com/williballenthin/idawilli/tree/master/scripts/yara_fn) 创建yara规则，匹配当前函数的basic block
- [**54**星][1y] [Python][zardus/idalink](https://github.com/zardus/idalink) 使用IDA API时保证不卡界面. 在后台启动与界面脱离IDA CLI会话, 再使用RPyC连接界面
- [**52**星][3y] [C++][sektioneins/wwcd](https://github.com/sektioneins/wwcd) Capstone powered IDA view
- [**51**星][2y] [Python][cseagle/ida_clemency](https://github.com/cseagle/ida_clemency) IDA cLEMENCy Tools
- [**49**星][10mo] [Python][agustingianni/utilities](https://github.com/agustingianni/utilities) 多个IDAPython脚本
- [**47**星][3y] [Python][jjo-sec/idataco](https://github.com/jjo-sec/idataco) 多功能
- [**47**星][2mo] [Python][lich4/personal_script](https://github.com/lich4/personal_script) 010Editor/BurpSuite/Frida/IDA等多个工具的多个脚本
    - 重复区段: [工具/导入导出&与其他工具交互/Frida](#a1cf7f7f849b4ca2101bd31449c2a0fd) |
    - [010Editor](https://github.com/lich4/personal_script/tree/master/010Editor_Script) 010Editor的多个脚本
    - [ParamChecker](https://github.com/lich4/personal_script/tree/master/BurpSuite_Script) Burp插件
    - [Frida](https://github.com/lich4/personal_script/tree/master/Frida_script) Frida多个脚本
    - [IDA](https://github.com/lich4/personal_script/tree/master/IDA_Script) IDA多个脚本
    - [IDA-read_unicode.py](https://github.com/lich4/personal_script/blob/master/IDA_Script/read_unicode.py) IDA插件，识别程序中的中文字符
    - [IDA-add_xref_for_macho](https://github.com/lich4/personal_script/blob/master/IDA_Script/add_xref_for_macho.py) 辅助识别Objective-C成员函数的caller和callee
    - [IDA-add_info_for_androidgdb](https://github.com/lich4/personal_script/blob/master/IDA_Script/add_info_for_androidgdb.py) 使用gdbserver和IDA调试Android时，读取module列表和segment
    - [IDA-trace_instruction](https://github.com/lich4/personal_script/blob/master/IDA_Script/trace_instruction.py) 追踪指令流
    - [IDA-detect_ollvm](https://github.com/lich4/personal_script/blob/master/IDA_Script/detect_ollvm.py) 检测OLLVM，在某些情况下修复（Android/iOS）
    - [IDA-add_block_for_macho](https://github.com/lich4/personal_script/blob/master/IDA_Script/add_block_for_macho.py) 分析macho文件中的block结构
- [**45**星][7y] [Python][carlosgprado/milf](https://github.com/carlosgprado/milf) IDA瑞士军刀
    - [milf](https://github.com/carlosgprado/MILF/blob/master/milf.py) 辅助漏洞挖掘
- [**40**星][6mo] [Visual Basic][dzzie/re_plugins](https://github.com/dzzie/re_plugins) 逆向插件收集
    - [IDASrvr](https://github.com/dzzie/re_plugins/tree/master/IDASrvr) wm_copydata IPC 服务器，可从其他进程中想IDA发送命令，查询数据，控制接口显示
    - [IDA_JScript](https://github.com/dzzie/re_plugins/tree/master/IDA_JScript) 
    - [IDA_JScript_w_DukDbg](https://github.com/dzzie/re_plugins/tree/master/IDA_JScript_w_DukDbg) 
    - [IDASrvr2](https://github.com/dzzie/re_plugins/tree/master/IDASrvr2) 
    - [IdaUdpBridge](https://github.com/dzzie/re_plugins/tree/master/IdaUdpBridge) 
    - [IdaVbScript](https://github.com/dzzie/re_plugins/tree/master/IdaVbScript) 
    - [OllySrvr](https://github.com/dzzie/re_plugins/tree/master/OllySrvr) 
    - [Olly_hittrace](https://github.com/dzzie/re_plugins/tree/master/Olly_hittrace) 
    - [Olly_module_bpx](https://github.com/dzzie/re_plugins/tree/master/Olly_module_bpx) 
    - [Olly_vbscript](https://github.com/dzzie/re_plugins/tree/master/Olly_vbscript) 
    - [PyIDAServer](https://github.com/dzzie/re_plugins/tree/master/PyIDAServer) 
    - [Wingraph32](https://github.com/dzzie/re_plugins/tree/master/Wingraph32) 
    - [rabc_gui](https://github.com/dzzie/re_plugins/tree/master/flash_tools/rabc_gui) 
    - [swfdump_gui](https://github.com/dzzie/re_plugins/tree/master/flash_tools/swfdump_gui) 
    - [gleegraph](https://github.com/dzzie/re_plugins/tree/master/gleegraph) 
    - [hidden_strings](https://github.com/dzzie/re_plugins/tree/master/misc_tools/hidden_strings) 
    - [memdump_conglomerate](https://github.com/dzzie/re_plugins/tree/master/misc_tools/memdump_conglomerate) 
    - [memdump_embedder](https://github.com/dzzie/re_plugins/tree/master/misc_tools/memdump_embedder) 
    - [rtf_hexconvert](https://github.com/dzzie/re_plugins/tree/master/misc_tools/rtf_hexconvert) 
    - [uGrapher](https://github.com/dzzie/re_plugins/tree/master/uGrapher) 
    - [wininet_hooks](https://github.com/dzzie/re_plugins/tree/master/wininet_hooks) 
- [**40**星][2y] [Python][mxmssh/idametrics](https://github.com/mxmssh/idametrics) 收集x86体系结构的二进制可执行文件的静态软件复杂性度量
- [**40**星][4y] [C++][nihilus/guid-finder](https://github.com/nihilus/guid-finder) 查找GUID/UUID
- [**38**星][2y] [Python][saelo/ida_scripts](https://github.com/saelo/ida_scripts) 多脚本
    - [kernelcache](https://github.com/saelo/ida_scripts/blob/master/kernelcache.py) 识别并重命名iOS kernelcache函数stub。ARM64 Only
    - [ssdt](https://github.com/saelo/ida_scripts/blob/master/ssdt.py) 解析Windows内核中的syscall表
- [**34**星][4y] [Python][madsc13ntist/idapython](https://github.com/madsc13ntist/idapython) IDAPython脚本收集（无文档）
- [**32**星][5y] [Python][iphelix/ida-pomidor](https://github.com/iphelix/ida-pomidor) 在长时间的逆向中保存注意力和效率
- [**28**星][4mo] [Python][enovella/re-scripts](https://github.com/enovella/re-scripts) IDA/Ghidra/Radare2脚本收集（无文档）
- [**28**星][1y] [Python][xyzz/vita-ida-physdump](https://github.com/xyzz/vita-ida-physdump) None
- [**27**星][1y] [python][daniel_plohmann/simplifire.idascope](https://bitbucket.org/daniel_plohmann/simplifire.idascope) 简化恶意代码分析
- [**26**星][5y] [Python][bastkerg/recomp](https://github.com/bastkerg/recomp) IDA recompiler（无文档）
- [**26**星][7mo] [C++][offlinej/ida-rpc](https://github.com/offlinej/ida-rpc) Discord rich presence plugin for IDA Pro 7.0
- [**25**星][3y] [Python][zyantific/continuum](https://github.com/zyantific/continuum) Plugin adding multi-binary project support to IDA Pro (WIP)
- [**23**星][9mo] [C++][trojancyborg/ida_jni_rename](https://github.com/trojancyborg/ida_jni_rename) IDA JNI调用重命名
- [**22**星][4y] [Python][onethawt/idapyscripts](https://github.com/onethawt/idapyscripts) IDAPython脚本
    - [DataXrefCounter ](https://github.com/onethawt/idapyscripts/blob/master/dataxrefcounter.py) 枚举指定区段的所有交叉引用，计算使用频率
- [**22**星][3y] [C++][patois/idaplugins](https://github.com/patois/idaplugins) Random IDA scripts, plugins, example code (some of it may be old and not working anymore)
- [**21**星][5y] [Python][nihilus/idascope](https://github.com/nihilus/idascope) 辅助恶意代码逆向（Bitbucket上的代码较新）
- [**21**星][4w] [Python][rceninja/re-scripts](https://github.com/rceninja/re-scripts) None
    - [Hyperv-Scripts](https://github.com/rceninja/re-scripts/tree/master/scripts/Hyperv-Scripts) 
    - [IA32-MSR-Decoder](https://github.com/rceninja/re-scripts/tree/master/scripts/IA32-MSR-Decoder) 查找并解码所有的MSR码
    - [IA32-VMX-Helper](https://github.com/rceninja/re-scripts/tree/master/scripts/IA32-VMX-Helper) 查找并解码所有的MSR/VMCS码
- [**20**星][1y] [Python][hyuunnn/ida_python_scripts](https://github.com/hyuunnn/ida_python_scripts) IDAPython脚本
- [**20**星][2mo] [Python][nlitsme/idascripts](https://github.com/nlitsme/idascripts) 枚举多种类型数据：Texts/NonFuncs/...
- [**20**星][2y] [C#][zoebear/radia](https://github.com/zoebear/radia) 创建一个用于可视化代码的交互式、沉浸式环境，辅助二进制文件逆向
- [**20**星][1y] [Python][hyuunnn/ida_python_scripts](https://github.com/hyuunnn/ida_python_scripts) ida python scripts
- [**20**星][2w] [Python][mephi42/ida-kallsyms](https://github.com/mephi42/ida-kallsyms) None
- [**19**星][8mo] [Python][yellowbyte/reverse-engineering-playground](https://github.com/yellowbyte/reverse-engineering-playground) 逆向脚本收集，包括：IDAPython、文件分析、文件格式分析、文件系统分析、Shellcode分析
- [**19**星][3y] [Python][ztrix/idascript](https://github.com/ztrix/idascript) Full functional idascript with stdin/stdout handled
- [**18**星][1y] [Python][a1ext/ida-embed-arch-disasm](https://github.com/a1ext/ida-embed-arch-disasm) 使IDA可在32位数据库中反汇编x64代码(WOW64) 
- [**17**星][1y] [Python][honeybadger1613/etm_displayer](https://github.com/honeybadger1613/etm_displayer) IDA Pro плагин для отображения результата Coresight ETM трассировки perf'а
- [**16**星][4y] [fabi/idacsharp](https://github.com/fabi/idacsharp) C# 'Scripts' for IDA 6.6+ based on
- [**14**星][6mo] [CMake][google/idaidle](https://github.com/google/idaidle) 如果用户将实例闲置时间过长，则会警告用户。在预定的空闲时间后，该插件首先发出警告，然后再保存当前的disassemlby数据库并关闭IDA
- [**14**星][4y] [C++][nihilus/fast_idb2sig_and_loadmap_ida_plugins](https://github.com/nihilus/fast_idb2sig_and_loadmap_ida_plugins) 2个插件
    - [LoadMap](https://github.com/nihilus/fast_idb2sig_and_loadmap_ida_plugins/tree/master/LoadMap) 
    - [idb2sig](https://github.com/nihilus/fast_idb2sig_and_loadmap_ida_plugins/blob/master/idb2sig/ReadMe.txt) 
- [**13**星][2y] [Python][cisco-talos/pdata_check](https://github.com/cisco-talos/pdata_check) 根据pdata节和运行时函数的最后一条指令识别异常运行时。
- [**13**星][1y] [Python][cxm95/ida_wrapper](https://github.com/cxm95/ida_wrapper) An IDA_Wrapper for linux, shipped with an Function Identifier. It works well with Driller on static linked binaries.
- [**12**星][1y] [Assembly][gabrielravier/cave-story-decompilation](https://github.com/gabrielravier/cave-story-decompilation) 使用IDA反编译的游戏洞窟物語（Cave Story）
- [**12**星][11mo] [C++][nihilus/graphslick](https://github.com/nihilus/graphslick) IDA Plugin - GraphSlick
- [**11**星][2y] [Python][0xddaa/iddaa](https://github.com/0xddaa/iddaa) idapython scripts
- [**11**星][5y] [Python][dshikashio/idarest](https://github.com/dshikashio/idarest) Expose some basic IDA Pro interactions through a REST API for JSONP
- [**11**星][8mo] [C++][ecx86/ida7-supportlib](https://github.com/ecx86/ida7-supportlib) IDA-SupportLib library by sirmabus, ported to IDA 7
- [**10**星][4y] [C++][revel8n/spu3dbg](https://github.com/revel8n/spu3dbg) 调试anergistic SPU emulator
- [**9**星][4y] [Python][nfarrar/ida-colorschemes](https://github.com/nfarrar/ida-colorschemes) A .clr colorscheme generator for IDA Pro 6.4+.
- [**9**星][5y] [Ruby][rogwfu/plympton](https://github.com/rogwfu/plympton) Library to work with yaml exported IDA Pro information and run statistics
- [**8**星][5y] [python][daniel_plohmann/idapatchwork](https://bitbucket.org/daniel_plohmann/idapatchwork) None
- [**8**星][2y] [C++][ecx86/ida7-segmentselect](https://github.com/ecx86/ida7-segmentselect) IDA-SegmentSelect library by sirmabus, ported to IDA 7
- [**8**星][1y] [Python][lanhikari22/gba-ida-pseudo-terminal](https://github.com/lanhikari22/gba-ida-pseudo-terminal) IDAPython tools to aid with analysis, disassembly and data extraction using IDA python commands, tailored for the GBA architecture at some parts
- [**8**星][3d] [C++][nlitsme/idcinternals](https://github.com/nlitsme/idcinternals) 研究IDC脚本的内部表现形式
- [**8**星][3y] [Python][pwnslinger/ibt](https://github.com/pwnslinger/ibt) IDA Pro Back Tracer - Initial project toward automatic customized protocols structure extraction
- [**8**星][2y] [C++][shazar14/idadump](https://github.com/shazar14/idadump) An IDA Pro script to verify binaries found in a sample and write them to disk
- [**7**星][2y] [Python][swackhamer/ida_scripts](https://github.com/swackhamer/ida_scripts) IDAPython脚本（无文档）
- [**7**星][8mo] [Python][techbliss/ida_pro_http_ip_geolocator](https://github.com/techbliss/ida_pro_http_ip_geolocator) ida_pro_http_ip_geolocator：IDA 插件，查找网址并解析为 ip，通过Google 地图查看
- [**7**星][5y] [Python][techbliss/processor-changer](https://github.com/techbliss/processor-changer) 修改处理器（需重新打开IDA）
- [**7**星][1y] [C++][tenable/mida](https://github.com/tenable/mida) 提取RPC接口，重新创建关联的IDL文件
- [**6**星][2y] [CMake][elemecca/cmake-ida](https://github.com/elemecca/cmake-ida) 使用CMake构建IDA Pro模块
- [**6**星][2y] [Python][fireundubh/ida7-alleycat](https://github.com/fireundubh/ida7-alleycat) Alleycat plugin by devttys0, ported to IDA 7
- [**6**星][7mo] [Python][geosn0w/dumpanywhere64](https://github.com/geosn0w/dumpanywhere64) An IDA (Interactive Disassembler) script that can save a chunk of binary from an address.
- [**6**星][1y] [C++][ecx86/ida7-hexrays-invertif](https://github.com/ecx86/ida7-hexrays-invertif) Hex-Rays Invert if statement plugin for IDA 7.0
- [**5**星][2y] [Python][andreafioraldi/idavshelp](https://github.com/andreafioraldi/idavshelp) 在IDA中集成VS的帮助查看器
- [**5**星][1y] [C++][lab313ru/m68k_fixer](https://github.com/lab313ru/m68k_fixer) IDA Pro plugin fixer for m68k
- [**5**星][5y] [C#][npetrovski/ida-smartpatcher](https://github.com/npetrovski/ida-smartpatcher) IDA apply patch GUI
- [**5**星][4y] [Python][tmr232/tarkus](https://github.com/tmr232/tarkus) Plugin Manager for IDA Pro
- [**4**星][4mo] [Python][fdiskyou/ida-plugins](https://github.com/fdiskyou/ida-plugins) IDAPython脚本（无文档）
    - [banned_functions](https://github.com/fdiskyou/ida-plugins/blob/master/banned_functions.py) 
- [**4**星][1mo] [Python][gitmirar/idaextapi](https://github.com/gitmirar/idaextapi) IDA API utlitites
- [**4**星][3y] [Python][hustlelabs/joseph](https://github.com/hustlelabs/joseph) IDA Viewer Plugins
- [**4**星][1y] [savagedd/samp-server-idb](https://github.com/savagedd/samp-server-idb) None
- [**4**星][4w] [Python][spigwitmer/golang_struct_builder](https://github.com/spigwitmer/golang_struct_builder) IDA 7.0+ script that auto-generates structs and interfaces from runtime metadata found in golang binaries
- [**3**星][8mo] [Python][gdataadvancedanalytics/ida-python](https://github.com/gdataadvancedanalytics/ida-python) None
- [**3**星][2y] [Python][ypcrts/ida-pro-segments](https://github.com/ypcrts/ida-pro-segments) It's very hard to load multiple files in the IDA GUI without it exploding. This makes it easy.
- [**3**星][1y] [abarbatei/ida-utils](https://github.com/abarbatei/ida-utils) links, information and helper scripts for IDA Pro
- [**2**星][2y] [C++][ecx86/ida7-oggplayer](https://github.com/ecx86/ida7-oggplayer) IDA-OggPlayer library by sirmabus, ported to IDA 7
- [**2**星][2y] [Python][mayl8822/ida](https://github.com/mayl8822/ida) 快速执行谷歌/百度/Bing搜索
- [**2**星][5y] [C++][nihilus/ida-x86emu](https://github.com/nihilus/ida-x86emu) x86模拟执行
- [**2**星][4y] [Python][nihilus/idapatchwork](https://github.com/nihilus/idapatchwork) Stitching against malware families with IDA Pro
- [**2**星][2y] [Python][sbouber/idaplugins](https://github.com/sbouber/idaplugins) None
- [**2**星][4w] [Python][psxvoid/idapython-debugging-dynamic-enrichment](https://github.com/psxvoid/idapython-debugging-dynamic-enrichment) None
- [**1**星][2y] [Python][andreafioraldi/idamsdnhelp](https://github.com/andreafioraldi/idamsdnhelp) 打开MSDN帮助搜索页
- [**1**星][1y] [Python][farzonl/idapropluginlab4](https://github.com/farzonl/idapropluginlab4) An ida pro plugin that tracks def use chains of a given x86 binary.
- [**0**星][1mo] [Python][voidsec/ida-helpers](https://github.com/voidsec/ida-helpers) Collection of IDA helpers


***


## <a id="fb4f0c061a72fc38656691746e7c45ce"></a>结构体&&类的检测&&创建&&恢复


### <a id="fa5ede9a4f58d4efd98585d3158be4fb"></a>未分类


- [**920**星][3d] [OCaml][airbus-seclab/bincat](https://github.com/airbus-seclab/bincat) 二进制代码静态分析工具。值分析（寄存器、内存）、污点分析、类型重建和传播（propagation）、前向/后向分析
    - 重复区段: [工具/污点分析&&符号执行](#34ac84853604a7741c61670f2a075d20) |
- [**648**星][4mo] [Python][igogo-x86/hexrayspytools](https://github.com/igogo-x86/hexrayspytools) 结构体和类重建插件
- [**168**星][12mo] [Python][bazad/ida_kernelcache](https://github.com/bazad/ida_kernelcache) 使用IDA Pro重建iOS内核缓存的C++类
    - 重复区段: [工具/Apple&&macOS&&iXxx&&Objective-C&&SWift&&Mach-O/内核缓存](#82d0fa2d6934ce29794a651513934384) |
- [**137**星][4y] [C++][nihilus/hexrays_tools](https://github.com/nihilus/hexrays_tools) 辅助结构体定义和虚函数检测
- [**102**星][2mo] [Python][lucasg/findrpc](https://github.com/lucasg/findrpc)  从二进制文件中提取内部的RPC结构体
- [**4**星][3y] [C#][andreafioraldi/idagrabstrings](https://github.com/andreafioraldi/idagrabstrings) 在指定地址区间内搜索字符串，并将其映射为C结构体
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |


### <a id="4900b1626f10791748b20630af6d6123"></a>C++类&&虚表


- [**591**星][2mo] [Python][0xgalz/virtuailor](https://github.com/0xgalz/virtuailor) 利用IDA调试获取的信息，自动创建C++的虚表
    - 重复区段: [工具/调试&&动态运行&动态数据/调试数据](#b31acf6c84a9506066d497af4e702bf5) |
        <details>
        <summary>查看详情</summary>


        ## 静态部分: 
        - 检测非直接调用
        - 利用条件断点, Hook非直接调用的值赋值过程
        
        ## 动态 部分
        - 创建虚表结构
        - 重命名函数和虚表地址
        - 给反汇编非直接调用添加结构偏移
        - 给非直接调用到虚表之间添加交叉引用
        
        ## 使用
        - File -> Script File -> Main.py(设置断点) -> IDA调试器执行
        </details>


- [**167**星][8mo] [C++][ecx86/classinformer-ida7](https://github.com/ecx86/classinformer-ida7) ClassInformer backported for IDA Pro 7.0
- [**128**星][2y] [Python][nccgroup/susanrtti](https://github.com/nccgroup/SusanRTTI) RTTI解析插件
- [**90**星][1y] [C++][rub-syssec/marx](https://github.com/rub-syssec/marx) 揭示C++程序中的类继承结构
    - [IDA导出](https://github.com/rub-syssec/marx/blob/master/ida_export/export.py) 
    - [IDA导入插件](https://github.com/rub-syssec/marx/tree/master/ida_import) 
    - [核心代码](https://github.com/rub-syssec/marx/tree/master/src) 
- [**65**星][7y] [C][nektra/vtbl-ida-pro-plugin](https://github.com/nektra/vtbl-ida-pro-plugin) Identifying Virtual Table Functions using VTBL IDA Pro Plugin + Deviare Hooking Engine
- [**35**星][5y] [C++][nihilus/ida_classinformer](https://github.com/nihilus/ida_classinformer) IDA ClassInformer PlugIn
- [**32**星][2y] [Python][krystalgamer/dec2struct](https://github.com/krystalgamer/dec2struct) 使用类定义/声明文件，在 IDA 中轻松创建虚表
- [**16**星][2y] [C++][mwl4/ida_gcc_rtti](https://github.com/mwl4/ida_gcc_rtti) Class informer plugin for IDA which supports parsing GCC RTTI




***


## <a id="a7dac37cd93b8bb42c7d6aedccb751b3"></a>收集


- [**1715**星][4w] [onethawt/idaplugins-list](https://github.com/onethawt/idaplugins-list) IDA插件收集
- [**349**星][8mo] [fr0gger/awesome-ida-x64-olly-plugin](https://github.com/fr0gger/awesome-ida-x64-olly-plugin) IDA x64DBG OllyDBG 插件收集
- [**10**星][1y] [Python][ecx86/ida-scripts](https://github.com/ecx86/ida-scripts) IDA Pro/Hex-Rays configs, scripts, and plugins收集


***


## <a id="fabf03b862a776bbd8bcc4574943a65a"></a>外观&&主题


- [**708**星][5mo] [Python][zyantific/idaskins](https://github.com/zyantific/idaskins) 皮肤插件
- [**257**星][7y] [eugeneching/ida-consonance](https://github.com/eugeneching/ida-consonance) 黑色皮肤插件
- [**103**星][5mo] [CSS][0xitx/ida_nightfall](https://github.com/0xitx/ida_nightfall) 黑色主题插件
- [**58**星][7y] [gynophage/solarized_ida](https://github.com/gynophage/solarized_ida) Solarized黑色主题
- [**10**星][7y] [Python][luismiras/ida-color-scripts](https://github.com/luismiras/ida-color-scripts) 导入导出颜色主题
- [**8**星][2y] [CSS][gbps/x64dbg-consonance-theme](https://github.com/gbps/x64dbg-consonance-theme) 黑色的x64dbg主题
- [**6**星][5y] [Python][techbliss/ida-styler](https://github.com/techbliss/ida-styler) 修改IDA样式
- [**3**星][1mo] [rootbsd/ida_pro_zinzolin_theme](https://github.com/rootbsd/ida_pro_zinzolin_theme) zinzolin主题
- [**1**星][11mo] [C][albertzsigovits/idc-dark](https://github.com/albertzsigovits/idc-dark) A dark-mode color scheme for Hex-Rays IDA using idc


***


## <a id="a8f5db3ab4bc7bc3d6ca772b3b9b0b1e"></a>固件&&嵌入式设备


- [**5079**星][3d] [Python][refirmlabs/binwalk](https://github.com/ReFirmLabs/binwalk) 固件分析工具（命令行+IDA插件）
    - [IDA插件](https://github.com/ReFirmLabs/binwalk/tree/master/src/scripts) 
    - [binwalk](https://github.com/ReFirmLabs/binwalk/tree/master/src/binwalk) 
- [**483**星][3mo] [Python][maddiestone/idapythonembeddedtoolkit](https://github.com/maddiestone/idapythonembeddedtoolkit) 自动分析嵌入式设备的固件
- [**172**星][2y] [Python][duo-labs/idapython](https://github.com/duo-labs/idapython) Duo 实验室使用的IDAPython 脚本收集
    - 重复区段: [工具/Apple&&macOS&&iXxx&&Objective-C&&SWift&&Mach-O/未分类](#8530752bacfb388f3726555dc121cb1a) |
    - [cortex_m_firmware](https://github.com/duo-labs/idapython/blob/master/cortex_m_firmware.py)  整理包含ARM Cortex M微控制器固件的IDA Pro数据库
    - [amnesia](https://github.com/duo-labs/idapython/blob/master/amnesia.py) 使用字节级启发式在IDA Pro数据库中的未定义字节中查找ARM Thumb指令
    - [REobjc](https://github.com/duo-labs/idapython/blob/master/reobjc.py) 在Objective-C的调用函数和被调用函数之间进行适当的交叉引用
- [**88**星][6d] [Python][pagalaxylab/vxhunter](https://github.com/PAGalaxyLab/vxhunter) 用于分析基于VxWorks的嵌入式设备的工具集
    - [R2](https://github.com/PAGalaxyLab/vxhunter/blob/master/firmware_tools/vxhunter_r2_py2.py) 
    - [IDA插件](https://github.com/PAGalaxyLab/vxhunter/blob/master/firmware_tools/vxhunter_ida.py) 
    - [Ghidra插件](https://github.com/PAGalaxyLab/vxhunter/tree/master/firmware_tools/ghidra) 


***


## <a id="02088f4884be6c9effb0f1e9a3795e58"></a>签名(FLIRT等)&&比较(Diff)&&匹配


### <a id="cf04b98ea9da0056c055e2050da980c1"></a>未分类


- [**415**星][2w] [C][mcgill-dmas/kam1n0-community](https://github.com/McGill-DMaS/Kam1n0-Community) 汇编代码管理与分析平台(独立工具+IDA插件)
    - 重复区段: [工具/作为辅助&&构成其他的一环](#83de90385d03ac8ef27360bfcdc1ab48) |
    - [IDA插件](https://github.com/McGill-DMaS/Kam1n0-Community/tree/master2.x/kam1n0-clients/ida-plugin) 
    - [kam1n0](https://github.com/McGill-DMaS/Kam1n0-Community/tree/master2.x/kam1n0) 
- [**146**星][12mo] [C++][ajkhoury/sigmaker-x64](https://github.com/ajkhoury/SigMaker-x64) IDA Pro 7.0 compatible SigMaker plugin
- [**128**星][1y] [Python][cisco-talos/bass](https://github.com/cisco-talos/bass) 从先前生成的恶意软件集群的样本中自动生成AV签名
- [**71**星][4y] [Python][icewall/bindifffilter](https://github.com/icewall/bindifffilter) IDA Pro plugin making easier work on BinDiff results
- [**68**星][5y] [Python][arvinddoraiswamy/slid](https://github.com/arvinddoraiswamy/slid) 静态链接库检测
- [**50**星][4w] [Python][vrtadmin/first-plugin-ida](https://github.com/vrtadmin/first-plugin-ida) 函数识别与签名恢复工具
- [**44**星][1y] [Python][l4ys/idasignsrch](https://github.com/l4ys/idasignsrch) 签名搜索
- [**33**星][3y] [Python][g4hsean/binauthor](https://github.com/g4hsean/binauthor) 识别未知二进制文件的作者
- [**31**星][1y] [Python][cisco-talos/casc](https://github.com/cisco-talos/casc) 在IDA的反汇编和字符串窗口中, 辅助创建ClamAV NDB 和 LDB签名
- [**25**星][2y] [LLVM][syreal17/cardinal](https://github.com/syreal17/cardinal) Similarity Analysis to Defeat Malware Compiler Variations
- [**23**星][4mo] [Python][xorpd/fcatalog_server](https://github.com/xorpd/fcatalog_server) Functions Catalog
- [**21**星][3y] [Python][xorpd/fcatalog_client](https://github.com/xorpd/fcatalog_client) fcatalog idapython client
- [**18**星][5y] [Python][zaironne/snippetdetector](https://github.com/zaironne/snippetdetector) IDA Python scripts project for snippets detection
- [**16**星][8y] [C++][alexander-pick/idb2pat](https://github.com/alexander-pick/idb2pat) idb2pat plugin, fixed to work with IDA 6.2
- [**14**星][7y] [Standard ML][letsunlockiphone/iphone-baseband-ida-pro-signature-files](https://github.com/letsunlockiphone/iphone-baseband-ida-pro-signature-files) IDA签名文件，iPhone基带逆向
    - 重复区段: [工具/Apple&&macOS&&iXxx&&Objective-C&&SWift&&Mach-O/未分类](#8530752bacfb388f3726555dc121cb1a) |
- [**3**星][4y] [Python][ayuto/discover_win](https://github.com/ayuto/discover_win) 对比Linux和Windows二进制文件，对Windows文件未命名的函数进行自动重命名
    - 重复区段: [工具/函数相关/重命名&&前缀&&标记](#73813456eeb8212fd45e0ea347bec349) |
- [**0**星][1y] [Python][gh0st3rs/idaprotosync](https://github.com/gh0st3rs/idaprotosync) 在2个或多个函数中识别函数原型


### <a id="19360afa4287236abe47166154bc1ece"></a>FLIRT签名


#### <a id="1c9d8dfef3c651480661f98418c49197"></a>FLIRT签名收集


- [**581**星][1y] [Max][maktm/flirtdb](https://github.com/Maktm/FLIRTDB) A community driven collection of IDA FLIRT signature files
- [**299**星][3mo] [push0ebp/sig-database](https://github.com/push0ebp/sig-database) IDA FLIRT Signature Database
- [**4**星][7mo] [cloudwindby/ida-pro-sig](https://github.com/cloudwindby/ida-pro-sig) IDA PRO FLIRT signature files MSVC2017的sig文件


#### <a id="a9a63d23d32c6c789ca4d2e146c9b6d0"></a>FLIRT签名生成


- [**56**星][9mo] [Python][push0ebp/allirt](https://github.com/push0ebp/allirt) Tool that converts All of libc to signatures for IDA Pro FLIRT Plugin. and utility make sig with FLAIR easily
- [**40**星][7mo] [Python][nwmonster/applysig](https://github.com/nwmonster/applysig) Apply IDA FLIRT signatures for Ghidra
    - 重复区段: [工具/导入导出&与其他工具交互/Ghidra](#c7066b0c388cd447e980bf0eb38f39ab) |




### <a id="161e5a3437461dc8959cc923e6a18ef7"></a>Diff&&Match工具


- [**1520**星][2w] [Python][joxeankoret/diaphora](https://github.com/joxeankoret/diaphora) program diffing
- [**349**星][3mo] [Python][checkpointsw/karta](https://github.com/checkpointsw/karta) Karta - source code assisted fast binary matching plugin for IDA
- [**327**星][11mo] [Python][joxeankoret/pigaios](https://github.com/joxeankoret/pigaios) A tool for matching and diffing source codes directly against binaries.
- [**136**星][12mo] [Python][nirizr/rematch](https://github.com/nirizr/rematch) REmatch, a complete binary diffing framework that is free and strives to be open source and community driven.
- [**94**星][6mo] [Visual Basic][dzzie/idacompare](https://github.com/dzzie/idacompare) 汇编级别对比工具
- [**72**星][5y] [Python][binsigma/binsourcerer](https://github.com/binsigma/binsourcerer) 反汇编与源码匹配
- [**72**星][4y] [C][nihilus/ida_signsrch](https://github.com/nihilus/ida_signsrch) signsrch签名匹配
- [**71**星][3y] [vrtadmin/first](https://github.com/vrtadmin/first) 函数识别和签名恢复, 带服务器
- [**51**星][5y] [C++][filcab/patchdiff2](https://github.com/filcab/patchdiff2) IDA binary differ. Since code.google.com/p/patchdiff2/ seemed abandoned, I did the obvious thing…
- [**14**星][2y] [Python][0x00ach/idadiff](https://github.com/0x00ach/idadiff) IDAPython脚本，使用@Heurs MACHOC algorithm (https://github.com/ANSSI-FR/polichombr)算法创建二进制文件的CFG Hash，与其他样本对比。如果发现1-1关系，则重命名
- [**14**星][5y] [C++][binsigma/binclone](https://github.com/binsigma/binclone) 检测恶意代码中的相似代码


### <a id="46c9dfc585ae59fe5e6f7ddf542fb31a"></a>Yara


- [**418**星][2w] [Python][polymorf/findcrypt-yara](https://github.com/polymorf/findcrypt-yara) 使用Yara规则查找加密常量
    - 重复区段: [工具/加密解密](#06d2caabef97cf663bd29af2b1fe270c) |
- [**92**星][3w] [Python][hyuunnn/hyara](https://github.com/hyuunnn/Hyara) 辅助编写Yara规则
    - [IDA插件](https://github.com/hy00un/hyara/tree/master/IDA%20Plugin) 
    - [BinaryNinja插件](https://github.com/hy00un/hyara/tree/master/BinaryNinja%20Plugin) 
- [**81**星][1y] [Python][oalabs/findyara](https://github.com/oalabs/findyara) 使用Yara规则扫描二进制文件
- [**16**星][10mo] [Python][bnbdr/ida-yara-processor](https://github.com/bnbdr/ida-yara-processor) 针对已编译Yara规则文件的Loader&&Processor
    - 重复区段: [工具/针对特定分析目标/Loader&Processor](#cb59d84840e41330a7b5e275c0b81725) |
- [**14**星][1y] [Python][alexander-hanel/ida_yara](https://github.com/alexander-hanel/ida_yara) 使用Yara扫描IDB数据
- [**14**星][12mo] [Python][souhailhammou/idaray-plugin](https://github.com/souhailhammou/idaray-plugin) IDARay is an IDA Pro plugin that matches the database against multiple YARA files which themselves may contain multiple rules.




***


## <a id="5e91b280aab7f242cbc37d64ddbff82f"></a>IDB操作


- [**312**星][5mo] [Python][williballenthin/python-idb](https://github.com/williballenthin/python-idb) idb 文件解析和分析工具
- [**135**星][11mo] [Python][nccgroup/idahunt](https://github.com/nccgroup/idahunt) 在IDA外部使用IDAPython脚本, 批量创建/读取/解析IDB文件, 可编写自己的IDB分析脚本,命令行工具,
- [**84**星][4mo] [C++][nlitsme/idbutil](https://github.com/nlitsme/idbutil) 从 IDA 数据库中提取数据，支持 idb 及 i64
- [**78**星][2mo] [Python][nlitsme/pyidbutil](https://github.com/nlitsme/pyidbutil) 读取IDB数据库
- [**18**星][1y] [Python][kkhaike/tinyidb](https://github.com/kkhaike/tinyidb) 从巨型IDB数据库中导出用户数据
- [**0**星][4y] [C][hugues92/idaextrapassplugin](https://github.com/hugues92/idaextrapassplugin) 修复与清理IDB数据库


***


## <a id="206ca17fc949b8e0ae62731d9bb244cb"></a>协作逆向&&多人操作相同IDB文件


- [**504**星][10mo] [Python][idarlingteam/idarling](https://github.com/IDArlingTeam/IDArling) 多人协作插件
- [**257**星][12mo] [C++][dga-mi-ssi/yaco](https://github.com/dga-mi-ssi/yaco) 利用Git版本控制，同步多人对相同二进制文件的修改
- [**88**星][5y] [Python][cubicalabs/idasynergy](https://github.com/cubicalabs/idasynergy) 集成了版本控制系统(svn)的IDA插件
- [**70**星][1w] [C++][cseagle/collabreate](https://github.com/cseagle/collabreate) Hook IDA的事件通知，将事件涉及的修改内容广播到中心服务器，中心服务器转发给其他分析相同文件的用户
- [**4**星][2y] [python][argussecurity/psida](https://bitbucket.org/socialauth/login/atlassianid/?next=%2Fargussecurity%2Fpsida) IDAPython脚本收集，当前只有协作逆向的脚本


***


## <a id="f7d311685152ac005cfce5753c006e4b"></a>与调试器同步&&通信&&交互


- [**444**星][1w] [C][bootleg/ret-sync](https://github.com/bootleg/ret-sync) 在反汇编工具和调试器之间同步调试会话
    - [GDB插件](https://github.com/bootleg/ret-sync/tree/master/ext_gdb) 
    - [Ghidra插件](https://github.com/bootleg/ret-sync/tree/master/ext_ghidra) 
    - [IDA插件](https://github.com/bootleg/ret-sync/tree/master/ext_ida) 
    - [LLDB](https://github.com/bootleg/ret-sync/tree/master/ext_lldb) 
    - [OD](https://github.com/bootleg/ret-sync/tree/master/ext_olly1) 
    - [OD2](https://github.com/bootleg/ret-sync/tree/master/ext_olly2) 
    - [WinDgb](https://github.com/bootleg/ret-sync/tree/master/ext_windbg/sync) 
    - [x64dbg](https://github.com/bootleg/ret-sync/tree/master/ext_x64dbg) 
- [**283**星][9mo] [C][a1ext/labeless](https://github.com/a1ext/labeless) 在IDA和调试器之间无缝同步Label/注释等
    - [IDA插件](https://github.com/a1ext/labeless/tree/master/labeless_ida) 
    - [OD](https://github.com/a1ext/labeless/tree/master/labeless_olly) 
    - [OD2](https://github.com/a1ext/labeless/tree/master/labeless_olly2) 
    - [x64dbg](https://github.com/a1ext/labeless/tree/master/labeless_x64dbg) 
- [**166**星][11mo] [Python][andreafioraldi/idangr](https://github.com/andreafioraldi/idangr) 在IDA中使用angrdbg调试器进行调试
- [**128**星][2y] [Python][comsecuris/gdbida](https://github.com/comsecuris/gdbida) 使用GDB调试时，在IDA中自动跟随当前GDB的调试位置
    - [IDA插件](https://github.com/comsecuris/gdbida/blob/master/ida_gdb_bridge.py) 
    - [GDB脚本](https://github.com/comsecuris/gdbida/blob/master/gdb_ida_bridge_client.py) 
- [**98**星][4y] [C++][quarkslab/qb-sync](https://github.com/quarkslab/qb-sync) 使用调试器调试时，自动在IDA中跟随调试位置
    - [GDB插件](https://github.com/quarkslab/qb-sync/tree/master/ext_gdb) 
    - [IDA插件](https://github.com/quarkslab/qb-sync/tree/master/ext_ida) 
    - [LLDB](https://github.com/quarkslab/qb-sync/tree/master/ext_lldb) 
    - [OD2](https://github.com/quarkslab/qb-sync/tree/master/ext_olly2) 
    - [WinDbg](https://github.com/quarkslab/qb-sync/tree/master/ext_windbg/sync) 
    - [x64dbg](https://github.com/quarkslab/qb-sync/tree/master/ext_x64dbg) 
- [**43**星][2mo] [JavaScript][sinakarvandi/windbg2ida](https://github.com/sinakarvandi/windbg2ida) 在IDA中显示Windbg调试的每个步骤
    - [Windbg脚本](https://github.com/sinakarvandi/windbg2ida/blob/master/windbg2ida.js) JavaScript
    - [IDA脚本](https://github.com/sinakarvandi/windbg2ida/blob/master/IDAScript.py) 
- [**36**星][9mo] [Python][anic/ida2pwntools](https://github.com/anic/ida2pwntools) IDA插件，远程连接pwntools启动的程序进行pwn调试
- [**28**星][1y] [Python][iweizime/dbghider](https://github.com/iweizime/dbghider) 向被调试进程隐藏IDA调试器
- [**17**星][7y] [Python][rmadair/windbg2ida](https://github.com/rmadair/windbg2ida) 将WinDBG中的调试trace导入到IDA


***


## <a id="6fb7e41786c49cc3811305c520dfe9a1"></a>导入导出&与其他工具交互


### <a id="8ad723b704b044e664970b11ce103c09"></a>未分类


- [**158**星][3w] [Python][x64dbg/x64dbgida](https://github.com/x64dbg/x64dbgida) x64dbg插件，用于IDA数据导入导出
- [**143**星][3w] [C++][alschwalm/dwarfexport](https://github.com/alschwalm/dwarfexport) Export dwarf debug information from IDA Pro
- [**95**星][2y] [Python][robindavid/idasec](https://github.com/robindavid/idasec) IDA插件，与Binsec 平台进行交互
- [**67**星][11mo] [Python][lucasg/idamagnum](https://github.com/lucasg/idamagnum) 在IDA中向MagnumDB发起请求, 查询枚举常量可能的值
- [**58**星][7mo] [Python][binaryanalysisplatform/bap-ida-python](https://github.com/binaryanalysisplatform/bap-ida-python) IDAPython脚本，在IDA中集成BAP
- [**35**星][5y] [Python][siberas/ida2sym](https://github.com/siberas/ida2sym) IDAScript to create Symbol file which can be loaded in WinDbg via AddSyntheticSymbol
- [**29**星][5y] [C++][oct0xor/deci3dbg](https://github.com/oct0xor/deci3dbg) Ida Pro debugger module for Playstation 3
    - 重复区段: [工具/针对特定分析目标/PS3&&PS4](#315b1b8b41c67ae91b841fce1d4190b5) |
- [**28**星][4mo] [C++][thalium/idatag](https://github.com/thalium/idatag) IDA plugin to explore and browse tags
- [**19**星][2y] [Python][brandon-everhart/angryida](https://github.com/brandon-everhart/angryida) 在IDA中集成angr二进制分析框架
- [**16**星][4y] [C++][m417z/mapimp](https://github.com/m417z/mapimp) This is an OllyDbg plugin which will help you to import map files exported by IDA, Dede, IDR, Microsoft and Borland linkers.
- [**16**星][4y] [Python][danielmgmi/virusbattle-ida-plugin](https://github.com/danielmgmi/virusbattle-ida-plugin) The plugin is an integration of Virus Battle API to the well known IDA Disassembler.
- [**8**星][7y] [C++][patois/madnes](https://github.com/patois/madnes) 从IDB中导出符号和名称，使可在FCEUXD SP中导入
- [**3**星][1y] [Python][r00tus3r/differential_debugging](https://github.com/r00tus3r/differential_debugging) Differential debugging using IDA Python and GDB


### <a id="c7066b0c388cd447e980bf0eb38f39ab"></a>Ghidra


- [**282**星][2mo] [Python][cisco-talos/ghida](https://github.com/cisco-talos/ghida) 在IDA中集成Ghidra反编译器
- [**233**星][7mo] [Python][daenerys-sre/source](https://github.com/daenerys-sre/source) 使IDA和Ghidra脚本通用, 无需修改
- [**84**星][2mo] [Python][cisco-talos/ghidraaas](https://github.com/cisco-talos/ghidraaas) 通过REST API暴露Ghidra分析服务, 也是GhIDA的后端
- [**47**星][3w] [Python][utkonos/lst2x64dbg](https://github.com/utkonos/lst2x64dbg) Extract labels from IDA .lst or Ghidra .csv file and export x64dbg database.
- [**40**星][7mo] [Python][nwmonster/applysig](https://github.com/nwmonster/applysig) Apply IDA FLIRT signatures for Ghidra
    - 重复区段: [工具/签名(FLIRT等)&&比较(Diff)&&匹配/FLIRT签名/FLIRT签名生成](#a9a63d23d32c6c789ca4d2e146c9b6d0) |


### <a id="11139e7d6db4c1cef22718868f29fe12"></a>BinNavi


- [**377**星][4d] [C++][google/binexport](https://github.com/google/binexport) 将反汇编以Protocol Buffer的形式导出为PostgreSQL数据库, 导入到BinNavi中使用
- [**213**星][3y] [PLpgSQL][cseagle/freedom](https://github.com/cseagle/freedom) 从IDA中导出反汇编信息, 导入到binnavi中使用
- [**25**星][7y] [Python][tosanjay/bopfunctionrecognition](https://github.com/tosanjay/bopfunctionrecognition) This python/jython script is used as plugin to BinNavi tool to analyze a x86 binanry file to find buffer overflow prone functions. Such functions are important for vulnerability analysis.


### <a id="d1ff64bee76f6749aef6100d72bfbe3a"></a>BinaryNinja


- [**67**星][7mo] [Python][lunixbochs/revsync](https://github.com/lunixbochs/revsync) IDA和Binja实时同步插件
- [**60**星][4mo] [Python][zznop/bnida](https://github.com/zznop/bnida) 4个脚本，在IDA和BinaryNinja间交互数据
    - [ida_export](https://github.com/zznop/bnida/blob/master/ida/ida_export.py) 将数据从IDA中导入
    - [ida_import](https://github.com/zznop/bnida/blob/master/ida/ida_import.py) 将数据导入到IDA
    - [binja_export](https://github.com/zznop/bnida/blob/master/binja_export.py) 将数据从BinaryNinja中导出
    - [binja_import](https://github.com/zznop/bnida/blob/master/binja_import.py) 将数据导入到BinaryNinja
- [**14**星][4mo] [Python][cryptogenic/idc_importer](https://github.com/cryptogenic/idc_importer) Binary Ninja插件，从IDA中导入IDC数据库转储


### <a id="21ed198ae5a974877d7a635a4b039ae3"></a>Radare2


- [**125**星][7mo] [Python][danigargu/syms2elf](https://github.com/danigargu/syms2elf) 将IDA Pro和Radare2识别的符号（目前仅函数）导出到ELF符号表
    - 重复区段: [工具/ELF](#e5e403123c70ddae7bd904d3a3005dbb) |[工具/函数相关/未分类](#347a2158bdd92b00cd3d4ba9a0be00ae) |
- [**123**星][2w] [Python][radare/radare2ida](https://github.com/radare/radare2ida) Tools, documentation and scripts to move projects from IDA to R2 and viceversa


### <a id="a1cf7f7f849b4ca2101bd31449c2a0fd"></a>Frida


- [**129**星][3y] [Python][friedappleteam/frapl](https://github.com/friedappleteam/frapl) 在Frida Client和IDA之间建立连接，将运行时信息直接导入IDA，并可直接在IDA中控制Frida
    - 重复区段: [工具/调试&&动态运行&动态数据/DBI数据](#0fbd352f703b507853c610a664f024d1) |
    - [IDA插件](https://github.com/FriedAppleTeam/FRAPL/tree/master/Framework/FridaLink) 
    - [Frida脚本](https://github.com/FriedAppleTeam/FRAPL/tree/master/Framework/FRAPL) 
- [**79**星][5y] [Python][techbliss/frida_for_ida_pro](https://github.com/techbliss/frida_for_ida_pro) 在IDA中使用Frida, 主要用于追踪函数
- [**47**星][2mo] [Python][lich4/personal_script](https://github.com/lich4/personal_script) 010Editor/BurpSuite/Frida/IDA等多个工具的多个脚本
    - 重复区段: [工具/未分类](#c39a6d8598dde6abfeef43faf931beb5) |
    - [010Editor](https://github.com/lich4/personal_script/tree/master/010Editor_Script) 010Editor的多个脚本
    - [ParamChecker](https://github.com/lich4/personal_script/tree/master/BurpSuite_Script) Burp插件
    - [Frida](https://github.com/lich4/personal_script/tree/master/Frida_script) Frida多个脚本
    - [IDA](https://github.com/lich4/personal_script/tree/master/IDA_Script) IDA多个脚本
    - [IDA-read_unicode.py](https://github.com/lich4/personal_script/blob/master/IDA_Script/read_unicode.py) IDA插件，识别程序中的中文字符
    - [IDA-add_xref_for_macho](https://github.com/lich4/personal_script/blob/master/IDA_Script/add_xref_for_macho.py) 辅助识别Objective-C成员函数的caller和callee
    - [IDA-add_info_for_androidgdb](https://github.com/lich4/personal_script/blob/master/IDA_Script/add_info_for_androidgdb.py) 使用gdbserver和IDA调试Android时，读取module列表和segment
    - [IDA-trace_instruction](https://github.com/lich4/personal_script/blob/master/IDA_Script/trace_instruction.py) 追踪指令流
    - [IDA-detect_ollvm](https://github.com/lich4/personal_script/blob/master/IDA_Script/detect_ollvm.py) 检测OLLVM，在某些情况下修复（Android/iOS）
    - [IDA-add_block_for_macho](https://github.com/lich4/personal_script/blob/master/IDA_Script/add_block_for_macho.py) 分析macho文件中的block结构


### <a id="dd0332da5a1482df414658250e6357f8"></a>IntelPin


- [**133**星][1y] [Python][carlosgprado/jarvis](https://github.com/carlosgprado/jarvis) 多功能, 带界面,辅助静态分析、漏洞挖掘、动态追踪(Pin)、导入导出等
    - 重复区段: [工具/调试&&动态运行&动态数据/DBI数据](#0fbd352f703b507853c610a664f024d1) |[工具/漏洞/未分类](#385d6777d0747e79cccab0a19fa90e7e) |
    - [IDA插件](https://github.com/carlosgprado/jarvis/tree/master/IDAPlugin) 
    - [PinTracer](https://github.com/carlosgprado/jarvis/tree/master/PinTracer) 
- [**43**星][3y] [Batchfile][maldiohead/idapin](https://github.com/maldiohead/idapin) plugin of ida with pin




***


## <a id="004c199e1dbf71769fbafcd8e58d1ead"></a>针对特定分析目标


### <a id="5578c56ca09a5804433524047840980e"></a>未分类


- [**537**星][2y] [Python][anatolikalysch/vmattack](https://github.com/anatolikalysch/vmattack) 基于虚拟化的壳的分析(静态/动态)与反混淆
    - 重复区段: [工具/反混淆](#7199e8787c0de5b428f50263f965fda7) |
- [**195**星][3y] [Python][f8left/decllvm](https://github.com/f8left/decllvm) 针对OLLVM的IDA分析插件
- [**116**星][1y] [Python][xerub/idastuff](https://github.com/xerub/idastuff) 针对ARM处理器
- [**93**星][3mo] [Python][themadinventor/ida-xtensa](https://github.com/themadinventor/ida-xtensa) 分析Tensilica Xtensa (as seen in ESP8266)
- [**81**星][4y] [C++][wjp/idados](https://github.com/wjp/idados) DOSBox调试器插件
    - 重复区段: [工具/调试&&动态运行&动态数据/未分类](#2944dda5289f494e5e636089db0d6a6a) |
- [**72**星][2mo] [Python][coldzer0/ida-for-delphi](https://github.com/coldzer0/ida-for-delphi) 针对Delphi的IDAPython脚本，从 Event Constructor (VCL)中获取所有函数名称
- [**59**星][1y] [Python][isra17/nrs](https://github.com/isra17/nrs) 脱壳并分析NSIS installer打包的文件
- [**52**星][3mo] [Python][giantbranch/mipsaudit](https://github.com/giantbranch/mipsaudit) IDA MIPS静态扫描脚本，汇编审计辅助脚本
- [**50**星][4mo] [C++][troybowman/dtxmsg](https://github.com/troybowman/dtxmsg) 辅助逆向DTXConnectionServices 框架
- [**47**星][2y] [C++][antid0tecom/aarch64_armv81extension](https://github.com/antid0tecom/aarch64_armv81extension) IDA AArch64 处理器扩展：添加对ARMv8.1 opcodes的支持
- [**47**星][8mo] [C][lab313ru/smd_ida_tools](https://github.com/lab313ru/smd_ida_tools) Sega Genesis/MegaDrive ROM文件加载器，Z80音频驱动加载器，IDA Pro调试器
- [**33**星][3y] [Python][sam-b/windows_syscalls_dumper](https://github.com/sam-b/windows_syscalls_dumper) 转储Windows系统调用Call的 number/name，以json格式导出
- [**23**星][3y] [Python][pfalcon/ida-xtensa2](https://github.com/pfalcon/ida-xtensa2) IDAPython plugin for Tensilica Xtensa (as seen in ESP8266), version 2
- [**21**星][10mo] [Python][howmp/comfinder](https://github.com/howmp/comfinder) 查找标记COM组件中的函数
    - 重复区段: [工具/函数相关/重命名&&前缀&&标记](#73813456eeb8212fd45e0ea347bec349) |
- [**20**星][5y] [Python][digitalbond/ibal](https://github.com/digitalbond/ibal) 辅助Bootrom分析
- [**17**星][2y] [C][andywhittaker/idaproboschme7x](https://github.com/andywhittaker/idaproboschme7x) Bosch ME7x C16x反汇编辅助
- [**16**星][3y] [Python][0xdeva/ida-cpu-risc-v](https://github.com/0xdeva/ida-cpu-risc-v) RISCV-V 反汇编器
- [**15**星][5y] [Python][dolphin-emu/gcdsp-ida](https://github.com/dolphin-emu/gcdsp-ida) 辅助GC DSP逆向
- [**11**星][2y] [C++][hyperiris/gekkops](https://github.com/hyperiris/gekkops) Nintendo GameCube Gekko CPU Extension plug-in for IDA Pro 5.2
- [**4**星][3y] [Python][neogeodev/idaneogeo](https://github.com/neogeodev/idaneogeo) NeoGeo binary loader & helper for the Interactive Disassembler
- [**2**星][3mo] [C][extremlapin/glua_c_headers_for_ida](https://github.com/extremlapin/glua_c_headers_for_ida) Glua module C headers for IDA
- [**2**星][4mo] [Python][lucienmp/idapro_m68k](https://github.com/lucienmp/idapro_m68k) 扩展IDA对m68k的支持，添加gdb step-over 和类型信息支持
- [**0**星][7mo] [C][0xd0cf11e/idcscripts](https://github.com/0xd0cf11e/idcscripts) idc脚本
    - [emotet-decode](https://github.com/0xd0cf11e/idcscripts/blob/master/emotet/emotet-decode.idc) 解码emotet
- [**0**星][4w] [C++][marakew/emuppc](https://github.com/marakew/emuppc) PowerPC模拟器，脱壳某些 PowerPC 二进制文件


### <a id="1b17ac638aaa09852966306760fda46b"></a>GoLang


- [**362**星][8mo] [Python][sibears/idagolanghelper](https://github.com/sibears/idagolanghelper) 解析Go语言编译的二进制文件中的GoLang类型信息
- [**279**星][2w] [Python][strazzere/golang_loader_assist](https://github.com/strazzere/golang_loader_assist) 辅助Go逆向


### <a id="4c158ccc5aee04383755851844fdd137"></a>Windows驱动


- [**302**星][1y] [Python][fsecurelabs/win_driver_plugin](https://github.com/FSecureLABS/win_driver_plugin) A tool to help when dealing with Windows IOCTL codes or reversing Windows drivers.
- [**216**星][12mo] [Python][nccgroup/driverbuddy](https://github.com/nccgroup/driverbuddy) 辅助逆向Windows内核驱动
- [**73**星][4y] [Python][tandasat/winioctldecoder](https://github.com/tandasat/winioctldecoder) IDA插件，将Windows设备IO控制码解码成为DeviceType, FunctionCode, AccessType, MethodType.
- [**23**星][1y] [C][ioactive/kmdf_re](https://github.com/ioactive/kmdf_re) 辅助逆向KMDF驱动


### <a id="315b1b8b41c67ae91b841fce1d4190b5"></a>PS3&&PS4


- [**68**星][1mo] [C][aerosoul94/ida_gel](https://github.com/aerosoul94/ida_gel) A collection of IDA loaders for various game console ELF's. (PS3, PSVita, WiiU)
- [**55**星][7y] [C++][kakaroto/ps3ida](https://github.com/kakaroto/ps3ida) IDA scripts and plugins for PS3
- [**44**星][2y] [C][aerosoul94/dynlib](https://github.com/aerosoul94/dynlib) 辅助PS4用户模式ELF逆向
    - 重复区段: [工具/ELF](#e5e403123c70ddae7bd904d3a3005dbb) |
- [**29**星][5y] [C++][oct0xor/deci3dbg](https://github.com/oct0xor/deci3dbg) Ida Pro debugger module for Playstation 3
    - 重复区段: [工具/导入导出&与其他工具交互/未分类](#8ad723b704b044e664970b11ce103c09) |


### <a id="cb59d84840e41330a7b5e275c0b81725"></a>Loader&Processor


- [**205**星][1y] [Python][fireeye/idawasm](https://github.com/fireeye/idawasm) WebAssembly的加载器和解析器
- [**158**星][4w] [Python][nforest/droidimg](https://github.com/nforest/droidimg) Android/Linux vmlinux loader
    - 重复区段: [工具/Android](#66052f824f5054aa0f70785a2389a478) |[工具/ELF](#e5e403123c70ddae7bd904d3a3005dbb) |
- [**155**星][2y] [Python][crytic/ida-evm](https://github.com/crytic/ida-evm) 以太坊虚拟机的Processor模块
- [**137**星][3w] [Python][argp/iboot64helper](https://github.com/argp/iboot64helper) IDAPython loader to help with AArch64 iBoot, iBEC, and SecureROM reverse engineering
- [**125**星][2y] [C][gsmk/hexagon](https://github.com/gsmk/hexagon) IDA processor module for the hexagon (QDSP6) processor
- [**105**星][1y] [pgarba/switchidaproloader](https://github.com/pgarba/switchidaproloader) Loader for IDA Pro to support the Nintendo Switch NRO binaries
- [**72**星][2y] [Python][embedi/meloader](https://github.com/embedi/meloader) 加载英特尔管理引擎固件
- [**53**星][5mo] [C++][mefistotelis/ida-pro-loadmap](https://github.com/mefistotelis/ida-pro-loadmap) Plugin for IDA Pro disassembler which allows loading .map files.
- [**37**星][11mo] [C++][patois/nesldr](https://github.com/patois/nesldr) Nintendo Entertainment System (NES) ROM loader module for IDA Pro
- [**35**星][1y] [Python][bnbdr/ida-bpf-processor](https://github.com/bnbdr/ida-bpf-processor) BPF Processor for IDA Python
- [**32**星][5y] [Python][0xebfe/3dsx-ida-pro-loader](https://github.com/0xebfe/3dsx-ida-pro-loader) IDA PRO Loader for 3DSX files
- [**32**星][1y] [C++][teammolecule/toshiba-mep-idp](https://github.com/TeamMolecule/toshiba-mep-idp) IDA Pro module for Toshiba MeP processors
- [**28**星][4y] [C][gdbinit/teloader](https://github.com/gdbinit/teloader) A TE executable format loader for IDA
- [**27**星][3y] [Python][w4kfu/ida_loader](https://github.com/w4kfu/ida_loader) loader module 收集
- [**25**星][2mo] [Python][ghassani/mclf-ida-loader](https://github.com/ghassani/mclf-ida-loader) An IDA file loader for Mobicore trustlet and driver binaries
- [**23**星][1y] [C++][balika011/belf](https://github.com/balika011/belf) Balika011's PlayStation 4 ELF loader for IDA Pro 7.0/7.1
- [**23**星][6y] [vtsingaras/qcom-mbn-ida-loader](https://github.com/vtsingaras/qcom-mbn-ida-loader) IDA loader plugin for Qualcomm Bootloader Stages
- [**20**星][3y] [C++][patois/ndsldr](https://github.com/patois/ndsldr) Nintendo DS ROM loader module for IDA Pro
- [**18**星][8y] [Python][rpw/flsloader](https://github.com/rpw/flsloader) IDA Pro loader module for Infineon/Intel-based iPhone baseband firmwares
- [**17**星][7mo] [C++][gocha/ida-snes-ldr](https://github.com/gocha/ida-snes-ldr) SNES ROM Cartridge File Loader for IDA (Interactive Disassembler) 6.x
- [**16**星][10mo] [Python][bnbdr/ida-yara-processor](https://github.com/bnbdr/ida-yara-processor) 针对已编译Yara规则文件的Loader&&Processor
    - 重复区段: [工具/签名(FLIRT等)&&比较(Diff)&&匹配/Yara](#46c9dfc585ae59fe5e6f7ddf542fb31a) |
- [**16**星][7mo] [C++][gocha/ida-65816-module](https://github.com/gocha/ida-65816-module) SNES 65816 processor plugin for IDA (Interactive Disassembler) 6.x
- [**16**星][12mo] [Python][lcq2/riscv-ida](https://github.com/lcq2/riscv-ida) RISC-V ISA处理器模块
- [**16**星][1y] [Python][ptresearch/nios2](https://github.com/ptresearch/nios2) IDA Pro processor module for Altera Nios II Classic/Gen2 microprocessor architecture
- [**13**星][2y] [Python][patois/necromancer](https://github.com/patois/necromancer) IDA Pro V850 Processor Module Extension
- [**13**星][1y] [Python][rolfrolles/hiddenbeeloader](https://github.com/rolfrolles/hiddenbeeloader) IDA loader module for Hidden Bee's custom executable file format
- [**10**星][4y] [C++][areidz/nds_loader](https://github.com/areidz/nds_loader) Nintendo DS loader module for IDA Pro 6.1
- [**10**星][6y] [python][cycad/mbn_loader](https://github.com/cycad/mbn_loader) IDA Pro Loader Plugin for Samsung Galaxy S4 ROMs
- [**7**星][1y] [C++][fail0verflow/rl78-ida-proc](https://github.com/fail0verflow/rl78-ida-proc) Renesas RL78 processor module for IDA
- [**5**星][8mo] [C++][gocha/ida-spc700-module](https://github.com/gocha/ida-spc700-module) SNES SPC700 processor plugin for IDA (Interactive Disassembler)
- [**3**星][8mo] [C++][gocha/ida-snes_spc-ldr](https://github.com/gocha/ida-snes_spc-ldr) SNES-SPC700 Sound File Loader for IDA (Interactive Disassembler)
- [**2**星][1mo] [C][cisco-talos/ida_tilegx](https://github.com/cisco-talos/ida_tilegx) This is an IDA processor module for the Tile-GX processor architecture


### <a id="f5e51763bb09d8fd47ee575a98bedca1"></a>PDB


- [**62**星][3mo] [C++][mixaill/fakepdb](https://github.com/mixaill/fakepdb) 通过IDA数据库生成PDB文件
- [**38**星][1y] [Python][ax330d/ida_pdb_loader](https://github.com/ax330d/ida_pdb_loader) IDA PDB Loader
- [**14**星][1y] [CMake][gdataadvancedanalytics/bindifflib](https://github.com/gdataadvancedanalytics/bindifflib) Automated library compilation and PDB annotation with CMake and IDA Pro
- [**2**星][5mo] [Python][clarkb7/annotate_lineinfo](https://github.com/clarkb7/annotate_lineinfo) Annotate IDA with source and line number information from a PDB


### <a id="7d0681efba2cf3adaba2780330cd923a"></a>Flash&&SWF


- [**33**星][1y] [Python][kasperskylab/actionscript3](https://github.com/kasperskylab/actionscript3) SWF Loader、ActionScript3 Processor和 IDA 调试辅助插件
- [**27**星][4y] [C++][nihilus/ida-pro-swf](https://github.com/nihilus/ida-pro-swf) 处理SWF文件


### <a id="841d605300beba45c3be131988514a03"></a>特定样本家族


- [**9**星][2y] [Python][d00rt/easy_way_nymaim](https://github.com/d00rt/easy_way_nymaim) IDA脚本, 用于去除恶意代码nymaim的混淆,创建干净的idb
- [**8**星][3y] [Python][thngkaiyuan/mynaim](https://github.com/thngkaiyuan/mynaim) Nymaim 家族样本反混淆插件
    - 重复区段: [工具/反混淆](#7199e8787c0de5b428f50263f965fda7) |
- [**4**星][1y] [Python][immortalp0ny/fyvmdisassembler](https://github.com/immortalp0ny/fyvmdisassembler) 对 FinSpy VM进行反虚拟化/反汇编的IDAPython脚本
- [**4**星][7mo] [C][lacike/gandcrab_string_decryptor](https://github.com/lacike/gandcrab_string_decryptor) 解密 GandCrab v5.1-5.3 中的字符串
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |


### <a id="ad44205b2d943cfa2fa805b2643f4595"></a>CTF


- [**130**星][2y] [Python][pwning/defcon25-public](https://github.com/pwning/defcon25-public) DEFCON 25 某Talk用到的 反汇编器和 IDA 模块




***


## <a id="ad68872e14f70db53e8d9519213ec039"></a>IDAPython本身


### <a id="2299bc16945c25652e5ad4d48eae8eca"></a>未分类


- [**706**星][3w] [Python][idapython/src](https://github.com/idapython/src) IDAPython源码
- [**362**星][4w] [Python][tmr232/sark](https://github.com/tmr232/sark) IDAPython的高级抽象
- [**249**星][2y] [Python][intezer/docker-ida](https://github.com/intezer/docker-ida) 在Docker容器中执行IDA, 以自动化/可扩展/分布式的方式执行IDAPython脚本
- [**79**星][4y] [idapython/bin](https://github.com/idapython/bin) IDAPython binaries
- [**65**星][2y] [Python][alexander-hanel/idapython6to7](https://github.com/alexander-hanel/idapython6to7) None
- [**43**星][1y] [Python][nirizr/pytest-idapro](https://github.com/nirizr/pytest-idapro) 辅助对IDAPython脚本进行单元测试
- [**28**星][2y] [Python][kerrigan29a/idapython_virtualenv](https://github.com/kerrigan29a/idapython_virtualenv) 在IDAPython中启用Virtualenv或Conda，使可以有多个虚拟环境
- [**23**星][3y] [Python][devttys0/idascript](https://github.com/devttys0/idascript) IDA的Wrapper，在命令行中自动对目标文件执行IDA脚本


### <a id="c42137cf98d6042372b1fd43c3635135"></a>cheatsheets


- [**230**星][1mo] [Python][inforion/idapython-cheatsheet](https://github.com/inforion/idapython-cheatsheet) Scripts and cheatsheets for IDAPython




***


## <a id="846eebe73bef533041d74fc711cafb43"></a>指令参考&文档


- [**493**星][11mo] [PLpgSQL][nologic/idaref](https://github.com/nologic/idaref) 指令参考插件.
- [**441**星][3mo] [C++][alexhude/friend](https://github.com/alexhude/friend) 反汇编显示增强, 文档增强插件
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
- [**240**星][2y] [Python][gdelugre/ida-arm-system-highlight](https://github.com/gdelugre/ida-arm-system-highlight) 用于高亮和解码 ARM 系统指令
- [**103**星][2w] [Python][neatmonster/amie](https://github.com/neatmonster/amie) 针对ARM架构的`FRIEND`插件, 文档增强
- [**45**星][8y] [Python][zynamics/msdn-plugin-ida](https://github.com/zynamics/msdn-plugin-ida) Imports MSDN documentation into IDA Pro
- [**25**星][3y] [AutoIt][yaseralnajjar/ida-msdn-helper](https://github.com/yaseralnajjar/IDA-MSDN-helper) IDA Pro MSDN Helper


***


## <a id="c08ebe5b7eec9fc96f8eff36d1d5cc7d"></a>辅助脚本编写


### <a id="45fd7cfce682c7c25b4f3fbc4c461ba2"></a>未分类


- [**382**星][3y] [Python][36hours/idaemu](https://github.com/36hours/idaemu) 基于Unicorn引擎的代码模拟插件
    - 重复区段: [工具/模拟器集成](#b38dab81610be087bd5bc7785269b8cc) |
- [**266**星][2mo] [Python][fireeye/flare-emu](https://github.com/fireeye/flare-emu) 结合Unicorn引擎, 简化模拟脚本的编写
    - 重复区段: [工具/模拟器集成](#b38dab81610be087bd5bc7785269b8cc) |
- [**134**星][] [Python][arizvisa/ida-minsc](https://github.com/arizvisa/ida-minsc) IDA-minsc is a plugin for IDA Pro that assists a user with scripting the IDAPython plugin that is bundled with the disassembler. This plugin groups the different aspects of the IDAPython API into a simpler format which allows a reverse engineer to script aspects of their work with very little investment. Smash that "Star" button if you like this.
- [**97**星][2w] [Python][patois/idapyhelper](https://github.com/patois/idapyhelper) IDAPython脚本编写辅助
- [**74**星][3mo] [C++][0xeb/ida-qscripts](https://github.com/0xeb/ida-qscripts) IDA“最近脚本/执行脚本”的进化版
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
- [**42**星][4mo] [C++][0xeb/ida-climacros](https://github.com/0xeb/ida-climacros) 在IDA命令行接口中定义和使用静态/动态的宏
- [**32**星][2y] [CMake][zyantific/ida-cmake](https://github.com/zyantific/ida-cmake) 使用CMake编译C++编写的IDA脚本
- [**22**星][1y] [Python][nirizr/idasix](https://github.com/nirizr/idasix) IDAPython兼容库。创建平滑的IDA开发流程，使相同代码可应用于多个IDA/IDAPython版本
- [**4**星][6mo] [inndy/idapython-cheatsheet](https://github.com/inndy/idapython-cheatsheet) scripting IDA like a Pro


### <a id="1a56a5b726aaa55ec5b7a5087d6c8968"></a>Qt


- [**25**星][11mo] [techbliss/ida_pro_ultimate_qt_build_guide](https://github.com/techbliss/ida_pro_ultimate_qt_build_guide) Ida Pro Ultimate Qt Build Guide
- [**13**星][1mo] [Python][tmr232/cute](https://github.com/tmr232/cute) 在IDAPython中兼容QT4/QT5
- [**9**星][3y] [Python][techbliss/ida_pro_screen_recorder](https://github.com/techbliss/ida_pro_screen_recorder) PyQt plugin for Ida Pro for Screen recording.


### <a id="1721c09501e4defed9eaa78b8d708361"></a>控制台&&窗口界面


- [**258**星][1w] [Python][eset/ipyida](https://github.com/eset/ipyida) 集成IPython控制台
- [**231**星][2y] [Jupyter Notebook][james91b/ida_ipython](https://github.com/james91b/ida_ipython) 嵌入IPython内核，集成IPython
- [**175**星][3mo] [Python][techbliss/python_editor](https://github.com/techbliss/python_editor) Python脚本编辑窗口


### <a id="227fbff77e3a13569ef7b007344d5d2e"></a>插件模板


- [**5**星][2y] [C++][patois/ida_vs2017](https://github.com/patois/ida_vs2017) IDA 7.x VS 2017 项目模板
- [**4**星][5y] [JavaScript][nihilus/ida-pro-plugin-wizard-for-vs2013](https://github.com/nihilus/ida-pro-plugin-wizard-for-vs2013) None


### <a id="8b19bb8cf9a5bc9e6ab045f3b4fabf6a"></a>其他语言


- [**20**星][3y] [Java][cblichmann/idajava](https://github.com/cblichmann/idajava) Java integration for Hex-Rays IDA Pro
- [**8**星][3y] [C++][nlitsme/idaperl](https://github.com/nlitsme/idaperl) 在IDA中使用Perl编写脚本




***


## <a id="e3e7030efc3b4de3b5b8750b7d93e6dd"></a>调试&&动态运行&动态数据


### <a id="2944dda5289f494e5e636089db0d6a6a"></a>未分类


- [**388**星][11mo] [C++][cseagle/sk3wldbg](https://github.com/cseagle/sk3wldbg) 用Unicorn引擎做后端的调试插件
    - 重复区段: [工具/模拟器集成](#b38dab81610be087bd5bc7785269b8cc) |
- [**184**星][5y] [C++][nihilus/scyllahide](https://github.com/nihilus/scyllahide) 用户模式反-反调试
- [**102**星][1mo] [Python][danielplohmann/apiscout](https://github.com/danielplohmann/apiscout) 简化导入API恢复。可以从内存中恢复API信息。包含命令行版本和IDA插件。可以处理PE头被抹掉等ImpRec/ImpRec无法处理的情况。
- [**81**星][4y] [C++][wjp/idados](https://github.com/wjp/idados) DOSBox调试器插件
    - 重复区段: [工具/针对特定分析目标/未分类](#5578c56ca09a5804433524047840980e) |
- [**56**星][7y] [Python][cr4sh/ida-vmware-gdb](https://github.com/cr4sh/ida-vmware-gdb) 辅助Windows内核调试
- [**42**星][5y] [Python][nihilus/idasimulator](https://github.com/nihilus/idasimulator) 扩展IDA的条件断点支持，在被调试进行中使用Python代码替换复杂的执行代码
- [**38**星][2y] [Python][thecjw/ida_android_script](https://github.com/thecjw/ida_android_script) 辅助Android调试的IDAPython脚本
    - 重复区段: [工具/Android](#66052f824f5054aa0f70785a2389a478) |
- [**22**星][5y] [Python][techbliss/scylladumper](https://github.com/techbliss/scylladumper) Ida Plugin to Use the Awsome Scylla plugin
- [**14**星][5y] [Python][techbliss/free_the_debuggers](https://github.com/techbliss/free_the_debuggers) 自动加载并执行调试器插件？？
- [**0**星][2y] [Python][benh11235/ida-windbglue](https://github.com/benh11235/ida-windbglue) 与远程WinDBG调试服务器进行连接的"胶水"脚本


### <a id="0fbd352f703b507853c610a664f024d1"></a>DBI数据


- [**923**星][11mo] [Python][gaasedelen/lighthouse](https://github.com/gaasedelen/lighthouse) 从DBI中收集代码覆盖情况，在IDA/Binja中映射、浏览、查看
    - [coverage-frida](https://github.com/gaasedelen/lighthouse/blob/master/coverage/frida/README.md) 使用Frida收集信息
    - [coverage-pin](https://github.com/gaasedelen/lighthouse/blob/master/coverage/pin/README.md) 使用Pin收集覆盖信息
    - [插件](https://github.com/gaasedelen/lighthouse/blob/master/plugin/lighthouse_plugin.py) 支持IDA和BinNinja
- [**133**星][1y] [Python][carlosgprado/jarvis](https://github.com/carlosgprado/jarvis) 多功能, 带界面,辅助静态分析、漏洞挖掘、动态追踪(Pin)、导入导出等
    - 重复区段: [工具/导入导出&与其他工具交互/IntelPin](#dd0332da5a1482df414658250e6357f8) |[工具/漏洞/未分类](#385d6777d0747e79cccab0a19fa90e7e) |
    - [IDA插件](https://github.com/carlosgprado/jarvis/tree/master/IDAPlugin) 
    - [PinTracer](https://github.com/carlosgprado/jarvis/tree/master/PinTracer) 
- [**129**星][3y] [Python][friedappleteam/frapl](https://github.com/friedappleteam/frapl) 在Frida Client和IDA之间建立连接，将运行时信息直接导入IDA，并可直接在IDA中控制Frida
    - 重复区段: [工具/导入导出&与其他工具交互/Frida](#a1cf7f7f849b4ca2101bd31449c2a0fd) |
    - [IDA插件](https://github.com/FriedAppleTeam/FRAPL/tree/master/Framework/FridaLink) 
    - [Frida脚本](https://github.com/FriedAppleTeam/FRAPL/tree/master/Framework/FRAPL) 
- [**121**星][5y] [C++][zachriggle/ida-splode](https://github.com/zachriggle/ida-splode) 使用Pin收集动态运行数据, 导入到IDA中查看
    - [IDA插件](https://github.com/zachriggle/ida-splode/tree/master/py) 
    - [PinTool](https://github.com/zachriggle/ida-splode/tree/master/src) 
- [**116**星][2y] [C++][0xphoenix/mazewalker](https://github.com/0xphoenix/mazewalker) 使用Pin收集数据，导入到IDA中查看
    - [mazeui](https://github.com/0xphoenix/mazewalker/blob/master/MazeUI/mazeui.py) 在IDA中显示界面
    - [PyScripts](https://github.com/0xPhoeniX/MazeWalker/tree/master/MazeTracer/PyScripts) Python脚本，处理收集到的数据
    - [PinClient](https://github.com/0xPhoeniX/MazeWalker/tree/master/MazeTracer/src) 
- [**88**星][8y] [C][neuroo/runtime-tracer](https://github.com/neuroo/runtime-tracer) 使用Pin收集运行数据并在IDA中显示
    - [PinTool](https://github.com/neuroo/runtime-tracer/tree/master/tracer) 
    - [IDA插件](https://github.com/neuroo/runtime-tracer/tree/master/ida-pin) 
- [**79**星][3y] [Python][davidkorczynski/repeconstruct](https://github.com/davidkorczynski/repeconstruct) 自动脱壳并重建二进制文件
- [**51**星][10mo] [Python][cisco-talos/dyndataresolver](https://github.com/cisco-talos/dyndataresolver) 动态数据解析: 在IDA中控制DyRIO执行程序的指定部分, 记录执行过程后传回数据到IDA
    - [DDR](https://github.com/cisco-talos/dyndataresolver/blob/master/VS_project/ddr/ddr.sln) 基于DyRIO的Client
    - [IDA插件](https://github.com/cisco-talos/dyndataresolver/tree/master/IDAplugin) 
- [**20**星][8mo] [C++][secrary/findloop](https://github.com/secrary/findloop) 使用DyRIO查找执行次数过多的代码块
- [**15**星][11mo] [C++][agustingianni/instrumentation](https://github.com/agustingianni/instrumentation) PinTool收集。收集数据可导入到IDA中
    - [CodeCoverage](https://github.com/agustingianni/instrumentation/tree/master/CodeCoverage) 
    - [Pinnacle](https://github.com/agustingianni/instrumentation/tree/master/Pinnacle) 
    - [Recoverer](https://github.com/agustingianni/instrumentation/tree/master/Recoverer) 
    - [Resolver](https://github.com/agustingianni/instrumentation/tree/master/Resolver) 


### <a id="b31acf6c84a9506066d497af4e702bf5"></a>调试数据


- [**591**星][2mo] [Python][0xgalz/virtuailor](https://github.com/0xgalz/virtuailor) 利用IDA调试获取的信息，自动创建C++的虚表
    - 重复区段: [工具/结构体&&类的检测&&创建&&恢复/C++类&&虚表](#4900b1626f10791748b20630af6d6123) |
        <details>
        <summary>查看详情</summary>


        ## 静态部分: 
        - 检测非直接调用
        - 利用条件断点, Hook非直接调用的值赋值过程
        
        ## 动态 部分
        - 创建虚表结构
        - 重命名函数和虚表地址
        - 给反汇编非直接调用添加结构偏移
        - 给非直接调用到虚表之间添加交叉引用
        
        ## 使用
        - File -> Script File -> Main.py(设置断点) -> IDA调试器执行
        </details>


- [**383**星][4mo] [Python][ynvb/die](https://github.com/ynvb/die) 使用IDA调试器收集动态运行信息, 辅助静态分析
- [**378**星][4y] [Python][deresz/funcap](https://github.com/deresz/funcap) 使用IDA调试时记录动态信息, 辅助静态分析
- [**103**星][3y] [Python][c0demap/codemap](https://github.com/c0demap/codemap) Hook IDA，调试命中断点时将寄存器/内存信息保存到数据库，在web浏览器中查看
    - [IDA插件](https://github.com/c0demap/codemap/blob/master/idapythonrc.py) 
    - [Web服务器](https://github.com/c0demap/codemap/tree/master/codemap/server) 




***


## <a id="d2166f4dac4eab7fadfe0fd06467fbc9"></a>反编译器&&AST


- [**1660**星][6mo] [C++][yegord/snowman](https://github.com/yegord/snowman) Snowman反编译器，支持x86, AMD64, ARM。有独立的GUI工具、命令行工具、IDA/Radare2/x64dbg插件，也可以作为库使用
    - [IDA插件](https://github.com/yegord/snowman/tree/master/src/ida-plugin) 
    - [snowman](https://github.com/yegord/snowman/tree/master/src/snowman) QT界面
    - [nocode](https://github.com/yegord/snowman/tree/master/src/nocode) 命令行工具
    - [nc](https://github.com/yegord/snowman/tree/master/src/nc) 核心代码，可作为库使用
- [**1312**星][1y] [C++][rehints/hexrayscodexplorer](https://github.com/rehints/hexrayscodexplorer) 反编译插件, 多功能
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
        <details>
        <summary>查看详情</summary>


        - 自动类型重建
        - 虚表识别/导航(反编译窗口)
        - C-tree可视化与导出
        - 对象浏览
        </details>


- [**465**星][4y] [Python][einstein-/decompiler](https://github.com/EiNSTeiN-/decompiler) 多后端的反编译器, 支持IDA和Capstone.
- [**399**星][2mo] [C++][avast/retdec-idaplugin](https://github.com/avast/retdec-idaplugin) retdec 的 IDA 插件
- [**291**星][5y] [C++][smartdec/smartdec](https://github.com/smartdec/smartdec) 反编译器, 带IDA插件(进阶版为: snowman)
    - [IDA插件](https://github.com/smartdec/smartdec/tree/master/src/ida-plugin) 
    - [nocode](https://github.com/smartdec/smartdec/tree/master/src/nocode) 命令行反编译器
    - [smartdec](https://github.com/smartdec/smartdec/tree/master/src/smartdec) 带GUI界面的反编译器
    - [nc](https://github.com/smartdec/smartdec/tree/master/src/nc) 反编译器的核心代码
- [**286**星][5y] [Python][aaronportnoy/toolbag](https://github.com/aaronportnoy/toolbag) 反编译强化插件
- [**222**星][6mo] [Python][patois/dsync](https://github.com/patois/dsync) 反汇编和反编译窗口同步插件
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
- [**167**星][1y] [Python][tintinweb/ida-batch_decompile](https://github.com/tintinweb/ida-batch_decompile) 将多个文件及其import用附加注释（外部参照，堆栈变量大小）反编译到pseudocode.c文件
- [**148**星][1y] [Python][ax330d/hrdev](https://github.com/ax330d/hrdev) 反编译输出增强: 使用Python Clang解析标准的IDA反编译结果
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /显示增强](#03fac5b3abdbd56974894a261ce4e25f) |
- [**103**星][7mo] [Python][sibears/hrast](https://github.com/sibears/hrast) 演示如何修改AST(抽象语法树)
- [**89**星][5mo] [Python][patois/hrdevhelper](https://github.com/patois/hrdevhelper) 反编译函数CTree可视化
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /显示增强](#03fac5b3abdbd56974894a261ce4e25f) |
- [**41**星][2w] [Python][patois/mrspicky](https://github.com/patois/mrspicky) IDA反编译器脚本，辅助审计对于memcpy() 和memmove()函数的调用
    - 重复区段: [工具/漏洞/未分类](#385d6777d0747e79cccab0a19fa90e7e) |
- [**23**星][1y] [C++][dougallj/dj_ida_plugins](https://github.com/dougallj/dj_ida_plugins) 向Hex-Rays反编译器添加VMX intrinsics


***


## <a id="7199e8787c0de5b428f50263f965fda7"></a>反混淆


- [**1338**星][1mo] [Python][fireeye/flare-floss](https://github.com/fireeye/flare-floss) 自动从恶意代码中提取反混淆后的字符串
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |
    - [floss](https://github.com/fireeye/flare-floss/tree/master/floss) 
    - [IDA插件](https://github.com/fireeye/flare-floss/blob/master/scripts/idaplugin.py) 
- [**537**星][2y] [Python][anatolikalysch/vmattack](https://github.com/anatolikalysch/vmattack) 基于虚拟化的壳的分析(静态/动态)与反混淆
    - 重复区段: [工具/针对特定分析目标/未分类](#5578c56ca09a5804433524047840980e) |
- [**285**星][3mo] [C++][rolfrolles/hexraysdeob](https://github.com/rolfrolles/hexraysdeob) 利用Hex-Rays microcode API破解编译器级别的混淆
    - 重复区段: [工具/Microcode](#7a2977533ccdac70ee6e58a7853b756b) |
- [**201**星][2y] [Python][tkmru/nao](https://github.com/tkmru/nao) 移除死代码(dead code), 基于Unicorn引擎
    - 重复区段: [工具/模拟器集成](#b38dab81610be087bd5bc7785269b8cc) |
- [**47**星][2y] [Python][riscure/drop-ida-plugin](https://github.com/riscure/drop-ida-plugin) Experimental opaque predicate detection for IDA Pro
- [**22**星][3mo] [Python][jonathansalwan/x-tunnel-opaque-predicates](https://github.com/jonathansalwan/x-tunnel-opaque-predicates) IDA+Triton plugin in order to extract opaque predicates using a Forward-Bounded DSE. Example with X-Tunnel.
    - 重复区段: [工具/污点分析&&符号执行](#34ac84853604a7741c61670f2a075d20) |
- [**8**星][3y] [Python][thngkaiyuan/mynaim](https://github.com/thngkaiyuan/mynaim) Nymaim 家族样本反混淆插件
    - 重复区段: [工具/针对特定分析目标/特定样本家族](#841d605300beba45c3be131988514a03) |


***


## <a id="fcf75a0881617d1f684bc8b359c684d7"></a>效率&&导航&&快速访问&&图形&&图像&&可视化 


### <a id="c5b120e1779b928d860ad64ff8d23264"></a>其他


- [**1312**星][1y] [C++][rehints/hexrayscodexplorer](https://github.com/rehints/hexrayscodexplorer) 反编译插件, 多功能
    - 重复区段: [工具/反编译器&&AST](#d2166f4dac4eab7fadfe0fd06467fbc9) |
        <details>
        <summary>查看详情</summary>


        - 自动类型重建
        - 虚表识别/导航(反编译窗口)
        - C-tree可视化与导出
        - 对象浏览
        </details>


- [**441**星][3mo] [C++][alexhude/friend](https://github.com/alexhude/friend) 反汇编显示增强, 文档增强插件
    - 重复区段: [工具/指令参考&文档](#846eebe73bef533041d74fc711cafb43) |
- [**362**星][4w] [Python][l4ys/lazyida](https://github.com/l4ys/lazyida) 若干快速访问功能, 扫描字符串格式化漏洞
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |[工具/漏洞/未分类](#385d6777d0747e79cccab0a19fa90e7e) |
        <details>
        <summary>查看详情</summary>


        ### 功能
        - 快速移除函数返回类型
        - 数据格式(format)快速转换
        - 扫描字符串格式化漏洞
        - 双击跳转vtable函数
        - 快捷键: w/c/v
        </details>


- [**325**星][2mo] [Python][pfalcon/scratchabit](https://github.com/pfalcon/scratchabit) 交互式反汇编工具, 有与IDAPython兼容的插件API
- [**222**星][6mo] [Python][patois/dsync](https://github.com/patois/dsync) 反汇编和反编译窗口同步插件
    - 重复区段: [工具/反编译器&&AST](#d2166f4dac4eab7fadfe0fd06467fbc9) |
- [**181**星][2w] [Python][danigargu/dereferencing](https://github.com/danigargu/dereferencing) 调试时寄存器和栈显示增强
- [**130**星][2y] [Python][comsecuris/ida_strcluster](https://github.com/comsecuris/ida_strcluster) 扩展IDA的字符串导航功能
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |
- [**98**星][1y] [Python][darx0r/stingray](https://github.com/darx0r/stingray) 递归查找函数和字符串
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |[工具/函数相关/导航&&查看&&查找](#e4616c414c24b58626f834e1be079ebc) |
- [**80**星][1y] [Python][ax330d/functions-plus](https://github.com/ax330d/functions-plus) 解析函数名称，按命名空间分组，将分组结果以树的形式展示
    - 重复区段: [工具/函数相关/导航&&查看&&查找](#e4616c414c24b58626f834e1be079ebc) |
- [**74**星][3mo] [C++][0xeb/ida-qscripts](https://github.com/0xeb/ida-qscripts) IDA“最近脚本/执行脚本”的进化版
    - 重复区段: [工具/辅助脚本编写/未分类](#45fd7cfce682c7c25b4f3fbc4c461ba2) |
- [**48**星][2mo] [C++][jinmo/ifred](https://github.com/jinmo/ifred) IDA command palette & more (Ctrl+Shift+P, Ctrl+P)
- [**40**星][3mo] [Python][tmr232/brutal-ida](https://github.com/tmr232/brutal-ida) 在IDA 7.3中禁用Undo/Redo
- [**23**星][6y] [C++][cr4sh/ida-ubigraph](https://github.com/cr4sh/ida-ubigraph) IDA Pro plug-in and tools for displaying 3D graphs of procedures using UbiGraph
- [**17**星][2y] [Python][tmr232/graphgrabber](https://github.com/tmr232/graphgrabber) 获取IDA图的全分辨率图像
- [**5**星][2y] [Python][handsomematt/ida_func_ptr](https://github.com/handsomematt/ida_func_ptr) 右键菜单中快速拷贝函数指针定义


### <a id="03fac5b3abdbd56974894a261ce4e25f"></a>显示增强


- [**200**星][4w] [Python][patois/idacyber](https://github.com/patois/idacyber) 交互式数据可视化插件
- [**148**星][1y] [Python][ax330d/hrdev](https://github.com/ax330d/hrdev) 反编译输出增强: 使用Python Clang解析标准的IDA反编译结果
    - 重复区段: [工具/反编译器&&AST](#d2166f4dac4eab7fadfe0fd06467fbc9) |
- [**103**星][2y] [Python][danigargu/idatropy](https://github.com/danigargu/idatropy) 使用idapython和matplotlib的功能生成熵和直方图的图表
- [**89**星][5mo] [Python][patois/hrdevhelper](https://github.com/patois/hrdevhelper) 反编译函数CTree可视化
    - 重复区段: [工具/反编译器&&AST](#d2166f4dac4eab7fadfe0fd06467fbc9) |
- [**47**星][4w] [Python][patois/xray](https://github.com/patois/xray) 根据正则表达式对IDA反编译输出的特定内容进行高亮显示
- [**20**星][3mo] [C++][revspbird/hightlight](https://github.com/revspbird/hightlight) 反编译窗口中代码块和括号高亮
- [**5**星][3y] [Python][oct0xor/ida_pro_graph_styling](https://github.com/oct0xor/ida_pro_graph_styling) call/jump指令高亮显示
- [**5**星][1y] [C][teppay/ida](https://github.com/teppay/ida) 指令高亮，黑色主题
- [**4**星][2y] [Python][andreafioraldi/idaretaddr](https://github.com/andreafioraldi/idaretaddr) 在IDA调试器中高亮函数的返回地址
    - 重复区段: [工具/函数相关/未分类](#347a2158bdd92b00cd3d4ba9a0be00ae) |


### <a id="3b1dba00630ce81cba525eea8fcdae08"></a>图形&&图像


- [**2560**星][4mo] [Java][google/binnavi](https://github.com/google/binnavi) 二进制分析IDE, 对反汇编代码的控制流程图和调用图进行探查/导航/编辑/注释.(IDA插件的作用是导出反汇编)
- [**231**星][2y] [C++][fireeye/simplifygraph](https://github.com/fireeye/simplifygraph) 复杂graphs的简化
- [**39**星][8mo] [Python][rr-/ida-images](https://github.com/rr-/ida-images) 图像预览插件，辅助查找图像解码函数（运行复杂代码，查看内存中是否存在图像）


### <a id="8f9468e9ab26128567f4be87ead108d7"></a>搜索


- [**149**星][2y] [Python][ga-ryo/idafuzzy](https://github.com/ga-ryo/idafuzzy) 模糊搜索: 命令/函数/结构体
    - 重复区段: [工具/函数相关/导航&&查看&&查找](#e4616c414c24b58626f834e1be079ebc) |
- [**64**星][3y] [Python][xorpd/idsearch](https://github.com/xorpd/idsearch) 搜索工具
- [**23**星][4mo] [Python][alexander-hanel/hansel](https://github.com/alexander-hanel/hansel) IDA搜索插件




***


## <a id="66052f824f5054aa0f70785a2389a478"></a>Android


- [**221**星][2y] [Python][strazzere/android-scripts](https://github.com/strazzere/android-scripts) Android逆向脚本收集
- [**158**星][4w] [Python][nforest/droidimg](https://github.com/nforest/droidimg) Android/Linux vmlinux loader
    - 重复区段: [工具/ELF](#e5e403123c70ddae7bd904d3a3005dbb) |[工具/针对特定分析目标/Loader&Processor](#cb59d84840e41330a7b5e275c0b81725) |
- [**115**星][4y] [Python][cvvt/dumpdex](https://github.com/cvvt/dumpdex) 基于IDA python的Android DEX内存dump工具
- [**79**星][2y] [Python][zhkl0228/androidattacher](https://github.com/zhkl0228/androidattacher) IDA debugging plugin for android armv7 so
- [**39**星][5y] [Python][techbliss/adb_helper_qt_super_version](https://github.com/techbliss/adb_helper_qt_super_version) All You Need For Ida Pro And Android Debugging
- [**38**星][2y] [Python][thecjw/ida_android_script](https://github.com/thecjw/ida_android_script) 辅助Android调试的IDAPython脚本
    - 重复区段: [工具/调试&&动态运行&动态数据/未分类](#2944dda5289f494e5e636089db0d6a6a) |
- [**16**星][7y] [C++][strazzere/dalvik-header-plugin](https://github.com/strazzere/dalvik-header-plugin) Dalvik Header Plugin for IDA Pro


***


## <a id="2adc0044b2703fb010b3bf73b1f1ea4a"></a>Apple&&macOS&&iXxx&&Objective-C&&SWift&&Mach-O


### <a id="8530752bacfb388f3726555dc121cb1a"></a>未分类


- [**172**星][2y] [Python][duo-labs/idapython](https://github.com/duo-labs/idapython) Duo 实验室使用的IDAPython 脚本收集
    - 重复区段: [工具/固件&&嵌入式设备](#a8f5db3ab4bc7bc3d6ca772b3b9b0b1e) |
    - [cortex_m_firmware](https://github.com/duo-labs/idapython/blob/master/cortex_m_firmware.py)  整理包含ARM Cortex M微控制器固件的IDA Pro数据库
    - [amnesia](https://github.com/duo-labs/idapython/blob/master/amnesia.py) 使用字节级启发式在IDA Pro数据库中的未定义字节中查找ARM Thumb指令
    - [REobjc](https://github.com/duo-labs/idapython/blob/master/reobjc.py) 在Objective-C的调用函数和被调用函数之间进行适当的交叉引用
- [**167**星][8y] [Python][zynamics/objc-helper-plugin-ida](https://github.com/zynamics/objc-helper-plugin-ida) 辅助Objective-C二进制文件的分析
- [**18**星][2y] [aozhimin/ios-monitor-resources](https://github.com/aozhimin/ios-monitor-resources) 对各厂商的 iOS SDK 性能监控方案的整理和收集后的资源
- [**17**星][9y] [C++][alexander-pick/patchdiff2_ida6](https://github.com/alexander-pick/patchdiff2_ida6) patched up patchdiff2 to compile and work with IDA 6 on OSX
- [**14**星][7y] [Standard ML][letsunlockiphone/iphone-baseband-ida-pro-signature-files](https://github.com/letsunlockiphone/iphone-baseband-ida-pro-signature-files) IDA签名文件，iPhone基带逆向
    - 重复区段: [工具/签名(FLIRT等)&&比较(Diff)&&匹配/未分类](#cf04b98ea9da0056c055e2050da980c1) |


### <a id="82d0fa2d6934ce29794a651513934384"></a>内核缓存


- [**168**星][12mo] [Python][bazad/ida_kernelcache](https://github.com/bazad/ida_kernelcache) 使用IDA Pro重建iOS内核缓存的C++类
    - 重复区段: [工具/结构体&&类的检测&&创建&&恢复/未分类](#fa5ede9a4f58d4efd98585d3158be4fb) |
- [**137**星][8y] [stefanesser/ida-ios-toolkit](https://github.com/stefanesser/ida-ios-toolkit) 辅助处理iOS kernelcache的IDAPython收集
- [**50**星][1y] [Python][synacktiv-contrib/kernelcache-laundering](https://github.com/Synacktiv-contrib/kernelcache-laundering) load iOS12 kernelcaches and PAC code in IDA


### <a id="d249a8d09a3f25d75bb7ba8b32bd9ec5"></a>Mach-O


- [**47**星][6mo] [C][gdbinit/extractmacho](https://github.com/gdbinit/extractmacho) IDA plugin to extract Mach-O binaries located in the disassembly or data
- [**18**星][3y] [C][cocoahuke/iosdumpkernelfix](https://github.com/cocoahuke/iosdumpkernelfix) This tool will help to fix the Mach-O header of iOS kernel which dump from the memory. So that IDA or function symbol-related tools can loaded function symbols of ios kernel correctly
- [**17**星][8y] [C][gdbinit/machoplugin](https://github.com/gdbinit/machoplugin) IDA plugin to Display Mach-O headers


### <a id="1c698e298f6112a86c12881fbd8173c7"></a>Swift


- [**17**星][3y] [Python][tylerha97/swiftdemang](https://github.com/0xtyh/swiftdemang) Demangle Swift
- [**17**星][4y] [Python][gsingh93/ida-swift-demangle](https://github.com/gsingh93/ida-swift-demangle) 对Swift函数名进行demangle
    - 重复区段: [工具/函数相关/demangle](#cadae88b91a57345d266c68383eb05c5) |




***


## <a id="e5e403123c70ddae7bd904d3a3005dbb"></a>ELF


- [**517**星][2y] [C][lunixbochs/patchkit](https://github.com/lunixbochs/patchkit) 给ELF文件打补丁(命令行+IDA插件)(可编写Python回调,C函数替换等)
    - 重复区段: [工具/补丁&&Patch](#7d557bc3d677d206ef6c5a35ca8b3a14) |
    - [IDA插件](https://github.com/lunixbochs/patchkit/tree/master/ida) 
    - [patchkit](https://github.com/lunixbochs/patchkit/tree/master/core) 
- [**201**星][5y] [C][snare/ida-efiutils](https://github.com/snare/ida-efiutils) 辅助ELF逆向
- [**158**星][4w] [Python][nforest/droidimg](https://github.com/nforest/droidimg) Android/Linux vmlinux loader
    - 重复区段: [工具/Android](#66052f824f5054aa0f70785a2389a478) |[工具/针对特定分析目标/Loader&Processor](#cb59d84840e41330a7b5e275c0b81725) |
- [**125**星][7mo] [Python][danigargu/syms2elf](https://github.com/danigargu/syms2elf) 将IDA Pro和Radare2识别的符号（目前仅函数）导出到ELF符号表
    - 重复区段: [工具/导入导出&与其他工具交互/Radare2](#21ed198ae5a974877d7a635a4b039ae3) |[工具/函数相关/未分类](#347a2158bdd92b00cd3d4ba9a0be00ae) |
- [**90**星][2y] [C++][gdbinit/efiswissknife](https://github.com/gdbinit/efiswissknife) 辅助 (U)EFI reversing 逆向
- [**83**星][2mo] [Python][yeggor/uefi_retool](https://github.com/yeggor/uefi_retool) 在UEFI固件和UEFI模块分析中查找专有协议的工具
- [**44**星][2y] [C][aerosoul94/dynlib](https://github.com/aerosoul94/dynlib) 辅助PS4用户模式ELF逆向
    - 重复区段: [工具/针对特定分析目标/PS3&&PS4](#315b1b8b41c67ae91b841fce1d4190b5) |
- [**44**星][4y] [Python][danse-macabre/ida-efitools](https://github.com/danse-macabre/ida-efitools) 辅助逆向ELF文件
- [**42**星][4y] [Python][strazzere/idant-wanna](https://github.com/strazzere/idant-wanna) ELF header abuse


***


## <a id="7a2977533ccdac70ee6e58a7853b756b"></a>Microcode


- [**285**星][3mo] [C++][rolfrolles/hexraysdeob](https://github.com/rolfrolles/hexraysdeob) 利用Hex-Rays microcode API破解编译器级别的混淆
    - 重复区段: [工具/反混淆](#7199e8787c0de5b428f50263f965fda7) |
- [**186**星][3mo] [C++][chrisps/hexext](https://github.com/chrisps/Hexext) 通过操作microcode, 优化反编译器的数据
- [**60**星][4mo] [Python][patois/genmc](https://github.com/patois/genmc) 显示Hex-Rays 反编译器的Microcode，辅助开发Microcode插件
- [**43**星][4w] [Python][idapython/pyhexraysdeob](https://github.com/idapython/pyhexraysdeob) 工具 RolfRolles/HexRaysDeob 的Python版本
- [**19**星][8mo] [Python][neatmonster/mcexplorer](https://github.com/neatmonster/mcexplorer) 工具 RolfRolles/HexRaysDeob 的 Python 版本


***


## <a id="b38dab81610be087bd5bc7785269b8cc"></a>模拟器集成


- [**475**星][11mo] [Python][alexhude/uemu](https://github.com/alexhude/uemu) 基于Unicorn的模拟器插件
- [**388**星][11mo] [C++][cseagle/sk3wldbg](https://github.com/cseagle/sk3wldbg) 用Unicorn引擎做后端的调试插件
    - 重复区段: [工具/调试&&动态运行&动态数据/未分类](#2944dda5289f494e5e636089db0d6a6a) |
- [**382**星][3y] [Python][36hours/idaemu](https://github.com/36hours/idaemu) 基于Unicorn引擎的代码模拟插件
    - 重复区段: [工具/辅助脚本编写/未分类](#45fd7cfce682c7c25b4f3fbc4c461ba2) |
- [**266**星][2mo] [Python][fireeye/flare-emu](https://github.com/fireeye/flare-emu) 结合Unicorn引擎, 简化模拟脚本的编写
    - 重复区段: [工具/辅助脚本编写/未分类](#45fd7cfce682c7c25b4f3fbc4c461ba2) |
- [**201**星][2y] [Python][tkmru/nao](https://github.com/tkmru/nao) 移除死代码(dead code), 基于Unicorn引擎
    - 重复区段: [工具/反混淆](#7199e8787c0de5b428f50263f965fda7) |
- [**124**星][2y] [Python][codypierce/pyemu](https://github.com/codypierce/pyemu) 在IDA中使用x86模拟器


***


## <a id="83de90385d03ac8ef27360bfcdc1ab48"></a>作为辅助&&构成其他的一环


- [**1506**星][3d] [Python][lifting-bits/mcsema](https://github.com/lifting-bits/mcsema) 将x86, amd64, aarch64二进制文件转换成LLVM字节码
    - [IDA7插件](https://github.com/lifting-bits/mcsema/tree/master/tools/mcsema_disass/ida7) 用于反汇编二进制文件并生成控制流程图
    - [IDA插件](https://github.com/lifting-bits/mcsema/tree/master/tools/mcsema_disass/ida) 用于反汇编二进制文件并生成控制流程图
    - [Binja插件](https://github.com/lifting-bits/mcsema/tree/master/tools/mcsema_disass/binja) 用于反汇编二进制文件并生成控制流程图
    - [mcsema](https://github.com/lifting-bits/mcsema/tree/master/mcsema) 
- [**415**星][2w] [C][mcgill-dmas/kam1n0-community](https://github.com/McGill-DMaS/Kam1n0-Community) 汇编代码管理与分析平台(独立工具+IDA插件)
    - 重复区段: [工具/签名(FLIRT等)&&比较(Diff)&&匹配/未分类](#cf04b98ea9da0056c055e2050da980c1) |
    - [IDA插件](https://github.com/McGill-DMaS/Kam1n0-Community/tree/master2.x/kam1n0-clients/ida-plugin) 
    - [kam1n0](https://github.com/McGill-DMaS/Kam1n0-Community/tree/master2.x/kam1n0) 
- [**27**星][4y] [Scheme][yifanlu/cgen](https://github.com/yifanlu/cgen) CGEN的Fork，增加了生成IDA IDP模块的支持
- [**23**星][2y] [Python][tintinweb/unbox](https://github.com/tintinweb/unbox) Unbox is a convenient one-click unpack and decompiler tool that wraps existing 3rd party applications like IDA Pro, JD-Cli, Dex2Src, and others to provide a convenient archiver liker command line interfaces to unpack and decompile various types of files


***


## <a id="1ded622dca60b67288a591351de16f8b"></a>漏洞


### <a id="385d6777d0747e79cccab0a19fa90e7e"></a>未分类


- [**485**星][6mo] [Python][danigargu/heap-viewer](https://github.com/danigargu/heap-viewer) 查看glibc堆, 主要用于漏洞开发
- [**376**星][2y] [Python][1111joe1111/ida_ea](https://github.com/1111joe1111/ida_ea) 用于辅助漏洞开发和逆向
- [**362**星][4w] [Python][l4ys/lazyida](https://github.com/l4ys/lazyida) 若干快速访问功能, 扫描字符串格式化漏洞
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |[工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
        <details>
        <summary>查看详情</summary>


        ### 功能
        - 快速移除函数返回类型
        - 数据格式(format)快速转换
        - 扫描字符串格式化漏洞
        - 双击跳转vtable函数
        - 快捷键: w/c/v
        </details>


- [**136**星][6mo] [Python][iphelix/ida-sploiter](https://github.com/iphelix/ida-sploiter) 辅助漏洞研究
- [**133**星][1y] [Python][carlosgprado/jarvis](https://github.com/carlosgprado/jarvis) 多功能, 带界面,辅助静态分析、漏洞挖掘、动态追踪(Pin)、导入导出等
    - 重复区段: [工具/导入导出&与其他工具交互/IntelPin](#dd0332da5a1482df414658250e6357f8) |[工具/调试&&动态运行&动态数据/DBI数据](#0fbd352f703b507853c610a664f024d1) |
    - [IDA插件](https://github.com/carlosgprado/jarvis/tree/master/IDAPlugin) 
    - [PinTracer](https://github.com/carlosgprado/jarvis/tree/master/PinTracer) 
- [**41**星][2w] [Python][patois/mrspicky](https://github.com/patois/mrspicky) IDA反编译器脚本，辅助审计对于memcpy() 和memmove()函数的调用
    - 重复区段: [工具/反编译器&&AST](#d2166f4dac4eab7fadfe0fd06467fbc9) |
- [**32**星][6y] [Python][coldheat/quicksec](https://github.com/coldheat/quicksec) IDAPython script for quick vulnerability analysis


### <a id="cf2efa7e3edb24975b92d2e26ca825d2"></a>ROP


- [**53**星][3y] [Python][patois/drgadget](https://github.com/patois/drgadget) 开发和分析ROP链
- [**19**星][1y] [Python][lucasg/idarop](https://github.com/lucasg/idarop) 列举并存储ROP gadgets




***


## <a id="7d557bc3d677d206ef6c5a35ca8b3a14"></a>补丁&&Patch


- [**710**星][11mo] [Python][keystone-engine/keypatch](https://github.com/keystone-engine/keypatch) 汇编/补丁插件, 支持多架构, 基于Keystone引擎
- [**517**星][2y] [C][lunixbochs/patchkit](https://github.com/lunixbochs/patchkit) 给ELF文件打补丁(命令行+IDA插件)(可编写Python回调,C函数替换等)
    - 重复区段: [工具/ELF](#e5e403123c70ddae7bd904d3a3005dbb) |
    - [IDA插件](https://github.com/lunixbochs/patchkit/tree/master/ida) 
    - [patchkit](https://github.com/lunixbochs/patchkit/tree/master/core) 
- [**87**星][5y] [Python][iphelix/ida-patcher](https://github.com/iphelix/ida-patcher) 二进制文件和内存补丁
- [**42**星][3y] [C++][mrexodia/idapatch](https://github.com/mrexodia/idapatch) IDA plugin to patch IDA Pro in memory.
- [**30**星][2mo] [Python][scottmudge/debugautopatch](https://github.com/scottmudge/debugautopatch) Patching system improvement plugin for IDA.
- [**16**星][8y] [C++][jkoppel/reprogram](https://github.com/jkoppel/reprogram) Patch binaries at load-time
- [**0**星][6mo] [Python][tkmru/genpatch](https://github.com/tkmru/genpatch) 生成用于打补丁的Python脚本


***


## <a id="90bf5d31a3897400ac07e15545d4be02"></a>函数相关


### <a id="347a2158bdd92b00cd3d4ba9a0be00ae"></a>未分类


- [**125**星][7mo] [Python][danigargu/syms2elf](https://github.com/danigargu/syms2elf) 将IDA Pro和Radare2识别的符号（目前仅函数）导出到ELF符号表
    - 重复区段: [工具/ELF](#e5e403123c70ddae7bd904d3a3005dbb) |[工具/导入导出&与其他工具交互/Radare2](#21ed198ae5a974877d7a635a4b039ae3) |
- [**10**星][2y] [C++][fireundubh/ida7-functionstringassociate](https://github.com/fireundubh/ida7-functionstringassociate) FunctionStringAssociate plugin by sirmabus, ported to IDA 7
- [**4**星][2y] [Python][andreafioraldi/idaretaddr](https://github.com/andreafioraldi/idaretaddr) 在IDA调试器中高亮函数的返回地址
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /显示增强](#03fac5b3abdbd56974894a261ce4e25f) |
- [**1**星][4mo] [Python][farzonl/idapropluginlab3](https://github.com/farzonl/idapropluginlab3) 通过静态分析使用的函数，描述恶意代码的行为


### <a id="73813456eeb8212fd45e0ea347bec349"></a>重命名&&前缀&&标记


- [**283**星][4w] [Python][a1ext/auto_re](https://github.com/a1ext/auto_re) 自动化函数重命名
- [**117**星][5y] [C++][zyantific/retypedef](https://github.com/zyantific/retypedef) 函数名称替换，可以自定义规则
- [**94**星][2y] [Python][gaasedelen/prefix](https://github.com/gaasedelen/prefix) IDA 插件，为函数添加前缀
- [**47**星][3y] [Python][alessandrogario/ida-function-tagger](https://github.com/alessandrogario/ida-function-tagger) 根据函数使用的导入表，对函数进行标记
- [**21**星][10mo] [Python][howmp/comfinder](https://github.com/howmp/comfinder) 查找标记COM组件中的函数
    - 重复区段: [工具/针对特定分析目标/未分类](#5578c56ca09a5804433524047840980e) |
- [**3**星][4y] [Python][ayuto/discover_win](https://github.com/ayuto/discover_win) 对比Linux和Windows二进制文件，对Windows文件未命名的函数进行自动重命名
    - 重复区段: [工具/签名(FLIRT等)&&比较(Diff)&&匹配/未分类](#cf04b98ea9da0056c055e2050da980c1) |


### <a id="e4616c414c24b58626f834e1be079ebc"></a>导航&&查看&&查找


- [**178**星][5mo] [Python][hasherezade/ida_ifl](https://github.com/hasherezade/ida_ifl) 交互式函数列表
- [**149**星][2y] [Python][ga-ryo/idafuzzy](https://github.com/ga-ryo/idafuzzy) 模糊搜索: 命令/函数/结构体
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /搜索](#8f9468e9ab26128567f4be87ead108d7) |
- [**98**星][1y] [Python][darx0r/stingray](https://github.com/darx0r/stingray) 递归查找函数和字符串
    - 重复区段: [工具/字符串](#9dcc6c7dd980bec1f92d0cc9a2209a24) |[工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
- [**80**星][1y] [Python][ax330d/functions-plus](https://github.com/ax330d/functions-plus) 解析函数名称，按命名空间分组，将分组结果以树的形式展示
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
- [**33**星][3y] [Python][darx0r/reef](https://github.com/darx0r/reef) 显示"由指定函数发起的"交叉应用。可以理解为函数内部引用的其他函数


### <a id="cadae88b91a57345d266c68383eb05c5"></a>demangle


- [**17**星][4y] [Python][gsingh93/ida-swift-demangle](https://github.com/gsingh93/ida-swift-demangle) 对Swift函数名进行demangle
    - 重复区段: [工具/Apple&&macOS&&iXxx&&Objective-C&&SWift&&Mach-O/Swift](#1c698e298f6112a86c12881fbd8173c7) |
- [**14**星][1y] [Python][ax330d/exports-plus](https://github.com/ax330d/exports-plus) 修复IDA不显示全部导出项以及不对导出项名称进行demangle的问题




***


## <a id="34ac84853604a7741c61670f2a075d20"></a>污点分析&&符号执行


- [**920**星][3d] [OCaml][airbus-seclab/bincat](https://github.com/airbus-seclab/bincat) 二进制代码静态分析工具。值分析（寄存器、内存）、污点分析、类型重建和传播（propagation）、前向/后向分析
    - 重复区段: [工具/结构体&&类的检测&&创建&&恢复/未分类](#fa5ede9a4f58d4efd98585d3158be4fb) |
- [**862**星][2y] [C++][illera88/ponce](https://github.com/illera88/ponce) 简化污点分析+符号执行
- [**22**星][3mo] [Python][jonathansalwan/x-tunnel-opaque-predicates](https://github.com/jonathansalwan/x-tunnel-opaque-predicates) IDA+Triton plugin in order to extract opaque predicates using a Forward-Bounded DSE. Example with X-Tunnel.
    - 重复区段: [工具/反混淆](#7199e8787c0de5b428f50263f965fda7) |


***


## <a id="7dfd8abad50c14cd6bdc8d8b79b6f595"></a>其他


- [**120**星][2y] [Shell][feicong/ida_for_mac_green](https://github.com/feicong/ida_for_mac_green) IDAPro 绿化增强版 （macOS）
- [**26**星][4mo] [angelkitty/ida7.0](https://github.com/angelkitty/ida7.0) 
- [**16**星][2y] [jas502n/ida7.0-pro](https://github.com/jas502n/ida7.0-pro) IDA7.0 下载


***


## <a id="9dcc6c7dd980bec1f92d0cc9a2209a24"></a>字符串


- [**1338**星][1mo] [Python][fireeye/flare-floss](https://github.com/fireeye/flare-floss) 自动从恶意代码中提取反混淆后的字符串
    - 重复区段: [工具/反混淆](#7199e8787c0de5b428f50263f965fda7) |
    - [floss](https://github.com/fireeye/flare-floss/tree/master/floss) 
    - [IDA插件](https://github.com/fireeye/flare-floss/blob/master/scripts/idaplugin.py) 
- [**362**星][4w] [Python][l4ys/lazyida](https://github.com/l4ys/lazyida) 若干快速访问功能, 扫描字符串格式化漏洞
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |[工具/漏洞/未分类](#385d6777d0747e79cccab0a19fa90e7e) |
        <details>
        <summary>查看详情</summary>


        ### 功能
        - 快速移除函数返回类型
        - 数据格式(format)快速转换
        - 扫描字符串格式化漏洞
        - 双击跳转vtable函数
        - 快捷键: w/c/v
        </details>


- [**177**星][4d] [Python][joxeankoret/idamagicstrings](https://github.com/joxeankoret/idamagicstrings) 从字符串常量中提取信息
- [**130**星][2y] [Python][comsecuris/ida_strcluster](https://github.com/comsecuris/ida_strcluster) 扩展IDA的字符串导航功能
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |
- [**98**星][1y] [Python][darx0r/stingray](https://github.com/darx0r/stingray) 递归查找函数和字符串
    - 重复区段: [工具/效率&&导航&&快速访问&&图形&&图像&&可视化 /其他](#c5b120e1779b928d860ad64ff8d23264) |[工具/函数相关/导航&&查看&&查找](#e4616c414c24b58626f834e1be079ebc) |
- [**45**星][5y] [Python][kyrus/ida-translator](https://github.com/kyrus/ida-translator) 将IDB数据库中的任意字符集转换为Unicode，然后自动调用基于网页的翻译服务（当前只有谷歌翻译）将非英文语言翻译为英文
- [**4**星][3y] [C#][andreafioraldi/idagrabstrings](https://github.com/andreafioraldi/idagrabstrings) 在指定地址区间内搜索字符串，并将其映射为C结构体
    - 重复区段: [工具/结构体&&类的检测&&创建&&恢复/未分类](#fa5ede9a4f58d4efd98585d3158be4fb) |
- [**4**星][7mo] [C][lacike/gandcrab_string_decryptor](https://github.com/lacike/gandcrab_string_decryptor) 解密 GandCrab v5.1-5.3 中的字符串
    - 重复区段: [工具/针对特定分析目标/特定样本家族](#841d605300beba45c3be131988514a03) |


***


## <a id="06d2caabef97cf663bd29af2b1fe270c"></a>加密解密


- [**418**星][2w] [Python][polymorf/findcrypt-yara](https://github.com/polymorf/findcrypt-yara) 使用Yara规则查找加密常量
    - 重复区段: [工具/签名(FLIRT等)&&比较(Diff)&&匹配/Yara](#46c9dfc585ae59fe5e6f7ddf542fb31a) |
- [**121**星][1mo] [Python][you0708/ida](https://github.com/you0708/ida) 查找加密常量
    - [IDA主题](https://github.com/you0708/ida/tree/master/theme) 
    - [findcrypt](https://github.com/you0708/ida/tree/master/idapython_tools/findcrypt) IDA FindCrypt/FindCrypt2 插件的Python版本
- [**41**星][6y] [C++][vlad902/findcrypt2-with-mmx](https://github.com/vlad902/findcrypt2-with-mmx) 对findcrypt2插件的增强，支持MMX AES指令


***


## <a id="dc35a2b02780cdaa8effcae2b6ce623e"></a>古老的


- [**163**星][4y] [Python][osirislab/fentanyl](https://github.com/osirislab/Fentanyl) 简化打补丁
- [**127**星][6y] [C++][crowdstrike/crowddetox](https://github.com/crowdstrike/crowddetox) None
- [**94**星][5y] [Python][nihilus/ida-idc-scripts](https://github.com/nihilus/ida-idc-scripts) 多个IDC脚本收集
- [**83**星][6y] [Python][einstein-/hexrays-python](https://github.com/einstein-/hexrays-python) Python bindings for the Hexrays Decompiler
- [**76**星][5y] [PHP][v0s/plus22](https://github.com/v0s/plus22) Tool to analyze 64-bit binaries with 32-bit Hex-Rays Decompiler
- [**63**星][5y] [C][nihilus/idastealth](https://github.com/nihilus/idastealth) None
- [**40**星][6y] [C++][wirepair/idapinlogger](https://github.com/wirepair/idapinlogger) Logs instruction hits to a file which can be fed into IDA Pro to highlight which instructions were called.
- [**39**星][10y] [izsh/ida-python-scripts](https://github.com/izsh/ida-python-scripts) IDA Python Scripts
- [**39**星][8y] [Python][zynamics/bincrowd-plugin-ida](https://github.com/zynamics/bincrowd-plugin-ida) BinCrowd Plugin for IDA Pro
- [**35**星][8y] [Python][zynamics/ida2sql-plugin-ida](https://github.com/zynamics/ida2sql-plugin-ida) None
- [**27**星][4y] [C++][luorui110120/idaplugins](https://github.com/luorui110120/idaplugins) 一堆IDA插件，无文档
- [**21**星][10y] [C++][sporst/ida-pro-plugins](https://github.com/sporst/ida-pro-plugins) Collection of IDA Pro plugins I wrote over the years
- [**18**星][10y] [Python][binrapt/ida](https://github.com/binrapt/ida) Python script which extracts procedures from IDA Win32 LST files and converts them to correctly dynamically linked compilable Visual C++ inline assembly.
- [**15**星][7y] [Python][nihilus/optimice](https://github.com/nihilus/optimice) None
- [**10**星][10y] [jeads-sec/etherannotate_ida](https://github.com/jeads-sec/etherannotate_ida) EtherAnnotate IDA Pro Plugin - Parse EtherAnnotate trace files and markup IDA disassemblies with runtime values
- [**6**星][10y] [C][jeads-sec/etherannotate_xen](https://github.com/jeads-sec/etherannotate_xen) EtherAnnotate Xen Ether Modification - Adds a feature to Ether that pulls register values and potential string values at each instruction during an instruction trace.


# <a id="35f8efcff18d0449029e9d3157ac0899"></a>TODO


- 对工具进行更细致的分类
- 为工具添加详细的中文描述，包括其内部实现原理和使用方式
- 添加非Github repo
- 添加文章


# <a id="18c6a45392d6b383ea24b363d2f3e76b"></a>文章


# 贡献
内容为系统自动导出, 有任何问题请提issue