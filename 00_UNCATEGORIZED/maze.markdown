---
layout: post
title: 1-1 Example Maze
date: 2021-02-26 13:25:20 +0300
author: Alex2006
---
  
  
------
## 1. Maze
![MAZE](./img/maze.jpg)
  * Yellow: Start, Green: End, Gray: Wall, White: Pathway
  * Start에서 End까지 Path가 존재하는지를 Return


## 2. Recursive Thinking
  * 현재 위치가 출구 이거나
  * 이웃한 셀들 중 하나에서 현재 위치를 지나지 않고 출구까지 가는 경로가 있거나


## 3. Pseudo Code
  * Step1

```cpp
bool findPath(x, y)
    if (x, y) is the exit then
        return TRUE
    else
        foreach neighboring cell (x', y') of (x, y) do
            if (x', y') is on the pathway
                if findPath (x', y') then
                   return TRUE
    return FALSE
```
     **두가지가 결여되어 있다 (1)  Basecase, (2) Basecase로의 수렴**

  * Step2

```cpp
bool findPath(x, y)
    if (x, y) is either on the wall or visited cell then
        return FALSE
    else if (x, y)is exit then
        ... ...
    else
        mark(x, y) as a visited cell
        foreach neighboring cell (x', y') of (x, y) do
        ... ...
```

## 4. Problem
  * TBD

------