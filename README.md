# cxf-log

**The easier, the better!**

Modern c++(c++11), cross-platform, header-only, easy to use, the sample code:

```c++
#include <iostream>
#include "log.h"


int main()
{
	LOG->set_log_cb([](const TLogLevel log_level, const std::string& log) {
		std::cout << log << std::endl;
	});
	LOG->set_log_level(kLevelInfo);

 	DEBUG("str1", 2, "str3", 4.0);
 	INFO("str1", 2, "str3", 4.0);
 	WARN("str1", 2, "str3", 4.0);
 	ERR("str1", 2, "str3", 4.0);
 	FATAL("str1", 2, "str3", 4.0);
 	  
 	getchar();
 	  
 	return 0;
 }
```

**The output:**<br/>
[22:46:55.723] [INFO ] [cst_test.cpp main 211] - str1 2 str3 4 [tid:1236]<br/>
[22:46:55.723] [WARN ] [cst_test.cpp main 212] - str1 2 str3 4 [tid:1236]<br/>
[22:46:55.724] [ERROR] [cst_test.cpp main 213] - str1 2 str3 4 [tid:1236]<br/>
[22:46:55.724] [FATAL] [cst_test.cpp main 214] - str1 2 str3 4 [tid:1236]<br/>
