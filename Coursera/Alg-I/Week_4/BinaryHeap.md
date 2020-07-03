#Binary Heap ( An alg to implement priority que )
=> Array representation of a heap-ordered complete binary tree

- complete: perfectly balanced (except bottom level) === height ~ lgN
- heap-ordered: Parent's key no smaller then children's keys
    storing in array:
    i 0 1 2 3 4 5 6 7 8 9 10 11
      - T S R P N O A E I H C G

     well it is hard to draw here
    lvl 1 2 2 3 3 3 3 3 4 4 4 4

    a parent of a node at k is at k/2
    children of a node k are at 2k and 2k+1

- promotion:
  resolving an ambiguity when child key is higher than the parent key
  exchange key in child with key in parent
  repeat until hear order is restored

  function implementation:
    private void swim(int k) {
      while(k > 1 && less(k/2, k)) {
        exch(k, k/2);
        k = k/2
      }
    }

- insertion:
public void insert(Key x) {
  pq[++ N] = x;
  swim(N);
}

- demotion:
 a case when a parent changes (for whatever reason) and becomes smaller than any of its children
 move stronger child up and repeat until ex parent is not smaller than any of it child
 private void sink(k) {
   while(2 * k <= N ) {
     int j = 2 * k
     if (j < N && less(j, j+1>)) j++
     if (!less(k,j)) break;
     exh(k,j);
     k = j;
   }
 }

- Delete the max value
public Key delMax() {
  Key msx = pq[1]
  exch(1, N--);
  pq[N+1] = null;
  sink(1);
  return max;
}


Review of data structure implementations
implementation  insert  del-max       max
unordered a        1        N          N
ordered a          N        1          1
binary heap        logN     logN       1
// d-ary heap      log(d)N   dlog(d)N   1
//Fibonacci         1       logN@      1        (@ amortized)
// impossible       1       1          1


best practices
- use immutable keys
- underflow and overflow error deleting from empty and resizing full
