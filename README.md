# SinglyLinkedList
A singly linked list , Objective-C.


## 节点类：MMNode
```
@interface MMNode : NSObject

@property (nonatomic, assign) int data;//节点数据
@property (nonatomic, strong) MMNode *next;//下一个节点

@end
```
## 单链表类：MMList
```
@interface MMList : NSObject

@property (nonatomic, strong) MMNode *head;//首节点
@property (nonatomic, strong) MMNode *hail;//尾节点

//初始化
- (instancetype)initWithData:(int)data;

//增加节点
- (void)append:(int)data;

//输出
- (void)printList;

//指针逆转
- (void)reverse;

@end
```
## main函数

```
int main(int argc, const char * argv[]) {
    @autoreleasepool {
        
        MMList *list = [[MMList alloc] initWithData:0];
        //刚初始化的链表，首节点即尾节点
        NSLog(@"首节点数据：%@ ；尾节点：%@",list.head,list.hail);
        
        //新增数据
        for (int i = 1; i < 10; i++) {
            [list append:i];
        }
        NSLog(@"首节点数据：%@ ；尾节点：%@",list.head,list.hail);

        //输出
        [list printList];
    }
    return 0;
}
```


thanks !

