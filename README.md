计G191 2019322184 张国琦
#
实验目的
掌握字符串String及其方法的使用
掌握异常处理结构
##
实验要求
内容：利用已学的字符串处理编程完成《长恨歌》古诗整理对齐工作，写出功能函数并运行，达到以下功能：
1、每七个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
2、允许提供输入参数，统计古诗中某个字或词出现的次数
###
启动
####
![image](https://github.com/xianyuforme/changhenge/blob/master/pic/b2baad94822c8710b36e467995532ae.png)
#####
输入要查询的字
######
![image](https://github.com/xianyuforme/changhenge/blob/master/pic/dd7df25eadf199e552b2f4c44365ac9.png)
# changhenge
``` JAVA
import java.util.Scanner;
public class Shi {
    public static void main(String args[]) {
		String str = "汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列土可怜光彩生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行翠华摇摇行复止西出都门百余里六军不发无奈何宛转蛾眉马前死花钿委地无人收翠翘金雀玉搔头君王掩面救不得回看血泪相和流黄埃散漫风萧索云栈萦纡登剑阁峨嵋山下少人行旌旗无光日色薄蜀江水碧蜀山青圣主朝朝暮暮情行宫见月伤心色夜雨闻铃肠断声天旋地转回龙驭到此踌躇不能去马嵬坡下泥土中不见玉颜空死处君臣相顾尽沾衣东望都门信马归归来池苑皆依旧太液芙蓉未央柳芙蓉如面柳如眉对此如何不泪垂春风桃李花开夜秋雨梧桐叶落时西宫南苑多秋草落叶满阶红不扫梨园弟子白发新椒房阿监青娥老夕殿萤飞思悄然孤灯挑尽未成眠迟迟钟鼓初长夜耿耿星河欲曙天鸳鸯瓦冷霜华重翡翠衾寒谁与共悠悠生死别经年魂魄不曾来入梦临邛道士鸿都客能以精诚致魂魄为感君王辗转思遂教方士殷勤觅排空驭气奔如电升天入地求之遍上穷碧落下黄泉两处茫茫皆不见忽闻海上有仙山山在虚无缥渺间楼阁玲珑五云起其中绰约多仙子中有一人字太真雪肤花貌参差是金阙西厢叩玉扃转教小玉报双成闻道汉家天子使九华帐里梦魂惊揽衣推枕起徘徊珠箔银屏迤逦开云鬓半偏新睡觉花冠不整下堂来风吹仙袂飘飖举犹似霓裳羽衣舞玉容寂寞泪阑干梨花一枝春带雨含情凝睇谢君王一别音容两渺茫昭阳殿里恩爱绝蓬莱宫中日月长回头下望人寰处不见长安见尘雾惟将旧物表深情钿合金钗寄将去钗留一股合一扇钗擘黄金合分钿但教心似金钿坚天上人间会相见临别殷勤重寄词词中有誓两心知七月七日长生殿夜半无人私语时在天愿作比翼鸟在地愿为连理枝天长地久有时尽此恨绵绵无绝期";
		int len = str.length();
		String line = "";
		for (int i = 1; i <= len; i++) {
			line += str.charAt(i - 1);
			if (i % 14 == 0) {
				System.out.println(line + "。");
				line = "";
			} else if (i % 7 == 0) {
				line += "，";
			}
		}

		try {
			Scanner sc = new Scanner(System.in);
			
			System.out.println("请输入一个字： ");
			String keyword = sc.next();
			int index = 0;
			int count = 0;
			while ((index = str.indexOf(keyword, index)) != -1) {
				count ++;
				index += keyword.length();
			}
		System.out.println("存在 " + keyword + " 有: " + count + "个");
		} 
		catch (Exception e) {
		}

} 
}
```
感想：在这个实验让我掌握了字符串String及其方法的使用和添加异常处理，由于对于JAVA不太熟悉所以通过在网络搜索相关资料教程，实现了本次实验要求。
这次实验还学习在Github平台上传代码，编写README。这个过程中也掌握了上传的方法。本次试验后感觉自己但对于字符串的一些方法的使用还是不太清晰、熟练，需要多加学习。
