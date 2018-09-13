# 快速排序
## 划分
给定一个数组以及一个枢纽数值，将小于或等于枢纽数值的元素移到左边，将大于或等于枢纽数值的元素移到右边，并返回划分位置。
```java
public int partition(int[] array, int pivot) {
  int left = -1;
  int right = array.length;
  while (true) {
    while (left < right && array[++left] < pivot);
    while (right > left && array[--right] > pivot);
    if (left >= right) {
      break;
    }
    swap(array, left, right);
  }
  return left;
}
```
测试：输入数据[2, 5, 8, 4, 6, 6, 3, 4, 6, 4, 1, 10]，pivot=5；

结果：6，[2,1,4,4,4,3,6,6,6,8,5,10]。可以知道，前6个数值的确小于5，而后面元素值都大于或等于5。
