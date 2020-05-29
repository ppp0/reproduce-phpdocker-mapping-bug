reproduce-phpdocker-mapping-bug
==


Run test
-----------

You need Idea plugin **PHP Docker** (https://plugins.jetbrains.com/plugin/8595-php-docker). Plugin **Python** needs to be disabled!

Select file `bin/test.php` and run it with the remote interpreter inside docker-compose (Service: phpide)

Reproduce bug
--

Now, activate plugin **Python** and try the same

In the run panel, you will see:
`[docker-compose://[<HOME>/IdeaProjects/reproduce-phpdocker-mapping-bug/docker-compose.yml]:phpide/]:php /opt/project/bin/test.php
 `
 
 That is, ` /opt/project/bin/test.php` instead of `/opt/reproduce-phpdocker-mapping-bug/bin/test.php`
 
