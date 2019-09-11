# Quiz: Object Inheritance

???

## Object Inheritance

?: Object inheritance means that an object can adopt all of the attributes and behaviors (i.e. all of the methods) of the parent/super class. 

(X) True ( ) False

?:

```ruby
class Computer

  attr_accessor :name, :ram, :hd

  def initialize(name, ram, hd)
    @name = name
    @ram_amount = ram
    @hd_size = hd
  end

  def calculate
    "Crunching numbers!"
  end

  def save_data
    "Saving changes!"
  end

end
```

To write a subclass of `Computer` which syntax should be used?

(X)
```ruby
class Laptop < Computer

end
```
( )
```ruby
class Computer > Laptop

end
```
( )
```ruby
class Laptop

end
```
( )
```ruby
class Computer < Laptop

end
```

?: To overwrite an inherited method from `Computer`, which syntax should be used?

( )
```ruby
class Computer::Laptop
  def calculate
    "Processing mathematics!"
  end
end
```
( )
```ruby
class Laptop
  def calculate
    "Processing mathematics!"
  end
end
```
( )
```ruby
Class Laptop < Computer
  def calculate
    "Processing mathematics!"
  end
end
```
(X)
```ruby
class Laptop < Computer
  def calculate
    "Processing mathematics!"
  end
end
```

?:

```ruby
module Phrase
  def hello
    "Hello!"
  end

  def question
    "What'cha doin?"
  end

  def goodbye
    "Good bye!"
  end

  def feed_babies
    "Gonna feed the babies!"
  end
end

class Parrot
  include Phrase

  attr_accessor :name

  def initialize(name)
    @name = name
  end
end

class Human
  include Phrase

  attr_accessor :name

  def initialize(name)
    @name = name
  end
end
```

The inheritance shown in the code above is an example of what?

( ) Subclass inheritance ( ) Hierarchical inheritance (X) Mixin usage ( ) All of the Above

?:

```ruby
require_relative "../lib/parrot.rb"
require_relative "../lib/human.rb"
```

Lending a module's methods to using the `extend` keyword, is an example of what?

( ) Subclass inheritance ( ) Mixin usage (X) Class Methods ( ) Both B and C

?:

```ruby
module Talk
  module Phrases
    def hello
      "Hello!"
    end

    def question
      "What'cha doin?"
    end

    def goodbye
      "Good bye!"
    end

    def feed_babies
      "Gonna feed the babies!"
    end
  end

  module Teachers

    def teach
      "Repeat after me."
    end
  end
end
```

The code sample above is an example of nested modules.

(X) True ( ) False

?: To avoid altering a method of a parent class and creating behavior that a subclass doesn't need, we can utilize what keyword to add on additional functionality to a method in a specific subclass?

( ) `extend` (X) `super` ( ) `require` ( ) `include`

?: To supercharge inheritance, which syntax should be used?

( )
```ruby
class ImportantNotification::Notification
  def alert
    super
    @send_text_message = true
  end
end
```
(X)
```ruby
class ImportantNotification < Notification
  def alert
    super
    @send_text_message = true
  end
end
```
( )
```ruby
class ImportantNotification < Notification
  def alert.super
    @send_text_message = true
  end
end
```
( )
```ruby
Class ImportantNotification < Notification
  def alert
    super
    @send_text_message = true
  end
end
```

?: In the last example, the `#alert` method inherits any functionality of the `#alert` method defined in the parent `ImportantNotification` class and adds a feature to send a text message.

( ) True (X) False

?: The `super` keyword overwrites the functionality of the method.

( ) True (X) False

???
