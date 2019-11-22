# sicp chapter by chapter
Initially, I'll work through only the sections covered in Brian Harvey's course syllabus found [here](./harvey_notes_and_syllabus.pdf).

## chapter 1: building abstractions with procedures

### introduction
* Computers are magical so programmers must be magicians.
* LISP is the best language ever.
* The history of LISP.

### 1.1 the elements of programming
* the mechanisms of any programming language are
  - primitive expressions
  - means of combination
  - means of abstraction

* there are two kinds of elements:
  - procedures
  - data

#### 1.1.1 expressions
Introduction to Scheme
  - another helpful resource is "The Little Schemer"
  - https://en.wikipedia.org/wiki/Polish_notation
  - many terms introduced, see glossary
  - NB:  even the operand of a combination can itself be evaluated from an expression
   e.g  . (cond (true) +) 1 1)`

#### 1.1.2 naming and environment
  - scheme uses `define` to correlate values to names
  - the interpreter stores these correlations in an 'environment'

#### 1.1.3 evaluating combinations
The combination evaluator is itself recursive in nature.  The first call evaulates the top level expression, and it will invoke itself for subexpressions as well.

`(define x 3)` is not a combination, but is a `special form`
> each special form has its own evaluation rule

> Syntactic sugar causes cancer of the semicolon. - Alan Perlis

#### 1.1.4 compound procedures
* With `define`, we can name new procedures made out of built-in procedures and expressions.  Define does two things:
    - creates a new procedure
    - gives it a name by which it can be referred
* This produces a _compound procedure_ because the new procedure itself contains another procedure, e.g. `(define (square x) (* x x))`
* It's important to keep these two things (creating a new procedure and naming that procedure) distinct because eventually we will create procedures without giving them names.

#### 1.1.5 The Substitution Model for Proecure Application
* The Substitution model is one of many to be presented in SICP.
* Now that we have procedures whose bodies are also procedures to be evaluated, a question arises about the order of evaluation.  In the procedure that sums two squares, `(sum-of-squares (+ 5 1) (* 5 2))`, should the evaluator invoke `sum-of-squares` first and handle the evaluation of `(+ 5 1)` and `(* 5 2)` later?  Or should it first evaluate (+ 5 1) and (* 5 2) and then invoke `(sum-of-squares 6 10)`?  The former is called **Normal-Order Evaluation** (a.k.a. lazy evaluation, because it waits until the operands are needed to evaluate them) and the latter is **Applicative-Order Evaluation**.
* LISP/Scheme uses applicative-order evaluation.


(Not sure where to put this yet but very useful)
Scheme programs are made of:
* self-evaluating elements:  `"hello world", 38, #t`
* names:  `+, x`   (where x is defined `(define x 3)`)
* combinations: `(+ 1 2)`, `(* x x)`
* special forms: `(define x 3)`, `(lambda (y) (* 2 y))`,
```
  (cond
    ((< x 5) "less")
    ((> x 5)) "more")
    ((= x 5)) "equal")
```


### 1.3
### 1.2 - 1.24
### 2.1 & 2.2.1
### 2.2.2-2.2.3, 2.3.1, 2.3.3
### 2.4-2.5.2
### 3.1, 3.2
### 3.3.1-3.3.3
### 3.4
### 3.5.1-3.5.5
### 4.1 metacircular evaluator
### 4.2, 4.3
### 4.4.1-3
