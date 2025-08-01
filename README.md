# 📖 *The Gospel According to SOLID*  
## Chapter 1. "S" — SRP: Single Responsibility Principle

---

## ✨ Preface: *In the beginning was the Code*  

> *"In the beginning was the Code, and the Code was with the Principle, and the Code was the Principle. It was in the beginning with the Architect. Through it all things were made; without it nothing was made that has been made. In it was Structure, and that Structure was the light of the team."*  
> *(SOLID Prologue 0:1)*

The Architect raised a Project and said:  
> *"Let there be an MVP!"*

And there was MVP.  
And it was without tests, and void, and dependencies moved upon the face of the legacy.

And the first man on earth committed `initial`, and named it “final”.

And lo, everything worked… until the product manager came.

From that day forward, began the Great Suffering — called **Technical Debt**.  
Methods grew like hydras, functions knew more than the CEO,  
and each `if` brought new heresy.

Then, through the spaghetti darkness, came a Principle.  
Its name was **S**.  
It bore a clear word, like a debug-level log, and declared:  
> *"To each class, its own burden. Mix not responsibilities, for that way lies chaos."*

---

## 🪐 I. The Emergence of SRP  

> *"And it was the morning of the first Principle, and he separated business from utility, data from presentation."*

SRP did not appear at once,  
but when it came, it was like a `clean_up()` in the `finally:` — a last chance to restore order.

Its message was simple:  
> *"Let each module have one reason to change."*

And thus went forth architects across the land,  
separating classes, purifying dependencies,  
creating layers as the Creator made heavens and earth.

---

## 🌱 II. The Formation of SRP  

> *"Take not unto thyself many tasks, for thy path will be tangled and thy logic unreadable."*

SRP is like monasticism: a voluntary limitation for the sake of purity.

Every righteous class must have:

- **A single goal**
- **One area of responsibility**
- **One reason to change**

Should a class take on more, it falls into **architectural pride**,  
and will collapse under its own weight.

---

## 🔥 III. A Parable of Fall and Redemption  

> *The Parable of the Programmer and the Almighty Class*

There was once a class named `UserManagerGod`,  
who did all things: create, delete, log, email... even launch missiles (allegedly).

One day, the client asked:  
> *"Can we filter users by activity?"*

The developer added `if` to `create_user()` and went off in search of caffeine,  
for the tests failed, logic broke, and the CI cried:  
> *"FAILED: TooMuchResponsibilityException"*.

Then came Tim, a junior of clean heart,  
and said:  
> *"Let us divide him, as God divided the light and the darkness."*

And he made:

```python
class UserCreator: ...
class PasswordEncrypter: ...
class EmailSender: ...
class Logger: ...
