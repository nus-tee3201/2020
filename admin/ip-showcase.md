<frontmatter>
title: "iP Showcase"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 2
</frontmatter>

# iP Showcase

{% set tutorials = [
"CS2103T-W11",
"CS2103T-W12",
"CS2103T-W13",
"CS2103T-T09",
"CS2103T-T10",
"CS2103-T11",
"CS2103T-T11",
"CS2103T-T12",
"CS2103T-T13",
"CS2103-T14",
"CS2103-T16",
"CS2103T-T17",
"CS2103-F09",
"CS2103-F10",
"CS2103T-F11",
"CS2103T-F12",
"CS2103T-F13",
"CS2103T-F14"
] %}

{% set students = [
["ANG W ... DRICK", "CS2103-F09-1", "KendrickAng"],
["GOH R ... I ZHI", "CS2103-F09-1", "mirozo"],
["HSU Z ... G JUN", "CS2103-F09-1", "dcshzj"],
["KHENG ...DONG", "CS2103-F09-1", "ChrisKheng"],
["KWAN... SHENG", "CS2103-F09-1", "mrchensheng21"],
["ABDUL ... ATIFF", "CS2103-F09-2", "AHaliq"],
["LEONG ... MOTHY", "CS2103-F09-2", "timothyleong97"],
["LIM H ... I MIN", "CS2103-F09-2", "huiminlim"],
["MUHAM ... ILANI", "CS2103-F09-2", "PhireHandy"],
["SHAWN ...CHEW", "CS2103-F09-2", "shawnpunchew11"],
["TAN Y ... TALIE", "CS2103-F09-2", "nattanyz"],
["ANDY... K WEE", "CS2103-F09-3", "andyylam"],
["CHOW... I WAI", "CS2103-F09-3", "chowyiwai"],
["LIM Z ... I WEI", "CS2103-F09-3", "halfwhole"],
["LIU Z ... ZECHU", "CS2103-F09-3", "LiuZechu"],
["ONG Y ...CHUN", "CS2103-F09-3", "yaaanch"],
["CHAIT ... ANWAL", "CS2103-F09-4", "chaitanyabaranwal"],
["CHEN... UANBO", "CS2103-F09-4", "ybchen97"],
["CHOW... I YIN", "CS2103-F09-4", "chowyiyin"],
["LAW A ... LARRY", "CS2103-F09-4", "larrylawl"],
["OLIVE ... CHEOK", "CS2103-F09-4", "olivercheok20"],
["CHAO... BRIEL", "CS2103-F10-1", "gabrielchao"],
["CHEON ...HONG", "CS2103-F10-1", "cheongsiuhong"],
["LEE W ... TTHEW", "CS2103-F10-1", "crazoter"],
["LOW S ... ANCIS", "CS2103-F10-1", "francislow"],
["RAMAC ... NDHYA", "CS2103-F10-1", "sandydays"],
["EVELY ... ULIET", "CS2103-F10-2", "evelynejuliet"],
["KELVI ... ARRIS", "CS2103-F10-2", "kelvinnharris"],
["TIE Y ... HLEEN", "CS2103-F10-2", "teika97"],
["VEGI... MANAS", "CS2103-F10-2", "ManasVegi"],
["ZHANG ...XUAN", "CS2103-F10-2", "zhangxuan97"],
["KENG...XIAN", "CS2103-F10-3", "jxofficial"],
["NEO S ... I HAO", "CS2103-F10-3", "neoshh"],
["NG TZ ... SHAUN", "CS2103-F10-3", "ShaunNgTX"],
["SIM K ...LEON", "CS2103-F10-3", "khiangleon"],
["WILFR ... Y TAN", "CS2103-F10-3", "wilfredbtan"],
["JOSHI ... ABHAY", "CS2103-T11-1", "atharvjoshi"],
["LIN M ... EI AN", "CS2103-T11-1", "hellopanda128"],
["MUHAM ... AJJAJ", "CS2103-T11-1", "madanalogy"],
["NG QI ... HERYL", "CS2103-T11-1", "Yoshi275"],
["WANG... INMAN", "CS2103-T11-1", "tirameshu"],
["CHEN... EN SU", "CS2103-T11-2", "chensu2436"],
["CHEON ...YUAN", "CS2103-T11-2", "CheongLiYuan"],
["LUK C ...HENG", "CS2103-T11-2", "AaronLuk"],
["NG YO ...KUAN", "CS2103-T11-2", "SendorasLeft"],
["TAN W ...ADAM", "CS2103-T11-2", "MistyRainforest"],
["CHRIS ...TENG", "CS2103-T11-3", "belbel98"],
["HO WE ...CHIN", "CS2103-T11-3", "HoWeiChin"],
["KOH Z ... SHAWN", "CS2103-T11-3", "shawnkoh"],
["OOI M ... SHENG", "CS2103-T11-3", "ooimingsheng"],
["LOH W ...KIAT", "CS2103-T14-1", "weikiat97"],
["SEBAS ...YONG", "CS2103-T14-1", "SebastianLie"],
["TAY S ... HERYL", "CS2103-T14-1", "sheryltay28"],
["YOON... , KEN", "CS2103-T14-1", "Xelyion"],
["AHMAD ... HAMAD", "CS2103-T14-2", "AhmadHatziq"],
["ELLIE ... EN NA", "CS2103-T14-2", "Ellieyee"],
["TAN Y ... YUGIN", "CS2103-T14-2", "lumos309"],
["YEW K ... I ZHE", "CS2103-T14-2", "Zihawkeye"],
["HE SO ... NGCHI", "CS2103-T14-3", "Akimatsu98"],
["JOLYN ... SI QI", "CS2103-T14-3", "jolynnn8D"],
["LIANG ... OYUAN", "CS2103-T14-3", "Oscar-B-Liang"],
["LING... I WEI", "CS2103-T14-3", "lzw12345"],
["LIM X ... N HUI", "CS2103-T14-4", "limxuanhui"],
["NG CH ... N WAH", "CS2103-T14-4", "choonx99"],
["SYED... UNIED", "CS2103-T14-4", "muhammadaljunied"],
["XIU Z ... IHENG", "CS2103-T14-4", "Cary-Xx"],
["CHEN... EN XI", "CS2103-T16-1", "chen-xi-cx"],
["JIANG ... YUXIN", "CS2103-T16-1", "jyx11011"],
["NEO W ... IHONG", "CS2103-T16-1", "whneo97"],
["STEPH ... G ZHI", "CS2103-T16-1", "scwaterbear"],
["ZHANG ... IAOYU", "CS2103-T16-1", "ZhangHuafan"],
["JOANN ... PURBA", "CS2103-T16-2", "joannasara"],
["TOH C ... SMINE", "CS2103-T16-2", "tohcejasmine"],
["TUAN... G WEI", "CS2103-T16-2", "tuandingwei"],
["VICTO ... ARIAN", "CS2103-T16-2", "victorvic54"],
["BILL...CHEE", "CS2103-T16-3", "LivingOnEdge"],
["CHAN... ATHAN", "CS2103-T16-3", "jonchan51"],
["LIU G ... GYUAN", "CS2103-T16-3", "gary-lgy"],
["LIU Z ...ZIMU", "CS2103-T16-3", "cutieprobe"],
["MO ZO ... NGRAN", "CS2103-T16-3", "moziliar"],
["CHAN...RONG", "CS2103-T16-4", "rongrongrr"],
["JESSI ... U XIN", "CS2103-T16-4", "jessicax941"],
["ONG M ... CHUNG", "CS2103-T16-4", "Dandford"],
["TAN Y ...JIAN", "CS2103-T16-4", "swampertx"],
["TAY Y ...HONG", "CS2103-T16-4", "yuhongtay"],
["ABHIM ... YADAV", "CS2103T-F11-1", "Abhiman2211"],
["JOSHU ... CHIEN", "CS2103T-F11-1", "hcwong"],
["KYUNG ... O MIN", "CS2103T-F11-1", "john0227"],
["YAP J ... A AUN", "CS2103T-F11-1", "Joanna-YJA"],
["YEN R ... BRIAN", "CS2103T-F11-1", "brianyenna"],
["LIAW... W YEE", "CS2103T-F11-2", "liawsy"],
["LIU X ... IAOYU", "CS2103T-F11-2", "xiaoyu-nus"],
["PHOEB ... R HUI", "CS2103T-F11-2", "febee99"],
["SIM J ... ARREN", "CS2103T-F11-2", "Kalsyc"],
["TAN K ... EREMY", "CS2103T-F11-2", "JermyTan"],
["HOON...PING", "CS2103T-F11-3", "hooncp"],
["LEE E ...JIAN", "CS2103T-F11-3", "eejian97"],
["LEOW...YONG", "CS2103T-F11-3", "jityong"],
["NI TI ... NZHEN", "CS2103T-F11-3", "niqiukun"],
["YANG...TING", "CS2103T-F11-3", "yhtingg"],
["JEREM ... IERUI", "CS2103T-F11-4", "Parcly-Taxel"],
["LEE L ... IRENE", "CS2103T-F11-4", "irene-lly"],
["SHUI... I YAO", "CS2103T-F11-4", "shuiyao-sg"],
["WANG... ETING", "CS2103T-F11-4", "ShirleyWangxt"],
["ZHANG ... NGJUN", "CS2103T-F11-4", "Auxinnn"],
["BRUCE ... E ONG", "CS2103T-F12-1", "bruceskellator"],
["DENIS ...TJIA", "CS2103T-F12-1", "WeomuCat"],
["ONG C ...GENG", "CS2103T-F12-1", "ChengGeng97"],
["TEH H ... ARCUS", "CS2103T-F12-1", "marcusteh1238"],
["TIMOT ... HIWEN", "CS2103T-F12-1", "Kyzure"],
["GABRI ... ENHAO", "CS2103T-F12-2", "gachia"],
["GABRI ... N XIN", "CS2103T-F12-2", "Q-gabe"],
["JASON ... G KAY", "CS2103T-F12-2", "ReignOfComputer"],
["JERRO ... YU YI", "CS2103T-F12-2", "Wingedevil"],
["ZHENG ... IQIAO", "CS2103T-F12-2", "SQwQ"],
["NG SH ... I WEI", "CS2103T-F12-3", "shiweing"],
["ONG Y ... JONAS", "CS2103T-F12-3", "e0031374"],
["STEVE ... IJAYA", "CS2103T-F12-3", "stevenwjy"],
["TAN L ... LIKAI", "CS2103T-F12-3", "tanlk99"],
["YEHEZ ... OROES", "CS2103T-F12-3", "Yehezkiel01"],
["CHIA... DAVID", "CS2103T-F12-4", "Davidcwh"],
["FANG... EIWEN", "CS2103T-F12-4", "waynefong0401"],
["HUANG ... EIJIE", "CS2103T-F12-4", "weiijiie"],
["LEE W ...FONG", "CS2103T-F12-4", "waifonglee"],
["ZHOU... NMING", "CS2103T-F12-4", "xinmingzh"],
["HO HO ... L YIN", "CS2103T-F13-1", "hoholyin"],
["LIN Y ... UTING", "CS2103T-F13-1", "linyutinglyt"],
["SEE Z ...YANG", "CS2103T-F13-1", "seeziyang"],
["WANG... HIYAO", "CS2103T-F13-1", "shiyao821"],
["YEO T ...TONG", "CS2103T-F13-1", "Cronyxx"],
["CHOO...YUAN", "CS2103T-F13-2", "Raikonen"],
["CHUA... , JON", "CS2103T-F13-2", "jon-chua"],
["KOH W ... RENCE", "CS2103T-F13-2", "fatclarence"],
["LOW J ...SEAN", "CS2103T-F13-2", "seanlowjk"],
["ROBY... ANAMA", "CS2103T-F13-2", "robytanama"],
["AUSTI ... NTOSO", "CS2103T-F13-3", "austinsantoso"],
["BENED ... G JUN", "CS2103T-F13-3", "Nanosync"],
["CHOON ... G XIN", "CS2103T-F13-3", "choongyx"],
["JONAT ... NDANA", "CS2103T-F13-3", "jonathantjendana"],
["MIN P ... E MOE", "CS2103T-F13-3", "minpyaemoe"],
["CALEB ... E GEN", "CS2103T-F13-4", "heze8"],
["CHIAN ... JARED", "CS2103T-F13-4", "jcjjjared"],
["MICHE ... I WEN", "CS2103T-F13-4", "michelleykw"],
["WONG... N KAI", "CS2103T-F13-4", "wongchuankai"],
["WU XI ... U XIA", "CS2103T-F13-4", "tswuxia"],
["ALEX... AN YU", "CS2103T-F14-1", "alxkohh"],
["LIM H ... W JIA", "CS2103T-F14-1", "limhawjia"],
["NING... GYING", "CS2103T-F14-1", "ning-sy210"],
["ZHANG ...JIAN", "CS2103T-F14-1", "zhangj1an"],
["BRYAN ... N WEI", "CS2103T-F14-2", "ngswbryan"],
["CAESA ... ZHANG", "CS2103T-F14-2", "caesarpjz"],
["LIM S ... ERWIN", "CS2103T-F14-2", "kerwin97"],
["TEO S ... N JIE", "CS2103T-F14-2", "TeoShyanJie"],
["XU TU ... U NAN", "CS2103T-F14-2", "Xuerneas"],
["HU YU ... UCHEN", "CS2103T-F14-3", "brebeek"],
["KO GI ... I HUN", "CS2103T-F14-3", "nordic96"],
["LIM Y ... KEVIN", "CS2103T-F14-3", "lyskevin"],
["NG JU ... N HAO", "CS2103T-F14-3", "jun-ha0"],
["SUDHA ... HAVAN", "CS2103T-F14-3", "uggi121"],
["CHEE... E YOU", "CS2103T-F14-4", "cheeyou"],
["RUSHA ... HAMAS", "CS2103T-F14-4", "ArgVampir"],
["SAM Y ... G JEK", "CS2103T-F14-4", "SamYJ2606"],
["SONG... IANYI", "CS2103T-F14-4", "tysng"],
["TAN J ...BANG", "CS2103T-F14-4", "junnbang"],
["CHEN... I JUN", "CS2103T-T09-1", "OneArmyj"],
["LEW K ...MING", "CS2103T-T09-1", "KxxMxxx"],
["OSCAR ...HONG", "CS2103T-T09-1", "oscarsu97"],
["YEO Y ... RNEST", "CS2103T-T09-1", "ernestyyh"],
["LEONG ... XIANG", "CS2103T-T09-1", "1nefootstep"],
["CHAI...TUNG", "CS2103T-T09-2", "jietung"],
["HO WE ... I HAW", "CS2103T-T09-2", "weihaw08"],
["KWEK... EE EN", "CS2103T-T09-2", "kwekke"],
["LIM Y ...GARY", "CS2103T-T09-2", "garylyp"],
["TAN C ...PENG", "CS2103T-T09-2", "t-cheepeng"],
["DANIE ...XIAN", "CS2103T-T09-3", "CarbonGrid"],
["LUM C ... SHAWN", "CS2103T-T09-3", "SakuraBlossom"],
["WEN S ... SHUFA", "CS2103T-T09-3", "woon17"],
["WONG... N MIN", "CS2103T-T09-3", "wongsm7"],
["EUGEN ... U WEI", "CS2103T-T09-4", "EugeneTeu"],
["OOI Q ... U JIA", "CS2103T-T09-4", "qiujiaaa"],
["OON Z ... XIANG", "CS2103T-T09-4", "zhixianggg"],
["YAN W ... LIANG", "CS2103T-T09-4", "uberSaiyan"],
["YEO D ... G HAN", "CS2103T-T09-4", "yeodonghan"],
["ANISH ... OSEPH", "CS2103T-T10-1", "nishcafe"],
["GOH S ...NING", "CS2103T-T10-1", "gohsnn"],
["MARC... G KIT", "CS2103T-T10-1", "marcfyk"],
["RYAN... AN YU", "CS2103T-T10-1", "ryanYtan"],
["TAN Y ... E KAI", "CS2103T-T10-1", "mrnewguy"],
["CHUA... A LUN", "CS2103T-T10-2", "hua-lun"],
["LEE W ... E WAH", "CS2103T-T10-2", "bakwxh"],
["LIEW... N WEI", "CS2103T-T10-2", "bigjunnn"],
["MUHAM ... AZMAN", "CS2103T-T10-2", "khairulazman1997"],
["YEO Y ... N XIN", "CS2103T-T10-2", "yyuanxin"],
["BRYAN ... N JIE", "CS2103T-T10-3", "blimyj"],
["CHAND ...HEMA", "CS2103T-T10-3", "lrchema"],
["LIM Y ... U HUI", "CS2103T-T10-3", "mannggoo"],
["LOW C ... NG YI", "CS2103T-T10-3", "Icesiolz"],
["NG SI ...HWEE", "CS2103T-T10-3", "sianghwee"],
["AIDIL ... MSANI", "CS2103T-T10-4", "aidilfbk"],
["ALVIN ... N KIT", "CS2103T-T10-4", "Alvinnyk"],
["LIM Y ... I JIE", "CS2103T-T10-4", "YiJiee"],
["ONG P ... ARCUS", "CS2103T-T10-4", "marqueurs404"],
["TAN D ... EMENT", "CS2103T-T10-4", "klementtan"],
["CHEN...ANQI", "CS2103T-T11-1", "anqichen9856"],
["CHONG ...KANG", "CS2103T-T11-1", "czkay"],
["FUNG... EI-EN", "CS2103T-T11-1", "briyanii"],
["QUEK...PING", "CS2103T-T11-1", "qweiping31415"],
["RYO C ... MANDA", "CS2103T-T11-1", "ryoarmanda"],
["CHEN... N HUI", "CS2103T-T11-2", "chrischenhui"],
["JASON ... CITRO", "CS2103T-T11-2", "jascxx"],
["KOH Y ... YI DA", "CS2103T-T11-2", "kohyida1997"],
["L.V.S ... BBASH", "CS2103T-T11-2", "sreesubbash"],
["THO W ...PAUL", "CS2103T-T11-2", "dragontho"],
["CALVI ... NGZHU", "CS2103T-T11-3", "calvincxz"],
["CHIA... E XUN", "CS2103T-T11-3", "DivineDX"],
["ESHWA ... PATHY", "CS2103T-T11-3", "eshwarkp"],
["GU CH ... UNZHI", "CS2103T-T11-3", "Crisgu"],
["YAP S ... I HAO", "CS2103T-T11-3", "shihaoyap"],
["ANG Z ... ZE YU", "CS2103T-T11-4", "ang-zeyu"],
["DERRI ...YING", "CS2103T-T11-4", "teoha"],
["KARAN ... SAPRA", "CS2103T-T11-4", "eizon05"],
["SAKSH ... DYUMN", "CS2103T-T11-4", "SakshiPradyumn"],
["WANG... IANYI", "CS2103T-T11-4", "arjunwangty"],
["ABHIN ... MNATH", "CS2103T-T12-1", "ambhinav"],
["KOH H ... ABETH", "CS2103T-T12-1", "elsakoh"],
["RAVI... UMARR", "CS2103T-T12-1", "ArunBeCoding"],
["SEAH...LYNN", "CS2103T-T12-1", "seahlynn"],
["SEOW... BRIEL", "CS2103T-T12-1", "gabrielseow"],
["CHOON ... N YAO", "CS2103T-T12-2", "charliechoong"],
["LOW E ... E TER", "CS2103T-T12-2", "etlow"],
["RYAN...JIAN", "CS2103T-T12-2", "ryantay232"],
["YUAN... ANLEY", "CS2103T-T12-2", "SoilingRogue"],
["ZHOU... IANYU", "CS2103T-T12-2", "MackyMaguire"],
["DOMIN ... WENYI", "CS2103T-T12-3", "hellodommy"],
["ERWIN ... O XIN", "CS2103T-T12-3", "ChangUo79"],
["LEE S ... SHAWN", "CS2103T-T12-3", "shawnlsj97"],
["LIM J ... N HUP", "CS2103T-T12-3", "junhuplim"],
["POON... N HOE", "CS2103T-T12-3", "jeunhoe"],
["KEITH ... U HUI", "CS2103T-T12-4", "keiteo"],
["LEONA ... A HAO", "CS2103T-T12-4", "LeonardTay748"],
["LEOW... N BIN", "CS2103T-T12-4", "LeowWB"],
["TAN W ... ALSON", "CS2103T-T12-4", "dalsontws"],
["YANG... UTING", "CS2103T-T12-4", "ShuTingY"],
["CHOW...YING", "CS2103T-T13-1", "C-likethis123"],
["CHUA... M NEE", "CS2103T-T13-1", "SimNee"],
["ISKAN ... HAINI", "CS2103T-T13-1", "TheRealRavager"],
["WILLI ... SNADI", "CS2103T-T13-1", "WilliamRyank"],
["YIP Y ...PENG", "CS2103T-T13-1", "Yen-Peng"],
["BAHET ... RJAVI", "CS2103T-T13-2", "arjavibahety"],
["BERNI ... I YIN", "CS2103T-T13-2", "bernicechio"],
["CHAN... DALIS", "CS2103T-T13-2", "dalisc"],
["HONG... AO YI", "CS2103T-T13-2", "shaoyi1997"],
["VOONG ...XUAN", "CS2103T-T13-2", "ambervoong"],
["DANIE ...SHEN", "CS2103T-T13-3", "dawo5010"],
["EVON...BING", "CS2103T-T13-3", "EvonDong"],
["JIN S ... UYUAN", "CS2103T-T13-3", "CoderStellaJ"],
["LIM K ... G YEE", "CS2103T-T13-3", "kangyeelim"],
["TANG... HAELA", "CS2103T-T13-3", "MichaelaTSH"],
["DARYL ... L TAN", "CS2103T-T13-4", "openorclose"],
["DORCA ... A TAN", "CS2103T-T13-4", "dorcastan"],
["NA NA ... AZHOU", "CS2103T-T13-4", "Na-Nazhou"],
["TSAI, ... O-HAN", "CS2103T-T13-4", "TSAI-HSIAO-HAN"],
["YOKE... I XIN", "CS2103T-T13-4", "kxyoke"],
["CHONG ...YUAN", "CS2103T-T17-1", "ccyccyccy"],
["KWONG ... JERRY", "CS2103T-T17-1", "jerryk1997"],
["PHILI ... DIMAN", "CS2103T-T17-1", "philipalexanderb"],
["SNG J ... FARIS", "CS2103T-T17-1", "fadisng"],
["WANG... NDING", "CS2103T-T17-1", "R-D-D-D"],
["HON H ...CHEN", "CS2103T-T17-2", "honhaochen"],
["NG ZH ...MING", "CS2103T-T17-2", "ngzhaoming"],
["ONG B ... G JUE", "CS2103T-T17-2", "bjhoohaha"],
["POH L ... N WEI", "CS2103T-T17-2", "pohlinwei"],
["TISHY ... HANNA", "CS2103T-T17-2", "tishyakhanna97"],
["LU WE ... WENQI", "CS2103T-W11-1", "LuWenQ"],
["SHE J ... JIAYU", "CS2103T-W11-1", "jiayushe"],
["TAN Y ... NHONG", "CS2103T-W11-1", "le0tan"],
["TIU W ... E HAN", "CS2103T-W11-1", "tiuweehan"],
["YU CH ... NGHUI", "CS2103T-W11-1", "Seris370"],
["JIA X ... ODONG", "CS2103T-W11-2", "podocarp"],
["JOHN... G JIE", "CS2103T-W11-2", "JohnNzj"],
["KEVEN ... UQUAN", "CS2103T-W11-2", "Aulud"],
["LEE L ...GHEE", "CS2103T-W11-2", "liakify"],
["LIM D ... EKOON", "CS2103T-W11-2", "daekoon"],
["ANG K ... AI QI", "CS2103T-W11-3", "jakq"],
["BALAM ... REDDY", "CS2103T-W11-3", "ROHITREDDYBALAM"],
["CHAN... DARYL", "CS2103T-W11-3", "dvrylc"],
["NADIA ... YAHYA", "CS2103T-W11-3", "walnads"],
["TEO J ...HONG", "CS2103T-W11-3", "JunHongT"],
["FANG...SERN", "CS2103T-W11-4", "fangpinsern"],
["NG WE ... FELIX", "CS2103T-W11-4", "FelixNWJ"],
["RYAN...RONG", "CS2103T-W11-4", "iltep64"],
["TAN X ... URICE", "CS2103T-W11-4", "MauriceTXS"],
["JOSHU ...SUEN", "CS2103T-W12-1", "joshuaseetss"],
["LAWNC ... A WEI", "CS2103T-W12-1", "lawncegoh"],
["LEE W ... I GEN", "CS2103T-W12-1", "weigenie"],
["TAN Z ...MING", "CS2103T-W12-1", "TanZhanMing"],
["WANG... G QIN", "CS2103T-W12-1", "wangqinNick"],
["ANG C ... ELVIN", "CS2103T-W12-2", "krusagiz"],
["LEE B ... QIANG", "CS2103T-W12-2", "lightz96"],
["LYE J ... N WEN", "CS2103T-W12-2", "lye-jw"],
["OEN Q ... ENSON", "CS2103T-W12-2", "kensonoenqh"],
["POH J ... A HAO", "CS2103T-W12-2", "limerencee"],
["DING... UCHEN", "CS2103T-W12-3", "dingyuchen"],
["LOONG ...JOEL", "CS2103T-W12-3", "joloong"],
["PARK... E WON", "CS2103T-W12-3", "yewon0303"],
["TAN W ... TRAND", "CS2103T-W12-3", "berttwm"],
["WALLA ... E LIM", "CS2103T-W12-3", "wallacelim97"],
["KARTI ... ELWAL", "CS2103T-W12-4", "troomtroom"],
["LEE Y ... IYUAN", "CS2103T-W12-4", "LeeYiyuan"],
["LIM W ... UGENE", "CS2103T-W12-4", "nexolute"],
["OLIVI ... ANZHI", "CS2103T-W12-4", "Alaete"],
["TAN W ...YANG", "CS2103T-W12-4", "weiyang13"],
["GE SH ... UMING", "CS2103T-W13-1", "geshuming"],
["GUO Z ...ZILI", "CS2103T-W13-1", "CowSaysBaa"],
["MURUG ... THIKA", "CS2103T-W13-1", "kzrthikz"],
["WANG... IRLEY", "CS2103T-W13-1", "bitterg0d"],
["WU XI ...ALEX", "CS2103T-W13-1", "alexwxh"],
["FABIA ...PENG", "CS2103T-W13-2", "fabbbbbbyy"],
["JEONG ... U HAN", "CS2103T-W13-2", "jeongyh99"],
["K ALA ... LAGES", "CS2103T-W13-2", "alages97"],
["LUM W ...BOON", "CS2103T-W13-2", "lumwb"],
["RUSSE ... UN FA", "CS2103T-W13-2", "Russell-Loh-NUS"],
["CHAN... N REN", "CS2103T-W13-3", "chanjunren"],
["CHEN... AIBIN", "CS2103T-W13-3", "ckb055"],
["JASMI ... A MIN", "CS2103T-W13-3", "jaesimin"],
["LIM Y ... AMUEL", "CS2103T-W13-3", "Sam-limyr"],
["SAHIL ... THANI", "CS2103T-W13-3", "Sahilgat"],
["CHEN... IEHAN", "CS2103T-W13-4", "ChenJiehan318"],
["CHONG ... G JUN", "CS2103T-W13-4", "tcgj"],
["DARYL ... I KAI", "CS2103T-W13-4", "cambrian-dk"],
["KENNE ... EN YU", "CS2103T-W13-4", "kenneth-fung"],
["TEE H ... O WEI", "CS2103T-W13-4", "thwnus"]
] %}

