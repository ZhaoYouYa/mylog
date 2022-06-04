> Initially,I only write cpp code,but now,I also write C#，python,and javascript. I need a unidentified code style.

## 1. File Name

1. Typically, don't use uppercase. like `hello.h`, `hello.cs`, `hello.js`, and `hello.py` are better. 
2. Using uppercase is also OK, usually, that occurred when I use C# with asp.net.
3. `_` and `-` are forbid


## 2. Class 


1. `class name` The first letter is capitalized. Using CamelCase. the namespace name is the same style.
2. `variable member` the first word is `_`, The interval in words is also `_`, don't use uppercase. if the variable is a group type, use like `_s_name`.
3. `function member`. Using CamelCase. the first letter is not capitalized. even if in C#.


for example:

```cpp

class Human {
public:
    void eat();
    std::vector<GirlFriend> _s_girl_friend;
    std::string _name;

}

```


```C#
class Human 
{
    public void eat(){ //DO Eat};
    public List<GirlFriend> __s_girl_friend {get;set;}
    public string _name{get;set;};

}
```
4. let variable members in a region, and function members in another region.

`wrong`
``` javascript

<script setup>
const _name = ref('zhaolei')
function eat() {

}
let age = 10
</script>

```

`right`

``` javascript

<script setup>
const _name = ref('zhaolei')
let age = 10

function eat() {

}

</script>

``` 

## 3. other

1. `parameter` end with `_`, using CamelCase.
2. if I don't need a name with some meaning, use `_`,`1_`, and so on.

`CPP`

``` cpp
int add(int l_,int r_) {
    return l_ + r_;
}

for(auto& _:_s_girl_friend) {
    std::cout<<_._name();
}
```

`js`

``` javascript
arr.forEach(_=>{
    console.log(_)
    _.forEach(1_=>{
         console.log(1_)
    })

})
```



## 4. javascript in VUE

1. if a variable is a 'ref' value. using like `const _name = ref('ZhaoYouya')`, it is similar to variable members in a class.
2. usually, a variable name uses CamelCase style, the first letter is not capital. this has a good difference with 'ref' variables.



## 5. SQL Name.

1. `Table Name`. they have a prefix, and use `_` as a interval word. like `sys_user`
2. `Field Name` use CamelCase, the first letter is capital. 




