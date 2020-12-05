# Expressions rationnelles

> AIDE - Expressions rationnelles (à venir)

## Délimiteurs

À venir...

## Méta-caractères

À venir...

## Classes de caractères

À venir...

## Options de recherche

À venir...

---

## Exemples de code

### C

> _**NOTE** : issu de la norme POSIX (n'est pas portable)_

```c
#include <stdio.h>
#include <stdlib.h>
#include <regex.h>

int main(void)
{
    char data[] = "tester-une-expression-rationnelle-avec-C";
    char pattern[] = "^[a-zA-Z-]+$";
    char buffer[128];
    regex_t regex;
    int exec_regex_code;
    
    if(regcomp(&regex, pattern, REG_EXTENDED))
    {
        fprintf(stderr, "ERREUR : Impossible de compiler le motif\n");
        exit(EXIT_FAILURE);
    }
    
    exec_regex_code = regexec(&regex, data, 0, NULL, 0);
        
    if(!exec_regex_code)
        printf("OK\n");
    else if(exec_regex_code == REG_NOMATCH)
        printf("PAS OK\n");
    else
    {
        regerror(exec_regex_code, &regex, buffer, sizeof(buffer));
        fprintf(stderr, "ERREUR : Echec du test de motif (%s)", buffer);
        exit(EXIT_FAILURE);
    }
    
    regfree(&regex);
    return 0;
}
```

### C++

```cpp
#include <iostream>
#include <regex>
#include <string>

int main()
{
	std::string data = "tester-une-expression-rationnelle-avec-CPP";
	std::string pattern = "^[a-zA-Z-]+$";

	if(std::regex_match(data, std::regex(pattern)))
		std::cout << "OK" << std::endl;

	return 0;
}
```

### Java

```java
import java.util.regex.Matcher;

public class Main
{
	public static void main(String[] args)
	{
		String data = "tester-une-expression-rationnelle-avec-Java";
		String pattern = "^[a-zA-Z-]+$";

		if(data.matches(pattern))
			System.out.println("OK");
	}
}
```

### JavaScript

```javascript
let data = "tester-une-expression-rationnelle-avec-JavaScript";
let pattern = "^[a-zA-Z-]+$";

if(data.match(pattern))
	document.write("OK");
```

### PHP

```php
<?php

$data = 'tester-une-expression-rationnelle-avec-PHP';
$pattern = '#^[a-zA-Z\-]+$#';

if(preg_match($pattern, $data))
	echo 'OK';
```

### Python

```python
#coding:utf-8
import re

data = 'tester-une-expression-rationnelle-avec-Python'
pattern = '^[a-zA-Z-]+$'

if re.search(pattern, data):
	print('OK')
```

### SQL

```sql
SELECT REGEXP_INSTR('tester-une-expression-rationnelle-avec-SQL', '^[a-zA-Z-]+$');
```