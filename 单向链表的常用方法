class Node(object):
    def __init__(self,elem):
        self.elem = elem
        self.next = None
class Linklist(object):
# 初始化头结点
    def __init__(self,node=None):
        self.__head = node
# 判断是否为空
    def is_empty(self):
        return self.__head == None
#获取链表的长度，增加游标和数量变量
    def length(self):
        cur = self.__head
        count = 1
        while cur != None:
            count += 1
            cur = cur.next
        return count
# 遍历链表
    def travel(self):
        cur = self.__head
        while cur != None:
            print(cur.elem)
            cur = cur.next
# 头部添加元素
    def add(self,item):
        node = Node(item)
        node.next = self.__head
        self.__head = node
# 尾部插入元素，尾插法
    def append(self,item):
        node = Node(item)
        # 排除链表为空的情况
        if self.__head == None:
            self.__head = node
        else:
            cur = self.__head
            while cur.next != None:
                cur = cur.next
            cur.next = node
# 中间插入，要在所指定位置的前一个区域插入元素，
    def insert(self,pos,item):
        if pos <= 0:
            self.add(item)
        # 如果所选位置 大于 在总长度位置，则执行尾插法
        elif pos >= (self.length()-1):
            self.append(item)
        else:
            cur = self.__head
            count = 0
            node = Node(item)
            while count < (pos-1):
                count += 1
                cur = cur.next
            node.next = cur.next
            cur.next = node
            # 循环退出后，cur指向pos-1的位置

# 查找
    def search(self,item):
        cur = self.__head
        while cur != None:
            if cur.elem == item:
                return True
            else:
                cur = cur.next
        return False
# 删除元素
    def remove(self,item):
        cur =self.__head
        pre = None
        while cur != None:
            if cur.elem == item:
                if cur == self.__head:
                    self.__head = cur.next
                else:
                    pre.next = cur.next
                # 删除完元素，要跳出循环，
                break
            else:
                pre = cur
                cur = cur.next

        return item


if __name__ == '__main__':
    ll = Linklist()
    print(ll.is_empty())
    ll.append(5)
    ll.add(3)
    ll.insert(1,200)
    ll.travel()
    ll.remove(200)
    ll.travel()













