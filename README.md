# Play-With-Interpreters-Scheme-
Here I have implemented scheme interpreter for lazy-eager evaluation together and Dynamic-Lexical scoping together.

Problem Statement :- 

Part A : Dual Scoping

In this part, you need to extend the interpreter kernel to have both lexical and dynamic scoping.
Specifically, a parameter may be declared to be dynamically scoped as:

```scheme
(define (foo
  (lambda (a (dynamic b))
   ( ... ))))
```

Similarly, a parameter may be dynamically referenced as:
```scheme
(define (foo
  (lambda (a (dynamic b))
   (+ a (dynamic-ref b)))))
```
Referencing a variable that wasn't declared as dynamically scoped, and referencing a dynamically scoped variable without `dynamic-ref`, should both default to lexical scoping.

Part B : Dual Evaluation Orders

In this part, you need to extend the provided interpreter kernel to have both eager and lazy evaluation.
Specifically, a parameter may be declared to be lazily evaluated as:

```scheme
(define (foo
  (lambda (a (lazy b))
   ( ... ))))
```

Now `b` should be evaluated lazily, upon need, and `a` should be evaluated eagerly.


parta.scm contains the code for part a
partb.scm contains the code for part b
