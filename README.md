# InstanceStorage for mruby

[instance_storage](https://github.com/toshia/instance_storage) gemをmrubyにポーティングしたものです。

## Original Description

クラスにincludeすると、クラスインスタンスごとにSymbolを割り振って、あとからその名前でインスタンスにアクセスする機能を提供します。

## Installation

Add conf.gem line to your `build_config.rb`:

```ruby
MRuby::Build.new do |conf|

    # ... (snip) ...

    conf.gem :github => 'shibafu528/mruby-instance-storage'
end
```

## Usage

```ruby
class Tag
  include InstanceStorage
end

foo = Tag[:foo]  # generate instance `foo'
foo.name         # => :foo
foo == Tag[:foo] # => true
foo == Tag[:bar] # => false
```

## Contributing

1. Fork it ( https://github.com/shibafu528/mruby-instance-storage/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
