# Autoframe is a low level framework that is oriented on SOLID flexibility

[![License: The 3-Clause BSD License](https://img.shields.io/github/license/autoframe/cli-tools)](https://opensource.org/license/bsd-3-clause/)
![Packagist Version](https://img.shields.io/packagist/v/autoframe/cli-tools?label=packagist%20stable)
[![Downloads](https://img.shields.io/packagist/dm/autoframe/cli-tools.svg)](https://packagist.org/packages/autoframe/components-socket-cache)

*Cli Prompt, Text styles Bold, Italic, Blink, Underline, Text colors, Background colors...*

**Examples** https://prnt.sc/-ns-4QpB3NYl

![Examples](https://img001.prntscr.com/file/img001/j6aDkLc5SkG0jMaKxPMSmw.png) 

```php
`AfrCliPromptMenu`

use Autoframe\CliTools\AfrCliPromptMenu;

        if (!AfrCliPromptMenu::insideCli()) {
            echo 'The script does not run inside CLI!' . PHP_EOL;
            return;
        }

        $options = [
            'Mercedes',
            'Audi',
            'Porsche',
        ];

        $user_choice = AfrCliPromptMenu::promptMenu(
            "Select your dream car",
            $options,
            $options[1]
        );
        print PHP_EOL . "You chose: '$user_choice'\n";
```

---

```php
`AfrCliTextColors`

use Autoframe\CliTools\AfrCliTextColors;

AfrCliTextColors::getInstance()->
        bgBlueLight('Hello ')->
        bgDefaultAllColorStyle( 'my ')->
        styleBold(true)->
        textAppend('bold ')->
        colorGreen('World! ')->
        styleBold(false)->
        bgMagenta('How ')->
        styleInvert(true)->
        textAppend('Inverted ')->
        styleInvert(false)->
        bgCyanLight()->
        colorYellowLight('is the ')->
        styleItalic(true)->
        colorRed('rainbow?')->
        styleDefaultAllBgColor()->
        textPrint();
```
