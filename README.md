# Console

Ultra easy-to-use [`Symfony\Console`](https://github.com/symfony/console) to [`Nette Framework`](https://github.com/nette/).

-----

[![Build Status](https://img.shields.io/travis/contributte/console.svg?style=flat-square)](https://travis-ci.org/contributte/console)
[![Code coverage](https://img.shields.io/coveralls/contributte/console.svg?style=flat-square)](https://coveralls.io/r/contributte/console)
[![Downloads this Month](https://img.shields.io/packagist/dm/contributte/console.svg?style=flat-square)](https://packagist.org/packages/contributte/console)
[![Downloads total](https://img.shields.io/packagist/dt/contributte/console.svg?style=flat-square)](https://packagist.org/packages/contributte/console)
[![Latest stable](https://img.shields.io/packagist/v/contributte/console.svg?style=flat-square)](https://packagist.org/packages/contributte/console)
[![HHVM Status](https://img.shields.io/hhvm/contributte/console.svg?style=flat-square)](http://hhvm.h4cc.de/package/contributte/console)

## Discussion / Help

[![Join the chat](https://img.shields.io/gitter/room/contributte/contributte.svg?style=flat-square)](https://gitter.im/contributte/contributte?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Install

```
composer require contributte/console
```

## Usage

```yaml
extensions:
    console: Contributte\Console\DI\ConsoleExtensions
    
```

Extension looks for all commands extending from [`Contributte\Console\Command\AbstractCommand`](https://github.com/contributte/console/blob/master/src/Command/AbstractCommand.php). And automatically adds them to the console application. 
That's all. You don't have to be worried.

## Configuration

### URL address

There's no url in console mode (SAPI). But you can setup it by following line.

```yaml
console:
    url: www.example.com
```

## Example

```php
use Contributte\Console\Command\AbstractCommand;
use Symfony\Component\Console\Input\InputInterface;
use Symfony\Component\Console\Output\OutputInterface;

final class FooCommand extends AbstractCommand
{

	/**
	 * Configure command
	 *
	 * @return void
	 */
	protected function configure()
	{
		$this->setName('foo');
	}

	/**
	 * @param InputInterface $input
	 * @param OutputInterface $output
	 * @return void
	 */
	protected function execute(InputInterface $input, OutputInterface $output)
	{
		// Some magic..
	}

}
```

-----

Thank you for testing, reporting and contributing.
