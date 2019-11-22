# glossary of terms in SICP

* **applicative order evaluation**

* **arguments** - values that derive from evaluated operands in an expression

* **compiler**

* **expression** - a representation of procedure or data that can be evaluated to a value (e.g. 3 yields 3, + yields a procedure)

* **combination** - a list of expressions within parentheses, the leftmost element is an operator, and the remaining elements are operands.  e.g. `(+ 1 2 3)`  but NOT `(define x 3)` because define is not an operator to be applied to its operands.

* **interpreter**

* **normal order evaluation** - Normal order (aka Lazy Eval) is the application of the procedure on stand-ins-for-arguments until the argument is needed.  This is bad because arguments will sometimes be calculated multiple times (ad hoc when each is needed) but good because sometimes arguments are rarely or never needed depending on program flow.  Contrast with _applicative order evaluation_.

* **prefix notation** - a.k.a. polish notation, wherein the operator comes first in order, e.g. instead of "2 + 3 -> 5", "(+ 2 3) -> 5"

* **procedure**

* **process**

* **recursive process vs recursive procedure** - A recursive procedure means only that the procedure refers to itself, but actual execution (in Scheme at least) is tail-recursive, meaning when it calls itself, it needs no call stack and can be executed in constant space.
A recursive process on the other hand will require departures from each caller to the callee and the saving of a call stack.


* **repl** - read-eval-print loop.   a terminal prompt for the interpreter which evaluates expressions entered.

* **semantics**

* **syntax**

* **tail recursion** - Tail recursion occurs when the final result of a procedure call ( call it `<procA>`) is a call to itself (and there are no other pending operations in `<procA>` and thus no context to remember/store).  The interpreter treats this as an instance of *iteration* and not recursion.
