# RailsCasts Episode #238: Mongoid (revised)

http://railscasts.com/episodes/238-mongoid-revised

Requires Ruby 1.9.2 or higher.


### Commands used in this episode

```
rails g mongoid:config
rails g scaffold product name price:big_decimal
rails g model review content
```


### Commands used in rails console

```ruby
Product.where(:price.lte => 40).first
Product.lte(price: 40).first
Product.lte(price: 40).gt(released_at: 1.month.ago)
Product.lte(price: 40).gt(released_at: 1.month.ago).asc(:name)

p = Product.first
p.reviews.create! content: "great game!"
p.reviews.size
Review.count

p = Product.first
p.destroy
Product.count
p.restore
```
