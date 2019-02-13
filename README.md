# WordCampGC2019
Mostly links to resources for my WordCampGC 2019 Workshop - Turbocharge your WordPress Development

# Turbocharge Your WordPress Development
Tips and tricks for improving your WordPress development skills

## https://12factor.net

Everything in this guide is aimed at helping you create 12 factor web apps in WordPress.

## Prefab WordPress Development Environments

**Important because**: time is money and we are not systems administrators (normally)

* _broken_: configure my Mac (Oh!), but there is [WordPress Valet](https://aaemnnost.tv/wp-cli-commands/valet/)…
* **tuned up**: [XAMPP](https://www.apachefriends.org/)
* **_turbocharged_**: [Homestead](https://laravel.com/docs/5.7/homestead) 
  or, soon, [WPLib Box](https://github.com/wplib/wplib-box) or some 
  sort of [Docker solution…](https://ghost.kontena.io/running-your-wordpress-site-in-containers/)

## Automated (Custom) WordPress Installation

**Important because**: time is money and we automation allows us to repeat our mistakes faster ;-)

* _broken_: go to wordpress.org, download, unzip, run installer etc.
* **tuned up**: `wp core download; wp config create --dbname=whatever --dbuser=homestead --dbpass=secret; wp db create; wp core install --url=https://something.test --title="Yo! What's up?" --admin_user=tedmasterweb --admin_password="Skip2TheLoo" --admin_email='ted@secret-source.eu' --skip-email; wp admin`
* **_turbocharged_**: `composer install` (or [roots.io](https://roots.io))

## Debugging WordPress

**Important because**: you can't fix what you can't see (or what you can't see in real time)

* _broken_: `echo` / `print_r()` / `var_dump()`
* **tuned up**: `WP_DEBUG_LOG` and `trigger_error()`
* **_turbocharged_**: [Debug Bar plugin](https://wordpress.org/plugins/debug-bar/) with [Console](https://wordpress.org/plugins/debug-bar-console/), [Cron](https://wordpress.org/plugins/debug-bar-cron/) (and a few others)

## Authoring Code

Writing any kind of non-trivial application is an exercise in composition.
In order for an application to work, be maintainable, and grow, it must
be well-planned, well-written, easy to modify, and break in obvious ways.

**Important because**: you focus on features, not on fixing bugs

* _broken_: copy and paste from google
* **tuned up**: reading [the WordPress standards](https://make.wordpress.org/core/handbook/)
* **_turbocharged_**: reading [Unlce Bob's Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882) book and Sandi Metz's OO Design in Ruby (provide examples from both)

## Formatting code, (automating your style - required for submitting plugins and themes)

**Important because**: you spend less time worrying about things that are unimportant

* _broken_: BBEdit (sorry!), manual formatting, no syntax checking, no style 
    conformance checking
* **tuned up**: vscode with PHP extensions, some formatting, some syntax 
    checking (but not WordPress specific)
* **_turbocharged_**: vscode with WordPress phpcs linting (we all write 
    code the same way) [Yoda Conditions](https://make.wordpress.org/core/handbook/best-practices/coding-standards/php/)

## Modifying Plugin Behavior

**Important because**: programming is a creative endeavor, and this is a 
typically hard challenge that often results in a much better understanding 
of programming. It's a lot like doing a code review of someone else's code.

* _broken_: copying the plugin and renaming
* **tuned up**: forking the plugin (if possible)
* **_turbocharged_**: grok the source looking for hooks, or maybe the 
    Debug actions module, override the plugin functions / classes and 
    then trap the exception

## CSS

**Important because**: You can't be an expert in everything. These tools
exist to help us create really great solutions without requiring us to
know everything!

* _broken_: box model, float, clear - a nightmare!important
* **tuned up**: bootstrap and company
* **_turbocharged_**: SASS (Flexbox and CSS Grid)

## Planning your work

**Important because**: Programming is a creative endeavor, much closer 
to story telling than math. Every program has a beginning, middle and an
end, and it needs to be a story with a happy ending. The best stories
are planned, from the beginning, and not the result of some divine 
moment of inspiration.

* _broken_: (no plan, just start programming from that amazing idea in your head)
* **tuned up**: Write a list of tasks on a piece of paper
* **_turbocharged_**: [FogBugz](https://www.fogbugz.com/). FogBugz allows 
    you to plan your program in terms of features, and features in terms 
    of tasks, and eventually, when the program is released, you can log
    bugs against features and tasks (a way to improve the story based on
    user feedback). And keep in mind that feature descriptions are only
    complete if they [include tests](https://www.smashingmagazine.com/2017/12/automated-testing-wordpress-plugins-phpunit/) (so we can verify when they are "done")
