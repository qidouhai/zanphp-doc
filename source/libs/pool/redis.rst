Redis
-----

获取redis连接可以采用连接池，服务启动时初始化好redis连接。

配置
~~~~

redis连接配置在项目 resource/config/$ENV/connection下。

.. code:: php

    <?php
    return [
        'default_write' => [
            'engine'=> 'redis',
            //redis server的host和port
            'host' => '127.0.0.1',
            'port' => 6379,
            'pool'  => [
                'keeping-sleep-time' => '10',
                'init-connection'=> '2',
            ],
        ],
    ];

注：redis server支持unix socket连接方式，只需将host和port设置改为‘path’
=> 'unix socket path'即可。

 
