# MDP REPRESENTATION

## NAME : GOKUL C
## REG NO : 212223240040

## AIM:
To Mapping a Real-World Problem to a Reinforcement Learning Problem.

## PROBLEM STATEMENT:

### Problem Description

The problem of robotic warehouse management can be formulated as a Reinforcement Learning (RL) problem. Efficient warehouse automation 
using robots can reduce order processing times, optimize storage, and improve operational efficiency. The goal is to dynamically allocate tasks 
to robots, optimize their movement, and minimize congestion in the warehouse.

### State Space


The state space represents the current conditions in the warehouse, including:
 
Position of robots in the warehouse grid.
 Location of items to be picked up.
 Status of shelves (occupied or empty).
 Traffic congestion in different zones.
 Number of pending orders.  

### Sample State

A possible state representation:
 
Robot Positions: Robot 1 at (3,5), Robot 2 at (7,2).
 Item Locations: Item A at (4,8), Item B at (2,6).
 Shelf Status: Shelf 1 occupied, Shelf 2 empty.
 Traffic Congestion: High in zone (5,5), Low elsewhere.
 Pending Orders: 5 orders waiting for fulfillment.

### Action Space

The action space consists of different robot control options:
 
Move robot in a direction (e.g., up, down, left, right).
 Pick up an item from a shelf.
 Drop an item at a designated packing station.
 Wait if no optimal move is available.

### Sample Action

A possible action could be:
 
Move Robot 1 from (3,5) to (4,5) to approach Item A

### Reward Function


The reward function incentivizes optimal task completion while minimizing delays and congestion:
 
 
Positive Rewards:
 
Successful item pickup (+5 reward).
 Order completion (+10 reward).
 Efficient path selection (shorter distance traveled = +2 reward).

 Negative Rewards:
 
Robot collision (-5 penalty).
 Unnecessary movement (-2 penalty for extra steps).
 Congestion in high-traffic zones (-3 penalty for crowding).

### Graphical Representation

![WhatsApp Image 2025-03-14 at 14 29 49_5d5d47b7](https://github.com/user-attachments/assets/b393eed4-a818-47fe-99c5-8d875c1cf8ff)



## PYTHON REPRESENTATION:

```
p={
    1:
    {
        0: [(0.8,2,0.0,True),(0.2,3,-5.0,True)],
        1: [(0.2,3,-5.0,True),(0.8,2,0.0,True)]
    },
    2:
    {
        0: [(0.7,3,0,True),(0.3,1,-3.0,True)],
        1: [(0.3,1,-3.0,True),(0.7,3,0,True)]
    },
    3:
    {
        0: [(1.0,2,+5.0,True)],
        1: [(1.0,1,+10.0,True)]
    },
}
```

## OUTPUT:

![Screenshot 2025-03-14 132544](https://github.com/user-attachments/assets/23d86cbb-e20c-42e9-82c3-46d7eebf0328)


## RESULT:

Thus, the given real-world problem of choosing the robotic warehouse management is successfully represented in MDP form.
