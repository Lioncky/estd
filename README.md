# estd
Exquisite and easy standard extension for basic types

## Manual
Add `vscprintf` to fix `_vscprintf` "%S" return -1,
also `exxsprintf` let sprintf more flexible

## Using
> `#include<estd.h>` and build the world!!!
>
> The Json parser speed as faster as `strlen`, enjoy!
>
> estr is useful for Win32 api with disposable towide
>
> estrs is a splitter contains the estr array
>
> all class comply with **RAII**
> 

> `estr (deep copy ONLY)`
> ```cpp
> // estr
> estr tmp("%d%S", 123, L"456");
> tmp = tmp + "789" + "ABCDEF";
> printf(*tmp);
> 
> dbk("Done!");
> ```
> ![image](https://github.com/KsaNL/estd/assets/73447685/15225cd3-73c7-481f-b747-87248ac2ea9f)

> `estrs` 
> ```cpp
> // estrs 
> estrs tmp("123 456 789", " ");
> 
> dbk("Done!");
> ```
> ![image](https://github.com/KsaNL/estd/assets/73447685/9cc6710e-f3eb-40e7-b6f7-ebf65dfacd1a)

> `ejson`
> ```cpp
> // ejson
> ejson ej(R"({
>     "data": {
>         "app_enabled": true,
>         "app_good": true,
>         "app_initialized": true,
>         "good": true,
>         "online": true,
>         "member": ["aaa","bbb","ccc"],
>         "stat": {
>             "packet_received": 16598,
>             "packet_sent": 14505,
>             "packet_lost": 0,
>             "message_received": 1914,
>             "message_sent": 135,
>             "disconnect_times": 0,
>             "lost_times": 0,
>             "last_message_time": 1689350878
>         }
>     },
>     "message": "",
>     "retcode": 0,
>     "status": "ok"
> })");
> 
> ejs& js = ej["data"];
> if (js) {
>   printf("this is a member!\n");
> }
> int _i = ej["data"]["stat"]["message_sent"];
> printf("_i %d", _i);
> ```
> ![image](https://github.com/KsaNL/estd/assets/73447685/70ff2fc9-1c79-4c74-b266-599ac0bf1e1f)


## Debug

> You can use Visual Vtudio debugger by copy *.nativs to, 
```
> VS2019
C:\Program Files (x86)\Microsoft Visual Studio\2019\Professional\Common7\Packages\Debugger\Visualizers
```

> OR 
```
> VS2022
"C:\Program Files\Microsoft Visual Studio\2022\Professional\Common7\Packages\Debugger\Visualizers"
```

## Future
- [x] estr support plus const char*

- [x] Json basic parser
- [x] Json support Obj array
- [x] Json support Number array
- [x] Json support String array
- [] Json support bool array
- [] Json support parse float array
