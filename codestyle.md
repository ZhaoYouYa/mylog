> Initially,I only write cpp code,but now,I also write C#，python, and javascript. I need an unidentified code style.


## 1. Dir Name

There are no special styles, any style is OK, but all dir names should have the same style. 

## 2. File Name

1. Typically, don't use uppercase. like `hello.h`, `hello.cs`, `hello.js`, and `hello.py` are better. 
2. Using uppercase is also OK, usually, that occurred when I use C# with asp.net.
3. `_` and `-` are forbid


## 3. Class or Region


1. `class name` The first letter is capitalized. Using CamelCase. the namespace name is the same style.
2. `variable member` the first word is `_`, The interval in words is also `_`, don't use uppercase. if the variable is a group type, use like `_s_name`.
3. `function member`. Using CamelCase. the first letter is not capitalized, but in C#, the first letter can be capitalized.


for example:

`cpp`
```cpp

class Human {
public:
    void eat();
    std::vector<GirlFriend> _s_girl_friend;
    std::string _name;

}

```

`C#`

```C#
class Human 
{
    public void eat(){};
    public List<GirlFriend> _s_girl_friend {get;set;}
    public string _name{get;set;};

}
```
4. let variable members in a region, and function members in another region.

`bad`
``` javascript

<script setup>
const _name = ref('zhaolei')
function eat() {

}
let age = 10
</script>

```

`good`

``` javascript

<script setup>
const _name = ref('zhaolei')
let age = 10

function eat() {

}

</script>

``` 



5. `[Vue]`if a variable is a 'ref' value. using like `const _name = ref('ZhaoYouya')`, it is similar to variable members in a class.
6. `[Vue]`usually, a variable name uses CamelCase style, the first letter is not capital. this has a good difference with 'ref' variables.

## 4. Function and Lambda

1. `parameter` end with `_`(for no other need), using CamelCase.
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

## 5. SQL Name.

1. `Table Name`. they have a prefix, and use `_` as an interval word. like `sys_user`
2. `Field Name` use CamelCase, the first letter is capital. 




