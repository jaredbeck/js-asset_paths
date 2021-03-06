# JS Asset Paths

Inspired by [js-routes](https://github.com/railsware/js-routes), JS Asset Paths makes the helper methods found in [ActionView::Helpers::AssetUrlHelper](http://rubydoc.info/docs/rails/ActionView/Helpers/AssetUrlHelper) available to the client.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'js-asset_paths'
```

Then require the js-asset_paths file in your `application.js`.

``` js
/*
= require js-asset_paths
*/
```

## Usage

A global object called `PathHelper` will be created with the following methods:

 - assetPath(source[, options])
 - fontPath(source)
 - imagePath(source)
 - javascriptPath(source)
 - stylesheetPath(source)

These functions operate in the same manner as their server-side counterparts.

## Explanation

JS Asset Paths inspects the configuration options for the current environment and determines whether or not a digest will be appended to the pathname of asset files. An object correlating the truncated asset path with the actual path to the asset on the server is stored in the generated javascript and referenced during each call.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
