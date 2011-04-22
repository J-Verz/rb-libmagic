# Ruby FFI bindings for libmagic

## Usage

```ruby
require 'ffi-magic'
magic = Magic.new
magic.file('spec/magic.png')
# => "PNG image data, 100 x 67, 8-bit/color RGB, non-interlaced"
magic.flags = Magic::MIME
# => 1040
magic.file('spec/magic.png')
# => "image/png; charset=binary"
```

### Getting the MIME Type

```ruby
magic = Magic.new(Magic::MIME)
magic.file('spec/magic.png')
# => "image/png"
```
