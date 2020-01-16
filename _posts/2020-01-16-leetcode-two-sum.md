---
title:  "LeetCode Algorithm #1"
excerpt: "Two Sum"

categories:
  - Coding-Test
tags:
  - Coding-Test
  - Algorithm
last_modified_at: 2020-01-16 22:10

---
> ## 1. 문제 이해  
>> 오늘 제가 푼 문제는 **LeetCode** 의 **1번** 문제입니다.  
<br> Two Sum 이라는 제목의 문제는 입력값으로는 **정수형 배열**과, **정수**가 주어집니다.  
<br> 그리고 **덧셈**을 통하여 입력으로 받은 **정수**가 나오도록하는 **인덱스가 서로 다른 두 개의 원소**를 반환하는 문제입니다.  
<br> 그래서 제가 생각한 방법은 배열을 이중으로 돌면서 덧셈을 통해 반환해야하는 인덱스를 찾아 새로운 배열을 만들어서 해결하는 것이었습니다.

---

> ## 2. C++ 코드
>>```c++
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        for(int i=0; i<nums.size(); i++) {
            // i와 같은 인덱스에 대한 연산을 안하기 위해 j=i+1
            for(int j=i+1; j<nums.size(); j++) {
                if(nums[i] + nums[j] == target){
                    vector<int> indices;
                    indices.push_back(i);
                    indices.push_back(j);
                    return indices;
                }
            }
        }
        vector<int> fail;
        return fail;
    }
};
>>```

---

> ## 3. 정리
>> **코딩테스트**에서는 익숙한 **Python** 언어를 이용하기 보다는 **컴파일 언어여서 실행 시간이 빠르면서** 그나마 익숙한 언어인 **C++**을 이용했습니다.  
<br>위 문제에서 LeetCode는 C++ 언어에서의 **vector container**를 사용하여 답안을 제출하도록 제시하였습니다.
> 이 vector container에 대해서 제대로된 지식이 없어 간단하게 검색을 해본 결과,
>
> - vector의 size를 **동적**으로 조절이 가능하다.
> - ***다양한 메소드***를 사용할 수 있어 편리하다. 
>
>> 이 정도의 특징을 가지고있는 컨테이너라고 생각합니다.  
<br> 상황에 **알맞은 자료구조**를 선택하고 알고리즘을 생각하는 것 또한 코딩에서 중요하다고 생각합니다. 따라서 더 많은 자료구조를 공부하고, 많은 상황에서 써봄으로써
> 실력을 키워야한다고 느꼈습니다. 우선은 vector 컨테이너에 대해서 공부해봐야 할 것 같습니다.  
<br> 그리고, LeetCode에서는 다른 사람들의 코드를 비교할 수 있는 장점이 있었는데, 이를 통해 실행 시간이 빠른 코드를 살펴보니 map이라는 자료구조를 쓰는 것을 알 수 있었습니다.
> 그래서 Map부분도 공부하여 더욱 좋은 코드를 짜도록 노력해야겠다고 느꼈습니다.
