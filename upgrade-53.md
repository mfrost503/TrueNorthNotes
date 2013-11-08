# Didn't I just upgrade to 5.3
# Sara Golemon @SaraMG

## Not "What", "Why" & "How"
* PHP was never designed
* Thrown at the wall, see if it sticks

### PHP 1
* Rasmus wanted to update his resume more easily
* Make websites "prettier"

### PHP 2
* Built for a larger audience
* Personal Home Page
* Based on low interpretive engine
* Unrecognizable as a modern PHP

### PHP 3 - PAAMAYIM_NEKUDOTAYIM
* Modern PHP syntax
* Installed on 10% of webservers world wide
* Actual compiler
* Resources and initial object support
* Bundled Extensions/More DB Support
* php3.com - original website

### PHP 4 - The Zend Engine
* Refactor architecture
* 3rd party extensions
* Multiple SAPIs
* Streams Layer
* PEAR/PECL
* Explosion of standard function
* Rapid iteration

### PHP 5
* Zend Engine 2
* Objections aren't just arrays with functions
* Performance, security, stability focused
* PDO

### PHP 6
* Native support for Unicode Strings
* Transparent encoding conversions
* Locale aware
* Streams Database integration
* l18n/ l10n is in the future
* Everyone stopped working on it...

### PHP 7
* 6 is forever dead
* PHP 7 will be name when there is a significant change
	* Everything in a namespace? Fix inconsistencies?
	* HHVM?

## Why do I need to keep chasing PHP Versions?
* 5.4 was ~25-30% increase from 5.3
* PHP is getting more stable
	* 1 year between minor releases
	* Fewer things to screw up between upgrades
* Minor versions must be backwards compatible
* PHP has goto because there wasn't an RFC process

## How is PHP getting faster?
* compiled variables
* 3 fetches per iteration before for 5.1
* 5.1 moves to 0 fetches per iteration
* 5.4 opline sizes are shrunk
* 63% reduction
* 76 bytes in 5.3 (or 152 bytes on 64-bit system)
* 28 bytes in 5.4 (or 56 bytes on 64-bit system)
* 5.5 Class compiled variables
* Same process on local variables applied to properties
* Not as significant a performance boost as 5.4
* Dynamic properties cannot take advantage of this
* Password hashing API
* Security is easy to get wrong
* http://bit.ly/1ilmU5B - Adobe password debacle
* password_hash/password_verify
	* Versioned hashes
	* Per-password salt
* Generators use the yield keyword
* Yield "saves your spot"

## Getting Involved
* PHP has no leader
* Run by people who care about the language
* PEAR/PECL
	* Centralized home of 3rd party apps, components and extensions
	* Release on your own schedule
	* Get other people involved
* PHP Documentation is the best documentation ever, you can contribute
* Thank-less, but important work
	* free @php.net email address!
	* Phenomenal cosmic power (to moderate comments)
	* Must use SVN 
* php-internals is a different story
* Help shape future
* Suggest/Comment/Vote on RFCs
* Bring Kevlar
* blog.golemon.com
* http://github.com/php/php-src
