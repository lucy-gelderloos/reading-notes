# Class 08 - Efficient Development

## [Don't Repeat Yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)

"Don't Repeat Yourself" (DRY) is a programming approach that emphasizes using abstraction and [data normalization](https://en.wikipedia.org/wiki/Database_normalization) (a way of approaching databases to ensure data consistency and predictable behavior). When followed, this approach means that elements in a system can be modified without affecting other elements. Non-DRY development is sometimes called WET.

AHA development takes a slightly different approach, noting that abstracting for the sake of abstracting can sometimes take more time than it saves and can lead to software that is rigid and difficult to update. AHA development says a certain amount of duplication is fine as long as that's the most efficient approach.

## [The Rule of Three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming))

Essentially, if you're repeating code in two different places, it's probably fine, but once you've repeated it a three or more times, you should consider refactoring it into its own method/procedure/etc.

## [You Aren't Gonna Need It](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)

When developing software, it's easy to come up with lots of "cool to have" features/functionality. Focus on what you actually need, and put the cool ideas in a readme or scratch file or something. You don't want unnecessary features getting in the way of debugging your main features, and the architecture may change along the way in a way that makes those features irrelevant.

## [Minimum Viable Product](https://en.wikipedia.org/wiki/Minimum_viable_product)

A minimum viable product (MVP) focuses on getting core features in place for customers (or a subset of customers) to test. Rather than releasting a huge finished product with tons of features, developers release an MVP and integrate feedback into future development.

This process also helps determine whether there is actually a market for the product before a company invests a bunch of time and money developing it.

Potential drawbacks are that releasing an unsatisfying product could hurt a company's reputation (especially given that customers can increasingly easily switch to another product) and that competitors could potentially copy the product at an early stage.

## Things I want to know more about

I think I understand abstraction in the abstract (get it??) but I'm still having trouble articulating it and understanding how I use it in my code.
