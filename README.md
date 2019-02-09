# WordCampGC2019
Mostly links to resources for my WordCampGC 2019 Workshop - Turbocharge your WordPress Development

# Turbocharge Your WordPress Development
Tips and tricks for improving your WordPress development skills

  ## https://12factor.net

  Everything in this guide is aimed at helping you create 12 factor web apps in WordPress.
  
  ## WordPress Development Environments
      * _old_: configure my Mac (Oh!), but there is [WordPress Valet](https://aaemnnost.tv/wp-cli-commands/valet/)…
      * _tuned up_: [XAMPP](https://www.apachefriends.org/)
      * turbocharged: [Homestead](https://laravel.com/docs/5.7/homestead) 
        or, soon, [WPLib Box](https://github.com/wplib/wplib-box) or some 
        sort of [Docker solution…](https://ghost.kontena.io/running-your-wordpress-site-in-containers/)

  ## Installing WordPress
      - old: go to wordpress.org, download, unzip, run installer etc.
      - tuned up: wp core download; wp config create --dbname=whatever --dbuser=homestead --dbpass=secret; wp db create; wp core install --url=https://something.test --title="Yo! What's up?" --admin_user=tedmasterweb --admin_password="Walk2TheLoo" --admin_email='ted@secret-source.eu' --skip-email; wp admin
      - turbocharged: composer install

  ## Debugging WordPress
      - old: echo / print_r / var_dump
      - tuned up: WP_DEBUG_LOG and trigger_error()
      - turbo charged: Debug plugin with Console

  ## Coding with style (and consistency - required for submitting plugins and themes)
      - old: copy and paste from google
      - tuned up: reading the WordPress coding standards (Yoda Conditions) https://make.wordpress.org/core/handbook/best-practices/coding-standards/php/
      - turbocharged: reading Unlce Bob's Clean Code book and Sandi Metz's OO Design in Ruby (provide examples from both)

  ## Formatting code, (automating your style)
      - old: BBEdit (sorry!), manual formatting, no syntax checking, no style conformance checking
      - tuned up: vscode with PHP extensions, some formatting, some syntax checking (but not WordPress specific)
      - turbocharged: vscode with WordPress phpcs linting (we all write code the same way)

  ## Modifying plugin behavior
      - old: copying the plugin and renaming
      - tuned up: forking the plugin (if possible)
      - turbocharged: grok the source looking for hooks, or maybe the Debug actions module, override the plugin functions / classes and then trap the exception
  - CSS
      - old: box model, float, clear - a nightmare!important
      - tuned up: bootstrap and company
      - turbocharged: SASS (Flexbox and CSS Grid)
