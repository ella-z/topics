# 实现mutiply函数
- 题目
```
mutiply(2,3).result = 6
mutiply(2,4)(2)(3,1).result = 48
//实现这个mutiply函数
```
- 解法一：
```
const mutiply=(...params)=>{
                        const func=(...params)=>{
                            for (let num of params){
                                if(isNaN(num)){continue;}
                                Function.prototype.result*=num;
                            }
                            return func
                        }
                        Function.prototype.result=1;
                        return func(...params);
                    }
```
- 该解法的缺陷是函数执行完成之后，result会遗留在Function.prototype中。
