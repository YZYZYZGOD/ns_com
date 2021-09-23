# ns_com
# 前言
该教程为为了将《二之国:白色圣灰的女王》的1.0.2版本游戏本体与xxgame.net的汉化包自行整合而搜寻并记录所成。仅为个人整合操作过程中的步骤，不涉及可能会出现的特殊情况。若日后还有类似需求并发现特殊情况，会在文章末尾补充。
# 所需工具
1.游戏文件及汉化补丁  
2.[hacpack-v1.36_r2_GUI](https://github.com/The-4n/hacPack)  
3.解包工具  
4.keys.txt 
# 操作
## 1.解包  
打开`NCA-NSP-XCI_TO extract\解包工具整合版.bat`，根据提示及自己的游戏文件格式选择，我的是XCI我就选择XCI了。  
[![4atBRS.png](https://z3.ax1x.com/2021/09/23/4atBRS.png)](https://imgtu.com/i/4atBRS)
然后选择`提取XXX文件`，回车等待解包结束。  
再选择`1.选择NCA文件-->2.提取加密的NCA文件(需Titlekey信息)/1.提取解密的NCA文件(下载的盗版一般选这个)-->2.转换为 Romfs 文件夹`，并将刚刚解包的`Extracted_XXX`文件夹中的最大的`nca`文件拖入回车(将tik格式文件拖入并回车)  
[![4atRI0.png](https://z3.ax1x.com/2021/09/23/4atRI0.png)](https://imgtu.com/i/4atRI0)  
[![4at5zF.png](https://z3.ax1x.com/2021/09/23/4at5zF.png)](https://imgtu.com/i/4at5zF)
当屏幕出现Done!时，结束。得到一个名为`Extracted_NCA`的文件夹，即为解包文件。解包完成。  
## 2.合包
一般解包后的`Extracted_NCA`文件夹中会有`exefs和romfs`两个文件夹，而汉化包也多是这两个文件夹，或是其中一个文件夹。将汉化包中的这两个文件夹复制到`Extracted_NCA`文件夹覆盖内容，合包完成  
[![4aN0T1.png](https://z3.ax1x.com/2021/09/23/4aN0T1.png)](https://imgtu.com/i/4aN0T1)  
## 3.打包
打开`hacpack-v1.36_r2_GUI\hacPack-GUI.exe`并按照提示依次填入所需信息。之后选择`Build NCA`等待漫长的时间后，会提示Done,初步打包完成。  
[![4aNclD.png](https://z3.ax1x.com/2021/09/23/4aNclD.png)](https://imgtu.com/i/4aNclD)  
[![4aNoff.png](https://z3.ax1x.com/2021/09/23/4aNoff.png)](https://imgtu.com/i/4aNoff)  
将原本的`Extracted_XXX`文件夹中的最大的`nca`文件的名字复制下来，并删掉。再将新打包的`nca`文件重命名为原本那个最大的`nca`文件，并放进`Extracted_XXX`文件夹中。  
[![4aUC1U.png](https://z3.ax1x.com/2021/09/23/4aUC1U.png)](https://imgtu.com/i/4aUC1U)  
在`hacPack-GUI.exe`中选择到NSP选项卡，按照提示填入信息，并选择`Build NSP`，漫长等待。  
[![4aUAB9.png](https://z3.ax1x.com/2021/09/23/4aUAB9.png)](https://imgtu.com/i/4aUAB9)  
再次提示Done时，就可以在之前设置的输出路径中看到一个打包好的nsp文件，打包完成。  
以上步骤完成后，整合工作就完成了。  
# 结语
整体步骤较为简单，但需注意的是，在解包步骤中，如果你的游戏文件包是加密过的，则要选择`提取加密的NCA文件`，如果未加密，就选`提取解密的NCA文件`。判断依据就是前一步解包NSP/XCI后的解包文件夹中是否有一个tik格式的文件，若有则为加密的，若无则为解密的。  
2021/9/23 9:37经过昨晚和今早的两次尝试，发现进入游戏都会报错2002-4144，目前原因未知。根据搜索发现更新系统版本可能能解决问题，等待deepsea更新后再做尝试。  
