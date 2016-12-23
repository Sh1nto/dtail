# dtail
Enhanced tail with auto inserting blank lines and highlighting PHP-Errors

#Installation
To install copy dtail e.g. to /usr/bin/dtail. Make dtail executable with 

`chmod ugo+x /usr/bin/dtail`

Check that the LOG_FORMAT defined in dtail matches your error apache error log format

``` PHP
//[Sun Nov 27 08:31:09.138751 2016] [:error] [pid 30039] [client 192.168.xx.xx:50691] script '/var/www/html/genlog.php' not found or unable to stat
define('LOG_FORMAT', '/^(?<date>\[[^\]]+\]) (?<type>\[[^\]]+\]) (?<pid>\[[^\]]+\]) (?<client>\[[^\]]+\]) (?<msg>.*)$/');
```

Customize LOG_FORMAT to your needs

#Usage
`dtail v1.0 - Developer Tail
Usage: dtail <filename>
   or: tail -F /var/log/apache2/error.log | dtail

Parms:
   -p<path>    Path to remove from filenames, otherwise current dir
`