# ---
#bitman - 小白组 - 李杰
##一： 重装系统问题
###1：利用软件重装
      工具：360重装系统大师（或者金山重装高手）	
方法步骤：具体步骤就可以按照软件上的来 ，选择想要装的系统和所需要保留的文件。
###2：用原版iso镜像文件进行安装
      前期准备：iso文件（从MSDN下载）
方法步骤：用一个U盘制作U盘启动PE系统，网上有老毛桃，大白菜等软件就可以制作。
	  启动PE系统并在虚拟光驱中加载原版iso文件。
	  打开windos安装器，一般PE里面自带，选择要安装系统类型，指定安装源，找到虚拟光驱加载的文件并在一个名叫sources的文件夹下找到“install.wim”文件，在选择镜像名。
	  选择把系统转在c盘并格式化c盘.
	  接下来跟着默认步骤走，等待镜像部署。
	  最后进入系统重装过程，耐心等待，装好后进行一些基本的设置即可。
###3：GHOST重装
      前期准备：GHO镜像文件，GHO安装器
方法步骤：运行GHO安装器。选择还原系统到c盘，浏览到映像文件的路径。
	  进行确认后就可以自动的进去系统还原过程。
	  最后安装好系统后在进行一些基本的设置即可。
    编程软件
因为是小白，电脑上的编程软件就只有visual stdio
##二：虚拟机问题
###1 虚拟机软件：VMware workstation
###2 准备的东西：VMware workstation软件，iso镜像文件
###3安装过程：一般可以直接安装默认的走，在勾选网络模式的时候使用桥接模式，最后安装系统的时候在虚拟光驱中浏览到所下载的iso文件就可以进行安装，安装好后在进行一些基本的设置。
 ![windos  xp](http://i.imgur.com/flCFGxo.png)
 ![ UNIX](http://i.imgur.com/5pGz9GT.png)
 ##三：C语言中基本数据内型长度问题
 	char——1
	short——2
	int——4
	long——4
	long long——8
	void*——4
	float——4
	/*  这是一个计算C语言中基本数据内型长度的一个程序  */
#include<stdio.h>
int main()
{
	printf("%d\n",sizeof(char));
	printf("%d\n",sizeof(short));
	printf("%d\n",sizeof(int));
	printf("%d\n",sizeof(long));
	printf("%d\n",sizeof(long long));
	printf("%d\n",sizeof(void*));
	printf("%d\n",sizeof(float));
	return 0;
}
##四:解释三个基本计算机部件的功能
###1 cpu
	中央处理器（CPU，Central Processing Unit）是一块超大规模的集成电路，是一台计算机的运算核心（Core）和控制核心（ Control Unit）。它的功能主要是解释计算机指令以及处理计算机软件中的数据。cpu负责着计算机内所有的工作，不过它是一个领导者，而不是执行人，它只负责接受指令，计算并告诉别的部件该做什么，而不是自己去做。也可以这么说，它相当于一个翻译官，负责把你的操作告诉计算机内相应的需要调动的部件，并告诉这个部件该如何做。比如，你要看一张自己的照片，欣赏下自己的美貌，所以你点击了下你的照片，这个时候，系统接收到你的指令，知道了你要打开这个文件，所以操作系统告诉cpu，算出这个文件，并且算好后交给显卡让显卡画出来，cpu就会把这个文件换算成代码，换算完成后交给显卡，就相当于它用显卡语言对显卡说“嘿，你，你，你，给我画一张图片，一张大脸，两个眼睛一个鼻子一张嘴，秃子，就这么个玩意，给我画出来。”然后显卡就按照cpu的指示，把图片画出来，你就看到了自己美丽的脸
	CPU主要包括运算器和高速缓冲存储器及实现它们之间联系的数据、控制及状态的总线。
主要工作过程为：CPU从存储器或高速缓冲存储器中取出指令，放入指令寄存器，并对指令译码。它把指令分解成一系列的微操作，然后发出各种控制命令，执行微操作系列，从而完成一条指令的执行。
###2内存：
	内存是计算机中重要的部件之一，它是与CPU进行沟通的桥梁。计算机中所有程序的运行都是在内存中进行的，因此内存的性能对计算机的影响非常大。内存(Memory)也被称为内存储器，其作用是用于暂时存放CPU中的运算数据，以及与硬盘等外部存储器交换的数据。只要计算机在运行中，CPU就会把需要运算的数据调到内存中进行运算，当运算完成后CPU再将结果传送出来，内存的运行也决定了计算机的稳定运行。 内存是由内存芯片、电路板、金手指等部分组成的。
###3 硬盘
	硬盘是电脑主要的存储媒介之一，由一个或者多个铝制或者玻璃制的碟片组成。碟片外覆盖有铁磁性材料。
###4设计原因
	Cpu相当于大脑的核心，负责运算和协调各肢体器官的分工合作，硬盘则相当于我们的记忆系统，负责储存我们输入的数据资料。但cpu并不能直接从硬盘中调取资料，他们之间必须有一个中转中心，那就是内存。Cpu将需要处理的数据从硬盘里拿出来放在内存里，并在内存里运算，并得出结果交给其他部分运行。这就是简单的三个部分设计的原理。
##五:通信录
	#include <stdio.h>
#include <string.h>
#include <stdlib.h>
struct person
{char name[8];
char tel[15];
char addr[50]; 
char email[30];
};
char filename[20];
FILE *fp;
void creat();
void output();
void search();
void append();
void modify();
void del();
void main()
{
	int m;char k;

	printf("\n请输入你要打开的通讯录文件名:");
	gets(filename);
	if((fp=fopen(filename,"r"))==NULL)
		{
		printf("\n当前没有此通讯录文件,现在是否执行创建(Y/N)？:");
		scanf("%c",&k);
		if(k!='Y'&&k!='N'&&k!='y'&&k!='n')
			{printf("\n输入有误,请再次输入一个值:");scanf("%c",&k);}
		else if(k=='Y'||k=='y') {creat();}
				else if(k=='N'||k=='n')
					{printf("\n由于你选择了退出,现在程序即将关闭!\n");exit(0);}
		}
	else
		{
			printf("\n你要打开的通讯录文件%s已存在，现在可直接对其操作：\n",filename);
			printf("通讯录文件中现已有的通讯信息：\n");output();
			printf("\n请选择根据提示选择1~5对通讯录文件进行操作。\n");
		}
  while (1)
  {printf("\n\n添加,请按1");
   printf("\n查找,请按2");
  printf("\n修改,请按3"); 
  printf("\n删除,请按4");
  printf("\n输出,请按5");
  printf("\n退出,请按0\n");
  scanf("%d",&m);
  if(m>=0&&m<=5)
  {switch(m)
  {case 1: append();break;
case 2: search();break;
case 3: modify();break;
case 4: del();break;
case 5:output();break;
case 0:exit(0);
  }
  printf("\n\n操作完毕,请再次选择!");
  }
 else printf("\n\n操作错误，请再次选择!:");
}
}
void creat()
{struct person one;
printf("\n请输入通讯簿文件名：");
scanf("%s",filename);
if ((fp=fopen(filename,"w"))==NULL)
{printf("\n不能建立通讯薄！");
exit(0);
}
fprintf(fp,"%-10s%-20s%-30s%-20s\n","姓名","电话号码","住址","电子邮箱");
printf("\n请输入姓名:\n");
		scanf("%s",one.name);
		while (strcmp(one.name,"0"))
	{		printf("请输入电话号码:\n");
		scanf("%s",one.tel);
		printf("请输入住址:\n");
		scanf("%s",one.addr);
		printf("请输入电子邮箱:\n");
			scanf("%s",one.email);
		fprintf(fp,"%-10s%-20s%-30s%-20s\n",one.name,one.tel,one.addr,one.email);
		printf("请再输入另一个人的姓名,若想要结束,请输入0\n");
		scanf("%s",one.name);
		}
		fclose(fp);
}

void output()
{struct person one;
	if((fp=fopen(filename,"r"))==NULL)
	{printf("\n不能打开通讯薄!");
	exit(0);
	}
while (!feof(fp))
{fscanf(fp,"%s%s%s%s\n",one.name,one.tel,one.addr,one.email);
printf("%-10s%-20s%-30s%-20s\n",one.name,one.tel,one.addr,one.email);
}
fclose(fp);
}
void append()
{struct person one;
if ((fp=fopen(filename,"a"))==NULL)
{printf("\n不能打开通讯薄!");
 exit(0);
}
	printf("\n请输入添加的姓名\n");
	scanf("%s",one.name);
	printf("请输入电话号码:\n");
		scanf("%s",one.tel);
		printf("请输入住址:\n");
		scanf("%s",one.addr);
		printf("请输入电子邮箱:\n");
		scanf("%s",one.email);
printf("%-10s%-20s%-30s%-20s\n",one.name,one.tel,one.addr,one.email);
fprintf(fp,"%-10s%-20s%-30s%-20s\n",one.name,one.tel,one.addr,one.email);
fclose(fp);
}

void search()
{int flag=0;
 char namekey[8];
 struct person one;
 printf("\n请输入姓名：");
 scanf("%s",namekey);
 if((fp=fopen(filename,"r"))==NULL)
 {printf("\n不能打开通讯薄！");
 exit(0);
}
 while(!feof(fp))
 {fscanf(fp,"%s%s%s%s\n",one.name,one.tel,one.addr,one.email);
 if (!strcmp(namekey,one.name))
 {printf("\n\n已查到，记录为：");
 printf("\n%-10s%-20s%-30s%-20s",one.name,one.tel,one.addr,one.email);
 flag=1;
 }
 }
 if(!flag)
	 printf("\n\n对不起，通讯薄中没有此人的记录。");
 fclose(fp);
}

void modify()
{int flag=0;
long offset;
char namekey[8];
struct person one;
printf("\n请输入姓名:");
scanf("%s",namekey);
if((fp=fopen(filename,"r+"))==NULL)
{printf("\n不能打开通讯薄!");
exit(0);
}
while(!feof(fp))
{ offset=ftell(fp);
fscanf(fp,"%s%s%s%s\n",one.name,one.tel,one.addr,one.email);
if(!strcmp(namekey,one.name))
{flag=1;
break;
}
}
if(flag)
{printf("\n已查到,记录为");
printf("\n%-10s%-20s%-30s%-20s",one.name,one.tel,one.addr,one.email);
    while (1)
	{	printf("\n\n修改姓名,请按2");
		printf("\n修改电话,请按3");
		printf("\n修改地址,请按4"); 
		printf("\n修改邮箱,请按5");
		printf("\n退出,请按6\n");
		 scanf("%d",&flag);
		 if (flag==2)  {printf("请输入新的姓名\n");  scanf("%s",one.name);printf("修改完毕,请指示!:\n");}
		if (flag==3) {printf("请输入新的电话\n");scanf("%s",one.tel);printf("修改完毕,请指示!:\n");}
		if(flag==4) {printf("请输入新的地址\n");scanf("%s",one.addr);printf("修改完毕,请指示!:\n");}
		if(flag==5) {printf("请输入新的邮箱\n");scanf("%s",one.email);printf("修改完毕,请指示!:\n");}
		 if (flag==6)  break;
      
	 }  
	  fseek(fp,offset,0);
	  fprintf(fp,"%-10s%-20s%-30s%-20s\n",one.name,one.tel,one.addr,one.email);
	  printf("\n%-10s%-20s%-30s%-20s",one.name,one.tel,one.addr,one.email);
}       
else printf("不存在指定的名字!\n");
fclose(fp);
}

void del()
{  
	int  m,flag=0;
    long offset;
    char namekey[8];
    struct person one;
    printf("\n请输入姓名:");
    scanf("%s",namekey);
    if((fp=fopen(filename,"r+"))==NULL)
    {  
		printf("\n不能打开通讯簿！");
		exit(0);
    }
    while(!feof(fp))
    {  
		offset=ftell(fp);
		fscanf(fp,"%s%s%s%s\n",one.name,one.tel,one.addr,one.email);
		if(!strcmp(namekey,one.name)) {flag=1;break;}
    }
	if(flag)
	{ 
		printf("\n已查到，记录为");
        printf("\n%-10s%-20s%-30s%-20s",one.name,one.tel,one.addr,one.email);
        printf("\n确定要删除,按1;不删除,按0:");
			scanf("%d",&m);
		if (m)
		{fseek(fp,offset,SEEK_SET);
		fprintf(fp,"%-10s%-20s%-30s%-20s\n","","","","","");
		}
				
	}
    else
		printf("\n对不起，通讯簿中没有此人的记录。");
    fclose(fp);
}
###ps：通信录取于百度，小白还在专研，并没有弄懂。
但因时间拖得太久  所以还是交了先。




