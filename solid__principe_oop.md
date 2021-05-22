Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@Slab3 
Slab3
/
useful
forked from YauhenKavalchuk/useful
0
076
Code
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
useful
/
solid.md
in
main
 

Tabs

8

Soft wrap
1
​
2
## **SOLID**
3
​
4
### [YouTube: Просто о SOLID (Принципы ООП)](https://youtu.be/A6wEkG4B38E)
5
---
6
​
7
### Single responsibility principle
8
​
9
👎**Bad:**
10
​
11
```javascript
12
class Auto {
13
        constructor(model: string) { }
14
        getCarModel() { }
15
        saveCustomerOrder(o: Auto) { }
16
        setCarModel() { }
17
        getCustomerOrder(id: string) { }
18
        removeCustomerOrder(id: string) { }
19
        updateCarSet(set: object) { }
20
}
21
```
22
​
23
👍**Good:**
24
```javascript
25
class Auto {
26
        constructor(model: string) { }
27
        getCarModel() { }
28
        setCarModel() { }
29
}
30
​
31
class CustomerAuto {
32
        saveCustomerOrder(o: Auto) { }
33
        getCustomerOrder(id: string) { }
34
        removeCustomerOrder(id: string) { }
35
}
36
​
37
class AutoDB {
38
        updateCarSet(set: object) { }
39
}
40
```
41
​
42
### Open/closed principle
43
​
44
👎**Bad:**
45
​
Файл не выбран
Attach files by dragging & dropping, selecting or pasting them.
@Slab3
Commit changes
Commit summary
Create solid.md
Optional extended description
Add an optional extended description…
 Commit directly to the main branch.
 Create a new branch for this commit and start a pull request. Learn more about pull requests.
 
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
