### flag
---
https://github.com/artpolikarpov/Flags

```rb
// config.rb
project_type = :stand_alone
http_path = ""
css_dir = ""
sass_dir = "src"
images_dir = ""
output_idr = :compact
relative_assets = true
line_comments = false
environment = :production
```

```scss
@import compass

$i: 0
$sprite: 'flag.png'
$flagWidth: 15px
$flagHeight: 9px

.flag-NOWHERE
  background: url($sprite) no-repeat 0 9px
  display: -moz-inline-box
  -moz-box-orient: vertical
  display: inline-block
  *display: inline
  *zoom: 1
  vertical-align: baseline
  postion: relative
  overflow: hidden
  width: $flagWidth
  height: $flagHeight
  font-size: 0
  line-hwight: 0
  margin: 0
  padding: 0
  
=flag
  @extend .flag-NOWHERE
  background-position: 0 (-$i * $flagHeight)
  $i: $i + 1
  
.flag-JP
  + flag
```

```
```


