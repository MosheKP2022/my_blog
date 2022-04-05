---
layout: post
title:  "Things I learned from Ruby Koans!"
---

Things I learned from Ruby Koans:

1. Many relevant exceptions inherit from ```StandardError```. Those include: 
- ```NoMethodError```
- ```TypeError```
- ```RuntimeError```

2. ```+=``` adds and then saves the answer. For example: 
```ruby
a=1 
a +=5
a=6
```

3. ```inject``` method can be used to sum items in array:
```ruby
[3, 6, 10].inject {|sum, number| sum + number} =>|3, 6| 3 + 6 => 9
 =>|9, 10| 9 + 10 =>19
 ```

4. ```super``` can be used to refer to parent method
``` ruby
class Dog
    def bark
    "woof"
    end
    
class BullDog < Dog
    def bark
      super + ", GROWL"
    end
  end
  def test_subclasses_can_invoke_parent_behavior_via_super
    ralph = BullDog.new("Ralph")
    assert_equal "WOOF, GROWL", ralph.bark
  end
```
