# sass-mq-generator
A sass mixin that uses a bundle of maps and functions to create fairly specific media queries

Allows you to combine both horizontal and vertical media queries in one declaration if you like

```
@include view(xnarrow only, middle) {
   height: 100px;
}
```

outputs

```
@media screen and (min-width: 0em) and (max-width: 39.99em) and (min-height: 35.5em) {
}
```
