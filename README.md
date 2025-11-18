# MDP REPRESENTATION

## AIM:
To represent a Markov Decision Process(MDP) problem in the following ways.

i) Text representation
ii) Graphical representation
iii) Python - Dictonary representation

## PROBLEM STATEMENT:

### Problem Description
The problem is to develop a Reinforcement Learning model for product detection in a manufacturing factory. The model should determine whether a product is ready to be exported or faulty based on its features. The goal is to optimize the production process and reduce the number of faulty products while maximizing the number of products ready for export.

### State Space
S_wait(0)	Wait State	Main signal is Red (on phase 0).
S_go(1)	Go State	Main signal is Green (on phase 1).
S_neighbour(x)	Neighbor State	State is influenced by the neighbor's signal status (x).
  
### Sample State
(Low Congestion, Queue Length 5, Neighbor Signal Red)

### Action Space
A_0,Set main signal to Red and the cross-road signal to Green.
A_1,Set main signal to Green and the cross-road signal to Red.

### Sample Action
is A_1: Set main signal to **Green** and the cross-road signal to **Red**.

### Reward Function
If Congestion(t+1) < Congestion(t) implies R = +1

If Queue_len(t+1) < Queue_Len(t) implies R = -n.

### Graphical Representation
<img width="814" height="1280" alt="image" src="https://github.com/user-attachments/assets/ae817d3b-e4ac-4879-904e-08a412034da2" />

## PYTHON REPRESENTATION:
```python
P = {
    0:{
        0: [(1.0,0,0.0,True)],
        1: [(1.0,0,0.0,True)]
    },
    1:{
        0: [(1.0,0,0.0,True)],
        1: [(1.0,2,1.0,True)]
    },
    2:{
        0: [(1.0,2,0.0,True)],
        1: [(1.0,2,0.0,True)]
    }
}
```
## OUTPUT:
```python
{0: {0: [(1.0, 0, 0.0, True)], 1: [(1.0, 0, 0.0, True)]},
 1: {0: [(1.0, 0, 0.0, True)], 1: [(1.0, 2, 1.0, True)]},
 2: {0: [(1.0, 2, 0.0, True)], 1: [(1.0, 2, 0.0, True)]}}
```
## RESULT:
Thus the given Markov Decision Process(MDP) problem is represented in the following ways.

1) Text representation
2) Graphical representation
3) Python - Dictonary representation
