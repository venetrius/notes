# Priority Queue
-> remove will remove highest value

## preview:
## API and elementary implementations
header: public class MaxPQ<Key extends Comparable<Key>>
  MaxPQ()
  MaxPq(Key[] array)
  void insert(Key k)
  Key delMax()
  boolean isEmpty()
  // Key max()
  // int size()

## Applications:
event driven simulation
numerical computation
data compression
graph searching
etc...

Real Life Client example:
huge amount of data, we are looking for the biggest, but cannot store all of them

## implementations:
          insert   max      delMin
unsorted  1         N       N
sorted    M         1       1