{% set current_team = "" %}
{% for tutorial in tutorials  %}
<panel header="## {{ tutorial }}" no-close expanded>
{% for student in students  %}
{% set student_team = student[1] %}
{% set student_tutorial = student_team.slice(0, -2) %}
{% if student_tutorial == tutorial %}
{% if current_team != student_team %}
  {% set current_team = student_team %}
### <span class="badge badge-secondary">{{ student_team }}</span>
{% endif %}
{% set student_name = student[0] %}
{% set username = student[2] %}
{% set duke_website = "https://" + username + ".github.io/duke" %}
{% set duke_repo = "https://github.com/" + username + "/duke" %}
#### {{ student_name }} ([<span class="text-monospace">@{{ username }}</span>](https://github.com/{{ username }})) <small>[:fas-home:]({{ duke_website }}) [:fab-github:]({{ duke_repo }}) [:fas-download:]({{ duke_repo }}/releases) [:fas-code:](https://nus-cs2103-{{ semester | lower }}.github.io/ip-dashboard/#sort=groupTitle&groupSelect=groupByAuthors&search={{ username }}&sortWithin=title&since=2019-08-16&timeframe=commit&mergegroup=false&breakdown=false&tabOpen=true&tabType=authorship&tabAuthor={{ username }}&tabRepo={{ username }}%2Fduke%5Bmaster%5D) [:fas-code-branch:](https://github.com/nus-cs2103-{{ semester }}/duke/pulls/{{ username }}) <trigger for="pop:{{ username }}"><span class="text-primary">:fas-user:</span></trigger></small>
<img src="{{ duke_website }}/Ui.png" height="750" style="max-width: 100%"  onerror="this.src='images/placeholder-small.png';" /><p/>


<popover id="pop:{{ username }}" title="{{ student_name }}" placement="top">
  <div slot="content">

<img style="border-radius: 8px;" src="https://{{ semester | lower }}-{{ student_team }}.github.io/main/images/{{ username | lower }}.png" width="200" onerror="this.src='images/placeholder-small.png';" />

  </div>
</popover>
<hr>
{% endif %}
{% endfor %}

</panel>
{% endfor %}