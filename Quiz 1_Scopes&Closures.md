function foo(a) {
    var b = a;
    return a + b;
}

var c = foo( 2 );


*Engine*: Hey, *Scope*, I have a (#1)RHS reference for `foo`. Ever heard of it?


*Scope*: Sure, *Engine* it is a function, *Compiler* just told me about it. Here you go, have `foo`.


*Engine*: Thanks, *Scope*, I'm going to execute `foo`.


*Engine*: Hey, *Scope*, I have a (#1)left hand side look up for something called `a`. Ever heard of it?


*Scope*: Actually, yes, *Compiler* just told me about it, `a` is a parameter of `foo`.


*Engine*: Always helpful, *Scope* thanks for letting me know what is up. I'm going to assign `a` to `foo`.


*Engine*: Hey ho, *Scope* I just found a (#2)LHS lookup I need to know about called `b`, do you know about it?


*Scope*: In fact, *Engine* I do! *Compiler* just told me that `b` is a variable.


*Engine*: Great to know, *Scope* thanks. Say, while we're talking do you know what value is assigned to `b`?


*Scope*: Funny you should ask, *Engine*. *Compiler* Just stopped by to tell me that the `a` parameter of `foo` is the (#3)LHS value of `b`.

*Engine*: Hey *Scope*, do you know what (#2) RHS `return` does? 

*Scope*: Sure! It's built in. Here you go!

*Engine*: And (#4)LHS `+`? What's that *Scope*?

*Scope*: It's built in too!

*Engine*: *Scope*, I have an (#3)RHS reference for `c`. Know what that is?

*Scope*: Sure do, *Engine*, `c` is a container for the function `foo` we talked about earlier.

*Engine*: OH! Good to know, now you reminded me that `foo` is a function, but what is its (#4)RHS lookup for its parameter?

*Scope*: Easy! *Compiler* just dropped it off, the (#4)RHS for `foo` is `2`!

*Engine* Ah super. Would you please tell *Compiler* that the return value is `4`? Thanks!


###GOT QUIZ WRONG###
***Correct answers***

_Quiz Answers_

function foo(a) {
    var b = a;
    return a + b;
}

var c = foo( 2 ); 

***Identify all the LHS look-ups (there are 3!).***
 
c = ..;, a = 2 (implicit param assignment) and b = .. 

***Identify all the RHS look-ups (there are 4!).***
 
foo(2.., = a;, a .. and .. b

