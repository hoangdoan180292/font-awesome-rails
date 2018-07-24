# font-awesome-rails

## Installation

Add this to your Gemfile:

```ruby
gem 'font-awesome-rails', git: 'https://github.com/hoangdoan180292/font-awesome-rails.git'
```

and run `bundle install`.

## Usage

In your `application.css`, include the css file:

```css
/*
 *= require font-awesome
 */
```
Then restart your webserver if it was previously running.

Congrats! You now have scalable vector icon support. Pick an icon and check out the
[FontAwesome Examples](http://fortawesome.github.io/Font-Awesome/examples/).

### Sass Support

If you prefer [SCSS](http://sass-lang.com/documentation/file.SASS_REFERENCE.html), add this to your
`application.css.scss` file:

```scss
@import "font-awesome";
```

If you use the
[Sass indented syntax](http://sass-lang.com/docs/yardoc/file.INDENTED_SYNTAX.html),
add this to your `application.css.sass` file:

```sass
@import font-awesome
```

### Helpers

There are also some helpers (`fa_icon` and `fa_stacked_icon`) that make your
views _icontastic!_

```ruby
icon('fas', 'sign-out-alt', text: 'Logout')
# => <i class="fas fa-sign-out-alt left"></i>Logout

icon('far', 'copy', text: 'review', icon_position: :right)
# => Review<i class="far fa-copy right"></i>
```

```ruby
fa_icon "camera-retro"
# => <i class="fa fa-camera-retro"></i>

fa_icon "camera-retro", text: "Take a photo"
# => <i class="fa fa-camera-retro"></i> Take a photo

fa_icon "chevron-right", text: "Get started", right: true
# => Get started <i class="fa fa-chevron-right"></i>

fa_icon "quote-left 4x", class: "text-muted pull-left"
# => <i class="fa fa-quote-left fa-4x text-muted pull-left"></i>

content_tag(:li, fa_icon("check li", text: "Bulleted list item"))
# => <li><i class="fa fa-check fa-li"></i> Bulleted list item</li>
```

```ruby
fa_stacked_icon "twitter", base: "square-o"
# => <span class="fa-stack">
# =>   <i class="fa fa-square-o fa-stack-2x"></i>
# =>   <i class="fa fa-twitter fa-stack-1x"></i>
# => </span>

fa_stacked_icon "dollar inverse", base: "circle", class: "fa-5x"
# => <span class="fa-stack fa-5x">
# =>   <i class="fa fa-circle fa-stack-2x"></i>
# =>   <i class="fa fa-dollar fa-inverse fa-stack-1x"></i>
# => </span>

fa_stacked_icon "terminal inverse", base: "square", class: "pull-right", text: "Hi!"
# => <span class="fa-stack pull-right">
# =>   <i class="fa fa-square fa-stack-2x"></i>
# =>   <i class="fa fa-terminal fa-inverse fa-stack-1x"></i>
# => </span> Hi!

```