## オブジェクト生成数比較

* [ko1/allocation\_tracer](https://github.com/ko1/allocation_tracer)を使用してobjectの生成数を見てみる

```ruby
ObjectSpace::AllocationTracer.trace { SequelPost.all.each{} }
p allocated: ObjectSpace::AllocationTracer.allocated_count_table

ObjectSpace::AllocationTracer.trace { ArPost.all.each{} }
p allocated: ObjectSpace::AllocationTracer.allocated_count_table
```

