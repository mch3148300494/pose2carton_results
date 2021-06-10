# Pose2Carton
EE228课程大作业，利用3D骨架控制3D卡通人物
# Maya环境配置
1、本小组使用windows系统完成上述大作业，根据助教在知乎给出的Windows配置maya环境的教程，首先在官网上下载、安装maya2020软件，并用学生卡申请教育版权限。  
2、进入maya2020安装目录，在bin文件夹内找到路径，并添加到环境变量。  
3、打开命令终端cmd，在maya环境安装pip和numpy。  
4、在cmd的mayapy中分别输入教程所示的import命令，检测无异常。  
在网上预下载一个fbx文件（本项目所有的fbx文件均在mixamo网站下载得到），在cmd的mayapy中运行fbx_parser文件，得到了对应的obj、txt、mtl以及fbm文件夹，至此Maya环境成功配置完成。
# 匹配流程
1、由于前期不懂如何匹配，经过二人的不断研究和尝试，我们采用了最差的方法来匹配：首先在manual序列中输入符合要求的n:n的序列，比如{0:0,1:1,……,13:13}，其中每一对数据的前一个数表示代码中给出的数字所对应的关节名称，而后一个数表示目前匹配的模型的关节名称，这里的目的是把代码给出的关节与目前匹配的模型的关节正确对应上。我们每次将一个配对后面的数改为0，得到结果后观察哪个部位发生了变化，进而判断前面的数对应的是模型的哪个部位，从而确定每个数代表的关节名称并完成匹配。  
2、后来经过同学们的讨论，我们发现在每一次运行transfer文件的时候都会输出每个数字所代表的关节名称，因此后期我们按照这种方法，首先确定这个模型有多少个关节，然后跑一下transfer代码得到该模型每个数所代表的关节名称，如果遇到少数对不上的关节，我们便按照老方法尝试，减少了很多工作量，最终我们完成了两个group共20个提供的模型的匹配。网上下载的fbx模型在经过fbx_parser代码后得到的txt与obj文件同样用transfer代码进行匹配，匹配流程与上述匹配过程相同。  
# 项目结果
![image](./img/0.png)
![image](./img/1.png)
![image](./img/2.png)
# 协议
本项目在Apache-2.0协议下开源  
所涉及的代码及数据的最终解释权归倪冰冰老师课题组所有  
Group 11
