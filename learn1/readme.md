# typescript笔记本

1. 类型注解 TypeScript里的类型注解是一种轻量级的为函数或变量添加约束的方式。

greeter.ts: 

`
function greeter(person: string) {...}
`

2. 接口：interface的添加及使用 greeter2.ts

3. 类：支持基于类的面向对象编程 greeter3.ts

```js
class Student {
  fullName: string
  // 构造函数
  constructor(public firstName, public middleInitial, public lastName) {
    this.fullName = firstName + ' ' + middleInitial + ' ' + lastName
  }
}

interface Person {
  firstName: string
  middleInitial: string
  lastName: string
}

function greeter(person: Person) {
  return 'Hello, ' + person.firstName + ' ' + person.lastName
}

let user = new Student('李', '冰', '泉')

document.body.innerHTML = greeter(user)
```