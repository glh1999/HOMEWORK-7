# Homework7

> 于佳艺 2017302580210

## P3.

在4. 2节中,我们注意到如果交换结构速率是输入线路速率的n倍，其最大的排队时延为(n-1)D>0 假设所有分组有相同长度，在相同时刻n个分组到达n个输出端口，同时所有n个分组要转发到不同的输出端口。对于内存、总线和纵横式交换结构，一个分组的最大时延是多少？ 

解：内存结构：(n-1)D

总线结构：(n-1)D

纵横式交换结构：0

## P5.

考虑使用32比特主机地址的某数据报网络。假定一台路由器具有4条链路。编号为0~3,分组能被 转发到如下的各链路接口： 

|            目的地址范围             | 链路接口 |
| :---------------------------------: | :------: |
| 11100000 00000000 00000000 00000000 |          |
|                 到                  |    0     |
| 11100000 00111111 11111111 11111111 |          |
| 11100000 01000000 00000000 00000000 |          |
|                 到                  |    1     |
| 11100000 01000000 11111111 11111111 |          |
| 11100000 01000001 00000000 00000000 |          |
|                 到                  |    2     |
| 11100001 01111111 11111111 11111111 |          |
|                其他                 |    3     |

a. 提供一个具有5个表项的转发表，使用最长前缀匹配，转发分组到正确的链路接口。 

b. 描述你的转发表是如何为具有下列目的地址的数据报决定适当的链路接口的。 

11001000 10010001 01010001 01010101 

11100001 01000000 11000011 00111100 

11100001 10000000 00010001 01110111

解：a.

|   目的地址范围    | 链路接口 |
| :---------------: | :------: |
|    11100000 00    |    0     |
| 11100000 01000000 |    1     |
|      1110000      |    2     |
|    11100001 1     |    3     |
|       其他        |    3     |

b.利用最长前缀匹配原则来决定链路接口：

11001000 10010001 01010001 01010101 ：接口3

11100001 01000000 11000011 00111100 ：接口2

11100001 10000000 00010001 01110111：接口三

## P6.

考虑使用8比特主机地址的某数据报网络。假定一台路由器使用最长前缀匹配并具有下列转发表:

|   目的地址范围    | 链路接口 |
| :---------------: | :------: |
| 00000000~00111111 |    0     |
| 01000000~01011111 |    1     |
| 01100000~01111111 |    2     |
| 10000000~10111111 |    2     |
| 11000000~11111111 |    3     |

对这4个接口中的每个，给出相应的目的主机地址的范围和在该范围中的地址数量。

解：

接口0的地址数量：2^6 = 64个
接口1的地址数量：2^5 = 32个
接口2的地址数量：2^5+2^6 = 96个
接口3的地址数量：2^6 = 64个