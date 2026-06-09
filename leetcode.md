
### 链表反转







常见jdk api总结：
数组拷贝
System.arraycopy(original,originalStart,current,currentStart,length);

list remove元素 remove方法重载 按元素值进行删除/ 按照下标index删除

随机Random random.nextInt(a)  生成[0,a)之间的随机整数


https://leetcode.cn/problems/add-strings/description/
在 Java 中，当传入 char 类型和 String 类型时，Integer.valueOf() 会执行完全不同的逻辑：字符 '9'（对应 char）：
会返回其对应的 ASCII 码值（即整数 57）。字符串 "9"（对应 String）：会解析该字符串，返回其实际的数值（即整数 9）。


```  快速排序模版 
public void quickSort(int[] nums,int start,int end){
        if(start>=end){
            return;
        }
        int left =start;
        int right= end;
        int pivot = nums[(start+end)>>1];
        while(left<=right){
            while(left<=right&&nums[left]<pivot){
                left++;
            }
            while(left<=right&&nums[right]>pivot){
                right--;
            }
            if(left<=right){
                swap(nums,left++,right--);
            }
        }
        quickSort(nums,start,right);
        quickSort(nums,left,end);
    }
```

```
摩尔投票法，给定一个数组，找到里面出现次数超过n/2的元素。众数
1、遍历数组的每一个元素，如果当前票数等于0 ，则假设当前元素为众数，
2、如果当前元素等于当前众数 票数+1，否则票数 -1
3、最终的众数就是真正的众数结果

int res =0;
int votes= 0;
for(int i=0;i<nums.length;i++){
  if(votes==0){
    res = nums[i];
  }
  votes+=nums[i]==res? 1:-1;
}
return res;

```

最大单词长度乘积  
判断两个单词有没有相同的字符，可以通过掩码的方式判断 按位与进行判断，这个思想类似于 将sku存到roaringbitmap位图中进行集合求交的优化
https://leetcode.cn/problems/maximum-product-of-word-lengths/




