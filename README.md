# sass-mq-generator
A sass mixin that uses a bundle of maps and functions to create fairly specific media queries

Allows you to combine both horizontal and vertical media queries in one declaration if you like. For example, something like:

```
.foo {
   @include view(xnarrow only, middle) {
      height: 100px;
   }
}
```

outputs

```
@media screen and (min-width: 0em) and (max-width: 39.99em) and (min-height: 35.5em) {
   .foo {
      height: 100px;
   }
}
```

or:

```
.foo {
   @include view(medium) {
      height: 100px;
   }
}
```

outputs

```
@media screen and (min-width: 50em) {
   .foo {
      height: 100px;
   }
}
```

Natural language instead of comma separators would be nice, but sass likes to choke on the keyword `and`. I might experiment with an ampersand though (e.g. `short & wide only`)
