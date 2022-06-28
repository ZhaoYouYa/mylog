- [1. The features of C#](#1-the-features-of-c)
  - [1.1 The features why you use C#](#11-the-features-why-you-use-c)
  - [1.2 The language features](#12-the-language-features)
- [2. Linq](#2-linq)
  - [2.1 Some examples](#21-some-examples)
    - [2.1.1 Aggregate String](#211-aggregate-string)

## 1. The features of C#

### 1.1 The features why you use C#

1. If you have experience in writing c++, c# is very easy for you.
2. C# is not a community language, it belongs to Microsoft. so, there are many great packages like asp. net, EF-Core, and so on for C#. Microsoft had decided that C# is their **first** language.
3. Not a system language, but C# has enough high speed.
4. C# has a big surface, sometimes, it causes a little confusion, but as a direct result, it can build apps in a great variety.


### 1.2 The language features

1. `Linq` queries many types of data sources. It's very very helpful.



## 2. Linq

> Maybe, It's the only reason why I use C#.

### 2.1 Some examples

#### 2.1.1 Aggregate String

> At two list, group one by other, aggregate some value

```csharp
record r1(int groupId,string mark);

record r2(int id);

var  _s_r1= new List<r1>{

    new r1(1,"a"),
    new r1(1,"b"),
    new r1(1,"c"),
    new r1(2,"d")

};

var _s_r2 = new List<r2> {
    new r2(1),
    new r2(2),
    new r2(3)
};

var item =from i in _s_r2
          join j in _s_r1 on i.id equals j.groupId into temp
          select new {
              id = i.id,
              str = (

                    from k in temp
                    where k.groupId == i.id
                    select k.mark
              ).Aggregate("-- ",(Sum,next)=>$"{Sum}{(Sum=="-- "?"":";")}{next}",Finalresult=>Finalresult+" **")
          };
foreach (var s in item)
{
    
        Console.WriteLine(s.str);

}
// The Result
// -- a;b;c **
// -- d **
// --  **

```
