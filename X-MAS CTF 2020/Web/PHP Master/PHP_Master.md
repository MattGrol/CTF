![](./../../../assets/images/banner_xmas.png)



    	
            
# PHP Master



## Challenge Author(s):
`yakuhito`

## Description:
```
Another one of *those* challenges.
```

## Target:

`http://challs.xmas.htsp.ro:3000/`

## Objective:

Forge a payload capable of bypassing the various filters and checks in code, in order to have the flag printed.

## Difficulty/Points: 
`easy/33`

## Flag:
`X-MAS{s0_php_m4ny_skillz-69acb43810ed4c42}`
# 


# Challenge
Connecting to the web application, the page returned is:
```php

<?php

include('flag.php');

$p1 = $_GET['param1'];
$p2 = $_GET['param2'];

if(!isset($p1) || !isset($p2)) {
    highlight_file(__FILE__);
    die();
}

if(strpos($p1, 'e') === false && strpos($p2, 'e') === false  && strlen($p1) === strlen($p2) && $p1 !== $p2 && $p1[0] != '0' && $p1 == $p2) {
    die($flag);
}

?>

```


# Solver


