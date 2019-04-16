# Simple Blog Theme

Simple Wallaby blog theme based on Bootstrap4.

## Usage

To use this theme, it goes:

```ruby
class BlogsController < Wallaby::ResourcesController
  self.theme_name = 'simple_blog_theme'
end
```

If the fields aren't detected correctly, you can config them in resource decorator:

```ruby
class BlogDecorator < Wallaby::ResourceDecorator
  # NOTE: author field should contain only string value
  index_field[:author_field][:is_author] = true

  # NOTE: title field should contain only string/text value
  index_field[:title_field][:is_title] = true

  # NOTE: summary field should contain only string/text value
  index_field[:summary_field][:is_summary] = true

  # NOTE: published_at field should contain only date/time value
  index_field[:published_at_field][:is_published_at] = true

  # NOTE: image field should contain only active_storage value
  index_field[:image_field][:is_image] = true

  # NOTE: body field should contain only string/text value
  index_field[:body_field][:is_body] = true
end
```

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'simple_blog_theme'
```

And then execute:

```bash
$ bundle
```

## Contributing

Contribution directions go here.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
