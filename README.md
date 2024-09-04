# MDP REPRESENTATION

## AIM:

To represent a Markov Decision Process (MDP) for a robot arm that picks up a product and places it on a goal node

## PROBLEM STATEMENT:

Write  robot arm that picks up a product and places it on a goal node

### Problem Description
The problem is to develop a reinforcement learning agent that learns and finds the optimal policy for the task of pick 
### State Space

State Space : {s1(start),s2,s3,s4(goal)}
### Sample State
Sample State : Start

### Action Space
A 1 : Move arm to the product location. 

𝐴 2 : Pick up the product.

𝐴 3 : Move arm towards the goal node.

𝐴 4 : Place the product on the goal node.

### Sample Action
Sample Action : A2 Pick up yhe Product 

### Reward Function
Reward Function : { +1 , When reaching on the Goal State } Reward Function : { 0 , Otherwise }

### Graphical Representation

![image](https://github.com/user-attachments/assets/a2dfbacc-4c38-4a65-934d-5fe237eef9a3)
![image](https://github.com/user-attachments/assets/ff77e40c-21ee-4e80-8629-deeea9eedab8)


## PYTHON REPRESENTATION:
```python
p = {
    -1: {
        0:[(1.0,-1,0.0,True)],
        1:[(0.8,0,0.0,False),(0.2,-1,0.0,True)]
    },
    0: {
        0:[(0.8,-1,0.0,True),(0.2,0,0.0,False)],
        1:[(0.8,1,0.0,False),(0.2,0,0.0,False)]
    },
    1: {
        0:[(0.8,0,0.0,False),(0.2,1,0.0,False)],
        1:[(0.8,2,+1.0,True),(0.2,1,0.0,False)]
    },
    2: {
        0:[(1.0,2,0.0,True)],
        1:[(1.0,2,0.0,True)]
    }

}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/8d31bf01-4c43-463a-98ec-e57bd719d852)


## RESULT:
Thus the given real world problem is successfully represented in a MDP form.

