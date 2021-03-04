                                 op如何跑GPU和CPU性能和精度

一：以matmul为例（测试matmul速度）

命令：bash tests_v2/run.sh matmul 0 speed

matmul相关配置文件：

1：tests_v2/configs/matmul.json是case输入输出等配置，通过修改json文件输入shape进行调整输入大小；

2： tests_v2/matmul.py是op执行文件，只需关注里面的PDMatul方法，TF和pytorch方法可忽略；

二：以matmul为例（测试matmul精度）

bash tests_v2/run.sh matmul 0 accuracy

matmul相关配置文件：

1：tests_v2/configs/matmul.json是case输入输出等配置，通过修改json文件输入shape进行调整输入大小；

2： tests_v2/matmul.py是op执行文件，只需关注里面的PDMatul方法，TF和pytorch方法可忽略；

repeated次数以及反向是否开启可通过配置tests_v2/run.sh进行配置；
