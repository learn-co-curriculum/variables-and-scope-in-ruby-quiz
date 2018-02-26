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

## Quiz

Consider the following code:

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

1. What does the `$` in front of `$best_dog_ever` signify?

2. What does `.new()` return (and assign to `oc`)?

3. Predict what `oc.opinionate!` returns

4. Your colleague is asking for some help debugging their code. When they
   invoke:
   ```ruby
   oc2 = OpinionatedClass.new()
   oc2.opinionate!
   ```

   they were expecting "Byron the Kleinpudel" to appear somewhere. It doesn't.
   Without running the code, what do you expect to see? How could you make this
   code work as your colleague is imagining?

5. Another colleague is asking for some help tweaking this code. When they
   invoke:
   ```ruby
   oc3 = OpinionatedClass.new("Novak the Goldendoodle")
   oc3.opinionate!
   ```

   they want to see `Novak the Goldendoodle is the best dog ever`. How should they
   adjust this code to support this usage.

6. What will happen with this code?
   ```ruby
   oc = OpinionatedClass.new()
   oc.dog = "Zebulon T. Bark"
   ```

   If the code will produce an error, suggest a bugfix.
