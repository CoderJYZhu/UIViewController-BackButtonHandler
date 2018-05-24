# UIViewController-BackButtonHandler

#####拦截UIViewController的popViewController事件


**使用**：
```

在UIViewController当中引入头文件
#import "UIViewController+BackButtonHandler.h"

在UIViewController中实现navigationShouldPopOnBackButton方法。
- (BOOL)navigationShouldPopOnBackButton{
    [[[UIAlertView alloc] initWithTitle:@"提示" message:@"确定返回上一界面?"
                               delegate:self cancelButtonTitle:@"取消" otherButtonTitles:@"确定", nil] show];
    //renturn no 拦截pop事件
    return NO;
}
```
