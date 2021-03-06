# “Google IP使用频率限制”选项

##概述：

GFW对google ip的使用，采用多种方法进行判断。  
其中同一个ip的连接频率，如果过高，会被封锁一段时间。  

因此同一个ip，不能过于频繁的使用。  
但是，高质量的ip也越来越少，如果好的ip没有充分利用，连接速度就会打折扣。   
不同地区、不同网络的限制也不相同，无法给出确切的指导，需要自己摸索试验。  

##原理：  

+ XX-Net保留了扫描到的3000个可用google ip，按连接速度排序
+ 优先采用最快的ip连接
+ 限制每个ip的连接频率，避免被探测到封锁
  
因此，如果连接频率限制太高，就会经常用到慢的ip，影响体验。  
反过来，如果连接频率限制太小，被探测到，就会导致上不了网、不稳定。  
所以需要根据实际情况，摸索最佳的连接频率限制。  

##调整方法：

+ 默认限制一个ip 10秒使用一次  
+ 如果感觉太慢，可以试试将这个数值改小，比如2秒，或则5秒  
+ 如果发现连接失败率很高、工作不稳定时，就把数值改大  
+ 调整ip connect interval，需要一点耐心和探索精神，如果不知道怎么改，就不要动它  
  