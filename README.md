# PunditCustomErrors

`pundit_custom_errors` is an extension for the Pundit gem that enables the creation of custom error messages. This adds more flexibility to retrieve different kinds of messages in the same validation method, according to the nature of the error. As for the default error message, it is also set up to generate them by using a localization file (if existent).

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'pundit_custom_errors'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install pundit_custom_errors

## Usage

### How to generate a custom error message

- extend PunditCustomErrors::Policy in your Policy class
- inside the validation method, populate the Policy's `error_message` attribute with the desired error message

### Extracting default error messages to YAML

#### Creating the YAML file 

By running the command:

```ruby
rails generate pundit_custom_errors:initialize 
```

A file called `pundit_custom_errors.en.yml` will be generated inside the `config/locales` folder. It contains the default message, used if there's no messages for the given controller/action validation.

#### Creating error messages in the localization file



## Contributing

1. Fork it ( https://github.com/[my-github-username]/pundit_custom_errors/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
