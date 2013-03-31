PHPMath
=======

PHPMath is a library to run [Mathematica][1] functions troght [PHP][2].

Instructions
============

- Mathematica License:
    - Copy your Mathematica® license to the PHP home folder (for example, 
        `/var/www`).
        - The license usually is on a hidden folder inside the licensed user
            home (for example, `/home/user/.Mathematica`).
        - In other words, for this example, the folder `.Mathematica` inside 
            `/home/user` should be copied to `/var/www`.
- Composer:
    - Put `"garoudan/phpmath": "dev-master"` in your `composer.json` require section.
    - Example of a full `composer.json` file:

    {
        "require": {
            "garoudan/phpmath": "dev-master"
        },
        "autoload" : {
            "psr-0" : {"Backend" : "core"}
        }
    }

- Start coding:

    $phpmath = new PHPMath\PHPMath();
    echo $phpmath->run("Prime[1000]");

Enjoy.

[1]: http://www.wolfram.com/mathematica/
[2]: http://php.net/