# Sass

##Loop

```sass
$plan-card: (one: #00ff00, two: #ff0000);

@each $num, $color in $plan-card {
  plan-#{$num} {
    color: $color;
    min-width: 100%;
    content: "#{$num}";
  }
}
```
