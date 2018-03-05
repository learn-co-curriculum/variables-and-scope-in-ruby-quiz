# Quiz: Variables and Scope in Ruby

## Introduction

Welcome to our quiz! Quizzes are designed for knowledge exploration and finding
weaknesses in your understanding. Use this to check up on your understanding.
Even if you see the "right" answer, consider what it would take to change the
given code to make it work. Think through the bugs that may arise in the given
code and consider multiple ways to fix the errors. Doing so will improve your
learning as there is always more than one solution and that solution may not be
immediately obvious. Incidentally, those are common tasks to assign in an
interview: explaining buggy code and then debugging it. Accordingly, these are
skills that we hope to help you grow over your course of study at Flatiron!

???

# Variables and Scope in Ruby Quiz

## Consider the following code:

```ruby
$best_dog_ever = "Byron the Moyen Poodle"

class OpinionatedClass
  def initialize(dog="Byron the Kleinpudel")
    @dog = dog
  end

  def opinionate!
    puts("#{$best_dog_ever} is the best dog ever")
  end
end

oc = OpinionatedClass.new()
oc.opinionate!
```

?: What does the `$` in front of `$best_dog_ever` signify?

( ) A protected variable
( ) A static variable
( ) A local variable
(X) A global variable

?: What does `.new()` return (and assign to `oc`)?

( ) A static copy of the `OpinionatedClass` class
( ) A reference to the `OpinionatedClass` constructor
(X) An instance of `OpinionatedClass`
( ) An instance of `OpinionatedClass` with no instance variables initialized

?: Predict what `oc.opinionate!` returns

( ) Trick question, it doesn't emit anything
(X) "Byron the Moyen Poodle is the best dog ever"
( ) "undefined is the best dog ever"
( ) " is the best dog ever"

?: Your colleague is asking for some help debugging their code. When they
   invoke:

   ```ruby
   oc2 = OpinionatedClass.new()
   oc2.opinionate!
   ```

   they were expecting "Byron the Kleinpudel" to appear somewhere. It doesn't.
   Without running the code, what do you expect to see? Help your colleague
   understand what's going on.

(X) In `opinionate!` the method returns a global versus an instance variable
( ) In `opinionate!` the method returns a instance versus an global variable
( ) `@dog` is in the global namespace and needs to be in the class namespace


5. Another colleague is asking for some help tweaking this code. When they
   invoke:
   ```ruby
   oc3 = OpinionatedClass.new("Novak the Goldendoodle")
   oc3.opinionate!
   ```

   they want to see `Novak the Goldendoodle is the best dog ever`. How should they
   adjust the provided starter code to support this usage?

( ) `puts(@dog.to_s + " is the best dog ever")`
(X) `puts("#{@dog} is the best dog ever")`
( ) `puts(String(@dog) + " is the best dog ever")`

6. Will this code work?

   ```ruby
   oc = OpinionatedClass.new()
   oc.dog = "Zebulon T. Bark"
   ```

( ) Works
(X) Nope, doesn't work

???
