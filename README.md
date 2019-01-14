# SysbenchTree
Mysql性能测试


![](https://i.imgur.com/oJH3NGU.png)

<pre>
Sysbench测试步骤：
</pre>

<pre>
在执行sysbench时，应该注意：

    （1）尽量不要在MySQL服务器运行的机器上进行测试，一方面可能无法体现网络（哪怕是局域网）
        的影响，另一方面，sysbench的运行（尤其是设置的并发数较高时）会影响MySQL服务器的表现。

    （2）可以逐步增加客户端的并发连接数（--thread参数），观察在连接数不同情况下，MySQL服
        务器的表现；如分别设置为10,20,50,100等。

    （3）一般执行模式选择complex即可，如果需要特别测试服务器只读性能，或不使用事务时的性
        能，可以选择simple模式或nontrx模式。

    （4）如果连续进行多次测试，注意确保之前测试的数据已经被清理干净。
</pre>