---
title: 'Mastering the Art of Naming in Code'
description: 'An Article based on the Clean Code methodology.'
pubDate: 'Jul 01 2023'
heroImage: '/naming-things-in-code.jpg'
---

One of the hallmarks of a professional developer is their ability to write clean, understandable code. A significant part of achieving this is naming things correctly. Names in your code should communicate intent, usage, and behavior efficiently and effectively. In this post, we'll walk through some essential rules and practices for naming conventions in code.

## Best Practices for Naming in Code

### 1. Never Abbreviate Names

Abbreviations can be cryptic and lead to confusion. It's better to be explicit. The few seconds you save typing an abbreviation can turn into hours of lost productivity and misunderstandings down the line.

```ts
// Bad practice.
String m = "movie";
// Good practice.
String movie = "movie";
```

### 2. Don't Put Types in Names

Embedding types into names can be misleading and reduces readability. The type or role of a class should be apparent from the context and its behavior, not its name suffix or prefix.


```ts
// Bad practice.
interface IUser { }
// Good practice.
interface User { }
```
### 3. Avoid Naming Classes Base or Abstract

Names like Base or Abstract don't convey the responsibility of the class. They are generic and do not describe what the class actually does or represents.

Instead of:

```ts
// Bad practice.
class BaseAdapter { }
abstract class AbstractHandler { }
// Good practice.
class MessageAdapter { }
abstract class RequestHandler { }
```
### 4. Refactor If You Name Code Utils or Helpers

If you find yourself using names like Utils or Helpers, it's often a signal that your code needs refactoring. These names can be too generic and indicate that the class or method is doing too much or isn't focused enough.

Split large utility classes into smaller, more focused classes that describe their purpose clearly.

### 5. Put Units in Names

Omitting units can lead to misunderstandings and errors. It's critical to communicate what kind of measurement is expected.

```ts
// Bad practice.
void execute(int delay) { }
// Good practice.
void execute(int delaySeconds) { }
```
### 6. Classes and Objects Should Have Noun Names

Classes and objects represent entities and should be named accordingly, using nouns which describe what they represent.

```ts
class Customer { }
class Account { }
class AddressParser { }
```

### 7. Methods Should Have Verb or Verb Phrase Names

Methods perform actions and thus their names should be verbs or verb phrases.
```ts
void postPayment() { }
void deletePage() { }
void save() { }
```

### 8. One Word per Concept

Consistency is key to readability. For a given concept, choose one word and stick with it throughout your codebase.

Using synonyms like fetch, retrieve, get, or manager and controller interchangeably can cause confusion. If you start with fetch, always use fetch.

```ts

void fetchPages() { }
void fetchUserInfo() { }

```

### Conclusion

By following these conventions, you ensure that your code remains understandable and maintainable. Clear and consistent naming makes collaboration easier and increases the longevity of your codebase. Remember, the goal of naming things in code is to create a shared vocabulary that everyone on your team can understand and use productively. Happy coding!
