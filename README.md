# Sass-Cheatsheet


Syntacticall awesome stylesheet cheatsheet

Calling a mixin:

```
@mixin gradiantbackground() {
  background: $orange;
  background: -moz-linear-gradient(-45deg,  $orange 0%, $light-orange 100%);
  background: -webkit-linear-gradient(-45deg,  $orange 0%,$light-orange 100%);
  background: linear-gradient(135deg,  $orange 0%,$light-orange 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='$orange', endColorstr='$light-orange',GradientType=1 );
}

section {
	@include gradiantbackground();
}

```
Passing values to a mixin:

```
@mixin anchor-color($color:$white,$hover:$orange) {
  a { color: $color;
    &:hover { color: $hover;}
  }
}

@include anchor-color($orange, scale-color($orange, $lightness: -14%));
or 
@include anchor-color($detail,$dark-gray);
``