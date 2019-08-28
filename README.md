# 2019BenBenPoemCorpus
some corpura sharing
关注微信公众号“笨笨”（微信号：benbenrobot），回复“笨笨古诗”或“笨笨古诗繁体”，可以互动喔
-
语料库来源：
-
    1.新课标初高中必背古诗，选取了其中一部分，来源于网络搜索
    2.Github开源语料库：
      https://github.com/hujiaweibujidao/poetry/tree/master/data/aio
    之后处理的语料库中，单句长度在9 - 20 之间，未加入元朝的诗词曲
    3.[正繁体转换参考]
      https://github.com/skydark/nstools/tree/master/zhtools

局限性：
-
    语料库仍存在一些错误，如果大家在运行时发现了错误，可以反馈到这个邮箱：l759490561@gmail.com
    
思路：
-
    参照《中国诗词大会》的题目形式：
    1.古诗带来的成语 module3_idiom
        笨笨显示一句含有成语的古诗，用户输入相应的成语，输入0退出此模式
    2.古诗九宫格(乱序重排) module2_sort
        笨笨将1句5言（7言）绝句乱序，添加一些干扰字，然后以3*3（4*3）字符阵输出，玩家输入排序后的诗句，输入0退出此模式
    3.古诗上下句默写/古诗填空 module1_gap_filling
        笨笨提示古诗上句（下句），用户输入下句（上句），输入0退出此模式(类似于中高考古诗填空题)
    4.诗词飞花令 module4_Feihualing
        玩家先输入一个汉字，之后和笨笨轮流说一句含有这个汉字的诗句，输入0退出此模式
    5.诗词接龙 module5_poem_string_up_puzzle
        玩家先输入一个汉字，之后笨笨和玩家轮流进行唐诗接龙，要求输入诗句的第一个字和的上一次屏幕显示诗句的最后一个字相同，
        笨笨先说,输入0退出此模式
    (输入格式要求：要求输入诗句的模块，诗句中间以逗号隔开，不输入结尾符号，不输入诗歌其他信息(诗人、朝代、诗名等))
    主函数界面：
        简单介绍，输入1 2 3 4 5分别进入相应子模块，输入其他退出
   

写代码的小结体会：
-
    1.在for遍历过程中不能remove：
      删除list内部信息，不能边遍历，边删，
      python的遍历只不过自动地加了下标，不是预备好了内容的遍历
    2.notepad++里面 ctrl + D 是翻倍同一行的效果
    3.list的extend 和 dist的upload 好用
    4.json很神奇
    5.语料的收集、处理还是很费功夫的
    6.先构思好思路再写代码，这个急不来

感谢：
-
    scir实验室的赵正宇学长帮助了我非常多，在多次加班结束的晚上给我思路的建议，非常感谢
    张伟男老师的支持:D
