# 🏫 edulink for Python

A Python library that allows you to seamlessly communicate with the [EduLink One](https://www.edulinkone.com) API from within Python.

It handles all authentication and the little things in the background for you. 😌

> EduLink One is a whole school solution designed for teachers, parents and students to effectively colaborate in a user-friendly mobile and web app.

The EduLink One API is completely proprietary and undocumented, so the creation of this package required some reverse engineering.

Please note that this is **NOT** a full-fledged integration of the EduLink API. This library is incredibly limited and does not provide certain API methods such as teacher methods. **Only the student calls have been implemented**.

~~If you require an additional feature in this library, please create an issue and it will be added on-demand.~~

> [!IMPORTANT]  
> This library is no longer maintained and will likely be in bad shape if EduLink One ever changes their API response structure, etc.
>
> I, the creator, am no longer enrolled in an educational institution which actively uses EduLink One, so I can no longer provide any updates.

## Installation

There are no plans to put this library onto PyPI (pip).

Installation is therefore as simple as copying [`/src/edulink/__init__.py`](./src/edulink/__init__.py) to wherever your Python project is, and renaming it to `edulink.py`.

## 🔨 Usage

Using this library is fairly simple, it involves creating a student object, authenticating, and then using it normally.

```py
from edulink import Student

me = Student()

me.authenticate("Username", "Password", "School Postcode")

print(me.timetable()) # Prints timetable in dictionary form
```

~~Documentation for this package will be created at a later date.~~

## Why the GPL License?

The research I put into this project is not worth putting into closed-source projects, and the EduLink One API is already proprietary enough without documentation, so let's not add to that.

## ⚠️ Disclaimer

This package is the result of ***reverse engineering efforts***...

...to understand the communication protocol between the client application and the EduLink One API itself. The EduLink One API is proprietary and undocumented. Although the intention behind this package is to facilitate seamless integration with Python and to explore for educational purposes how applications are built, it is important to be aware of potential legal implications.

Please use this package at ***your own risk***.

***Unauthorised access of certain school systems can become problematic***. Please stay within your student boundaries when using the API and do not attempt to access things you should not.

----------

I, the author, its contributors, and maintainers are not responsible for any actions, legal consequences, or issues that may arise as a result of using this package. Users are advised to review the Terms of Service and licensing agreements of EduLink One by Overnet Data Ltd. before incorporating this package into proper production projects.
