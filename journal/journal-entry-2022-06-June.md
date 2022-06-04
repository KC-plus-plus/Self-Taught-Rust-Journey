# Journal Entry: June 2022 [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

## 01 Wednesday, June 1st
Day 0!... Or day 1, depending on how you count it I suppose. *[Insert witty joke about Computer Scientists being obsessed with counting from 0]*.

Coincidentally also the first day of Pride month, I feel like there's also some joke to be made about being queer and learning how to write Rust, but idk, so 
*[insert joke about trans fem person writing Rust for Pride month]*.

I put in a lot of effort to make this all structured and organzied and I hope I actually carry through and use it.
So cheers to the very first day of my learning Rust journal. I think it's a good idea to take stock of where I'm at and what's next.
Currently the repo looks ready for note taking and my current focus is going to be knocking out [Rustlings](https://github.com/rust-lang/rustlings) while also writing about it.
During the spring semester I got about halfway through and then got distracted from it with school being busy.
I recently took another crack at it but I think I was just blazing through and just trying to solve the problem asap while (re)learning the minimal amount just to get by, and I don't think that's a good way to approach it.
I think I will start over on that... again. As of right now I don't think I will be posting any of my code work for Rustlings to this repo, I don't see much point.

As far as improving my self-teaching, a couple articles came up while I was internet searching that I may want to look at more in the future. Here they are: [Nat Eliason Blog](https://www.nateliason.com/blog/self-education), [Lifehack Article by Dustin Wax](https://www.lifehack.org/articles/featured/becoming-self-taught.html).

Setting up this repo I think was a good acomplishment but I think if I want to keep the ball rolling I should do at least a little bit of Rustlings today as well, that way I can start off with a good momentum.

Update: I had a big brain move called "Remembering that this is a Github repo and therefore I have access to features like issues and projects" (it's a working title). So I made an [issue tracker for completing rustlings](https://github.com/KC-plus-plus/Self-Taught-Rust-Journey/issues/1).

## 02 Thursday, June 2nd
Nothing to report.

## 03 Friday, June 3rd
Okay, maybe I was a little ambitious to think that I'd make this whole repo and then actually start doing the thing in the same day, because, as it turns out, I did not start rustlings that day, nor the day after, but I did now! So time to talk about variables.

### Variables
The first rustlings section is about variables. Coming from C++ i can already see similarities. Rust is statically typed and avoids uninitialized behavior. In C++ it's more on the programmer to avoid uninitialized variables, but the Rust compiler will complain at you for not initializing which is good.
The syntax is a little weird for me because in C++, the data type *is* the keyword for declaring the variable, whereas in Rust, the keyword is `let` (or `const`) and then the type annotation comes *after* the name (and before the value).
Rust variables are also immutable by default which is an interesting change of pace, if you want it to be mutable then you add the `mut` keyword after `let`.
Interestingly, Rust allows and encourages the use of shadowing, where you can basically reuse a variable name for a different variable.
If you use `let` again on a variable then you can shadow it and assign a different value even if it's immutable, you can even give it a new type!
It's not *actually* overwriting, because if you did the overwrite in an inner scope and left that scope then it would go back to the value in the outer scope.
Also something worth noting, C++ types work on a guarenteed minumum size, but Rust you very explicitly specify the size like `i32` for example.
Integer division behaves like C++. Arrays and tuples exist but aren't covered at in the variables part of Rustlings. Arrays have a weird syntax to me but I don't have to learn that right now.

### Functions
The next rustlings section is functions and it seemed pretty easy to me with less to note than variables.
Much like variables, there's a keyword for function that isn't a data type and in rust a function is declared with `fn`.
Return types are also similar in that they come after, they're after the declaration and before the body with a `->` indicating the return type.
Parameters are typed just like how they would be for variables. The notation for the return type thing seemed weird to me, only to realize that it's similar to variables so it's not actually that hard to remember. One notable difference from C++ is that you can define the function anywheres.
It doesn't matter if there's no declaration above main and a definition below, it will still work. Oh, also important to note! It's typical to name functions in rust using snake_case which is weird to me because I'm used to lowerCamelCase (also called just camelCase), but honestly I think snake case might be better.
Similar to C++, the compiler will complain if the arguments don't match the parameter types or number of parameters.
Important thing to note is that you can *implicitly* return a value if it's the last expression evaluated.
