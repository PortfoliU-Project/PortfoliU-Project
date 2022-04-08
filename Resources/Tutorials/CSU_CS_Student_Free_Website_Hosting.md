# Colorado State University CS Students

## *How to Host Your Own Personal Website*


### 1. Connect to a CS Department machine via SSH or through physical login
To connect to a department machine, first select a machine in this list:

    https://www.cs.colostate.edu/~info/machines

Then type the following commmand in your terminal, MobaXterm, Putty, etc...

    ssh yourCSUeid@machineName.cs.colostate.edu
    
### 2. Create a public_html subdirectory in your home folder with permissions of 711

      cd
      mkdir public_html
      chmod 711 ./public_html
      
Now anything placed under this directory will be accessible from the web using the ~ operator. For example:

      http://www.cs.colostate.edu/~USERNAME/file
      
Would map to 

      ~/public_html/file
      
### 3. If you are running into "Access Forbidden" errors, you probably have a permissions problem.

In general, permissions should be:

      644 for regular files (HTML, CSS, images, etc)
      600 for PHP files
      711 for directories
      
*Note that PHP scripts do not need to be world-readable and are run using the permissions of their owner. This prevents other CS users from being able to see your PHP code.*

### 4. index.html (your website code)
In order to determine the default page to be displayed when accessing a directory from the web, CSU's web server looks for files named:

      index.html
      index.php
      etc...
      
If you have an index.html in your ~/public_html/ directory, it will be displayed when visiting http://www.cs.colostate.edu/~yourCSUeid

### Setting all of the file permissions can be time consuiming depending on how many files your website will contain but the end result will be plenty worth the work.
