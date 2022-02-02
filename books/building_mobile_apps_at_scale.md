![cover](https://www.mobileatscale.com/assets/images/Book_Display.jpg)

    Gergely Orosz
    Abril 2021  
    ISBN 1638778868  
    236 pages

https://www.mobileatscale.com/

---

# Introduction
Most engineers who have not built mobile apps assume the mobile app is a simple facade that requires less engineering effort to build and operate. Having built both types of systems, I can say this is not the case.

**When the problem you are solving is simple, and the scope is small, it is easier to come up with simple solutions.**

# PART 1: Challenges Due to the Nature of Mobile Applications
People who have not done mobile development often assume that most challenges of native apps are similar to those on the web. This could not be further from reality.

## 1. State Management
The difference with mobile apps is how app lifecycle events and transitions are not a cause for concern in the web and backend world.

- **Events drive state changes in most mobile apps**. Most bugs and unexpected crashes are usually caused by an unexpected or untested combination of events and the application's state becoming corrupted. State becoming corrupted is a common problem area with apps where global or local states are manipulated by multiple components unknown to each other. Teams that run into this issue start to isolate component and application state as much as possible and tend to start using reactive state management sooner or later (preferred method for dealing with a large and stateful app, in order to isolate state changes).
- **Applications sharing the same resources with all other apps.** (CPU, memory...)
- **Global application state**. (Permissions, connectivity state...)
- **App launch points** (deeplink, push...)

## 2. Mistakes are hard to revert
- Both Apple and Google are strict on allowing executable code to be sent to apps.
- It takes from hours to days to release.
- Users take days to update to the latest version.
- You can not assume that all users will get this updated version, ever. Previous versions of your app need to be supported indefinitely.

What steps can you take to minimize bugs or regressions from occurring in old versions?
- **Do thorough testing** at all levels.
- **Have a feature flagging system**.
- **Consider gradual rollouts**.
- **Force upgrading** is a robust solution.

## 3. The Long Tail of Old App Versions


