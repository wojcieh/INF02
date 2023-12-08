    1  sudo apt update
    2  sudo apt upgrade
    3  ip a
    4  pwd
    5  ip a
    6  top
    7  python3
    8  sudo apt install snap
    9  sudo snap install onionshare
   10  echo Choo Choo
   11  pwd
   12  code .
   13  sudo apt update
   14  sudo apt upgrade
   15  /bin/python3 /home/marcin/skrypty/liczby2,py
   16  ls
   17  mkdir skrypty
   18  cd skrypty/
   19  code .
   20  pwd
   21  echo ~
   22  ls
   23  mkdir 2TA
   24  cd 2TA/
   25  ls
   26  echo "Cześć Marcin"
   27  $imie = "Marcin"
   28  $imie == "Marcin"
   29  var $imie == "Marcin"
   30  ls
   31  echo {1..10}
   32  touch plik{1..10}.{txt, jpg, mp3, html, js, py}
   33  ls
   34  touch plik{1..10}.{txt jpg mp3 html js py}
   35  ls
   36  ls -l
   37  rm  *
   38  ls
   39  touch plik{1..10}
   40  ls
   41  rm *
   42  touch plik{1..10}.txt
   43  ls
   44  touch plik{1..10}.jpeg
   45  touch plik{1..10}.p
   46  touch plik{1..10}.py
   47  ls
   48  touch zdjecie{1..10}.jpg
   49  ls
   50  ls -l
   51  ls *
   52  ls *.txt
   53  ls *.jpg
   54  ls -l *.jpg
   55  ls -l *.p
   56  ls -l *.p*
   57  rm *.p
   58  ls -l *.p*
   59  echo *
   60  ls -l *.??
   61  ls -l *1.??
   62  ls -l
   63  ls
   64  ls -l ?????.*
   65  ls -l *.????
   66  ls -l [pz]*
   67  ls -l *[89.]*
   68  ls -l *[89].*
   69  touch zdjecie{2022..2023}{1..12}.jpg
   70  ls
   71  ls -l *2022*
   72  ls -l [!z]*
   73  ls -l [!p]*
   74  ||
   75  echo {1..10}
   76  echo {1..10}>>liczby.txt
   77  cat liczby.txt
   78  cp liczby.txt liczby1.txt
   79  cat liczby.txt 
   80  cat liczby1.txt 
   81  echo {a..z}>>liczby.txt
   82  ls
   83  touch liczby.txt 
   84  cat liczby.txt 
   85  diff liczby.txt liczby1.txt
   86  diff liczby1.txt liczby.txt
   87  cp liczby1.txt liczby2.txt
   88  diff liczby1.txt liczby2.txt
   89  cd ..
   90  echo .
   91  find .
   92  find . -name "*.txt"
   93  find . type f -name "zd*"
   94  find . -type f -name "zd*"
   95  find . -type d -name "zd*"
   96  find . -type d -name "z*"
   97  find . -name "z*" -size +100k -1m
   98  man find
   99  find . -name "z*" -size +100k -1M
  100  find . -name "z*" -size +100k size -1M
  101  find . -name "z*" -size +100k -size -1M
  102  find . -size +100k -size -1M
  103  find ./2TA/ -size -100k 
  104  find ./2TA/ -size -100k -name "*.txt"
  105  find ./2TA/ -size -100k -name "*.txt" -exec ls {};
  106  find ./2TA/ -size -100k -name "*.txt" -exec ls{};
  107  find ./2TA/ -size -100k -name "*.txt" -exec ls -l {};
  108  find ./2TA/ -size -100k -name "*.txt" -exec ls -l {}
  109  find ./2TA/ -size -100k -name "*.txt" -exec ls -l {}\;
  110  find ./2TA/ -size -100k -name "*.txt" -exec ls -l {} \;
  111  find ./2TA/ -size -100k -name "*.txt" -exec echo "test">> {} \;
  112  find ./2TA/ -size -100k -name "*.txt" -exec cat {} \;
  113  find ./2TA/ -size -100k -name "*.txt" -exec echo "test" >> {} \;
  114  find ./2TA/ -size -100k -name "*.txt" -exec cat {} \;
  115  tmux
  116  top
  117  htop
  118  btop
  119  sudo snap install btop
  120  sudo btop
  121  /bin/python3 /home/marcin/skrypty/lokata.py
  122  curl https://static-labs.tryhackme.cloud/sites/favicon/images/favicon.ico | md5sum
  123  exit
  124  sudo apt-get update
  125  sudo apt-get upgrade
  126  sudo apt-get install apache2
  127  ip a
  128  sudo apt install mysql-server
  129  cd /etc/
  130  ls sudo apt-get instal phpmyadmin
  131  sudo apt-get instal phpmyadmin
  132  sudo apt-get install phpmyadmin
  133  sudo apt install php libapache2-mod-php php-mysql
  134  ls
  135  cd phpmyadmin/
  136  ls
  137  code apache.conf 
  138  nano config-db.php 
  139  sudo nano config.inc.php 
  140  exit
  141  mysql -l root
  142  mysqli
  143  sudo mysql -u root
  144  sudo mysql -u root -p
  145  sudo sytemctl reaload apache2
  146  sudo service apache2 reload
  147  sudo service apache2 status
  148  sudo sytemctl reaload msql
  149  sudo service mysql reboot
  150  sudo service mysql restart
  151  sudo service mysql status
  152  sudo service apache2 status
  153  nano /etc/phpmyadmin/config.inc.php 
  154  sudo service apache2 status
  155  nano /etc/phpmyadmin/config.inc.php 
  156  sudo mysql -u root -p
  157  sudo mysqli -u marcin
  158  sudo mysql -u marcin
  159  sudo mysql -u marcin -p
  160  ls /etc/mysql/
  161  sudo nano /etc/mysql/mysql.cnf 
  162  ls /etc/mysql/mysql.conf.d/
  163  ls /etc/mysql/mysql.conf.d/mysql.cnf 
  164  nano /etc/mysql/mysql.conf.d/mysql.cnf 
  165  nano /etc/mysql/mysql.conf.d/mysqld.cnf 
  166  exit
  167  sudo service apache2 status
  168  ip a
  169  sudo mysqli -u root -p
  170  sudo mysql -u root -p
  171  sudo service mysql restart
  172  sudo service mysql status
  173  sudo service apache2 status
  174  sudo mysql -u root -p
  175  cd /var/www/html/
  176  ls
  177  mkdir z4
  178  sudo mkdir z4
  179  cd z4/
  180  sudo code .
  181  code .
  182  ls
  183  cd ..
  184  ls
  185  ls -l
  186  sudo chown marcin:marcin z4
  187  ls
  188  ls -l
  189  cd z4/
  190  code .
  191  cd /var/www/html
  192  ls
  193  mkdir 5ta
  194  sudo mkdir 5ta
  195  ls
  196  sudo chmod marcin:marcin 5ta/
  197  sudo chmod marcin:marcin 5ta
  198  sudo chown marcin:marcin 5ta/
  199  ls -l
  200  ls
  201  cd 5ta
  202  ls
  203  cd z1/
  204  ls
  205  diff -qr PuchtaDawid/ StrzebonskiPatryk/
  206  ls PuchtaDawid/
  207  diff PuchtaDawid/index.php StrzebonskiPatryk/index.php 
  208  diff -ql PuchtaDawid/index.php StrzebonskiPatryk/index.php 
  209  code .
  210  ls
  211  pwd
  212  ln www /var/www/html/
  213  man ln
  214  ln /var/www/html/ www
  215  man ln
  216  ln -L /var/www/html/ www
  217  man ln
  218  ln -s /var/www/html/ www
  219  cd www
  220  ls
  221  cd 5ta/
  222  ls
  223  cd z1/
  224  ls
  225  cd ..
  226  mkdir proba1
  227  ls
  228  ls -l
  229  ls
  230  cd 2TA/
  231  ls
  232  man grep
  233  touch warzywa.txt
  234  nano warzywa.txt 
  235  grep marchewka warzywa.txt 
  236  grep marchew warzywa.txt 
  237  grep -n marchew warzywa.txt 
  238  grep -n sałata warzywa.txt 
  239  grep -nC sałata warzywa.txt 
  240  grep -nC 2 sałata warzywa.txt 
  241  grep -nC 1 sałata warzywa.txt 
  242  grep -nC 1 Sałata warzywa.txt 
  243  grep -niC 1 Sałata warzywa.txt 
  244  grep -niC 1 * warzywa.txt 
  245  grep -n * warzywa.txt 
  246  nano warzywa.txt 
  247  grep -n c* warzywa.txt 
  248  sort warzywa.txt 
  249  cat warzywa.txt 
  250  sort warzywa.txt 
  251  sort warzywa.txt > warzywa_sort.txt
  252  cat warzywa_sort.txt 
  253  sort -r warzywa.txt
  254  sort warzywa.txt
  255  sort -u warzywa.txt
  256  cp warzywa.txt salatka.txt
  257  nano salatka.txt 
  258  uniq salatka.txt 
  259  man uniq
  260  uniq -d salatka.txt 
  261  uniq -u salatka.txt 
  262  uniq -c salatka.txt 
  263  diff warzywa.txt salatka.txt 
  264  mkdir dir1 dir2
  265  cd dir1
  266  touch plik1.txt
  267  touch plik2.tst
  268  cd ..
  269  cd dir2
  270  touch plik1.txt
  271  cd ..
  272  diff dir1 dir2
  273  cd ..
  274  diff -y warzywa.txt salatka.txt
  275  cd 2TA/
  276  diff -y warzywa.txt salatka.txt 
  277  diff -y salatka.txt warzywa.txt
  278  diff -u dir1 dir2
  279  cd dir2/
  280  ls
  281  nano plik1.txt 
  282  cd ..
  283  diff -u dir1 dir2
  284  diff -u warzywa.txt salatka.txt 
  285  ssh 191.268.1.113
  286  ssh 191.168.1.113
  287  ssh marcin@191.168.1.113
  288  ping 192.168.1.113
  289  ssh root@191.168.1.113
  290  ssh admin@191.168.1.113
  291  ssh marcin@192.168.1.38
  292  ssh marcin@192.168.1.48
  293  ssh marcin@192.168.1.39
  294  ls
  295  ls -l
  296  cd 2ta
  297  cd 2TA/
  298  ls
  299  useradd
  300  adduser
  301  adduser User1
  302  sudo adduser User1
  303  sudo adduser User
  304  sudo adduser user
  305  su user
  306  pwd
  307  cd /home
  308  mkdir dokumenty
  309  sudo mkdir dokumenty
  310  ls -l
  311  cd dokumenty/
  312  touch plik1
  313  cd ..
  314  ls
  315  ls -l
  316  id
  317  sudo chown marcin dokumenty/
  318  ls 0l
  319  ls -l
  320  sudo chown :marcin dokumenty/
  321  ls -l
  322  cd dokumenty/
  323  touch dokumet.txt
  324  cd ..
  325  su user
  326  cd dokumenty/
  327  echo "Nowa linia" > dokumet.txt 
  328  cat dokumet.txt 
  329  su user
  330  addgroup grupa
  331  sudo addgroup grupa
  332  sudo addgroup grupa marcin
  333  sudo addgroup marcin grupa
  334  id
  335  sudo addgroup user grupa
  336  id
  337  user id
  338  id user
  339  id marcin
  340  cd ..
  341  ls -l
  342  chmod -r :grupa dokumenty
  343  chmod -r :grupa dokumenty/
  344  chown -r :grupa dokumenty
  345  chown -R :grupa dokumenty
  346  chown :grupa dokumenty
  347  sudo chown :grupa dokumenty
  348  ls -;
  349  ls -l
  350  cd dokumenty/
  351  ls -l
  352  ls 
  353  cd ..
  354  chmod +ro dokumenty/
  355  chmod r+o dokumenty/
  356  man chmod
  357  chmod +r dokumenty/
  358  ls 0l
  359  ls -l
  360  cd dokumenty/
  361  ls
  362  ls -l
  363  cd ..
  364  sudo chown -R :grupa dokumenty
  365  cd dokumenty/
  366  ls
  367  ls -l
  368  su user
  369  chmod g+w dokumet.txt 
  370  ls -l
  371  su user
  372  ls
  373  mkdir Dokumenty
  374  cd Dokumenty/
  375  touch haslo.txt
  376  echo "zaq1@WSX" > haslo.txt
  377  cat haslo
  378  cat haslo.txt 
  379  chown stefan haslo.txt 
  380  exit
  381  ssh marcin@192.168.1.39
  382  ls
  383  cd Dokumenty/
  384  cd ..
  385  rm -r Dokumenty
  386  ls
  387  mkdir Dokumenty
  388  ls -la Dokumenty/
  389  cd Dokumenty/
  390  cd ..
  391  cd Dokumenty
  392  cat salatka.txt
  393  touch salatka.txt
  394  echo "pomidor" > salatka.txt
  395  cat salatka.txt 
  396  chown kucharz salatka.txt 
  397  echo *
  398  echo "*"
  399  ls
  400  cd 2TA
  401  touch choinka.sh
  402  nano choinka.sh 
  403  ls
  404  ls choinka.sh 
  405  ls -l choinka.sh 
  406  chmod a+x
  407  chmod a+x choinka.sh 
  408  ls -l choinka.sh 
  409  ./choinka.sh 
  410  nano choinka.sh 
  411  ./choinka.sh 
  412  nano choinka.sh 
  413  ./choinka.sh 
  414  nano choinka.sh 
  415  ./choinka.sh 
  416  nano choinka.sh 
  417  ./choinka.sh 
  418  nano choinka.sh 
  419  ./choinka.sh 
  420  nano choinka.sh 
  421  ./choinka.sh 
  422  nano choinka.sh 
  423  ./choinka.sh 
  424  ls
  425  rm choinka.sh choinka_kolor.sh
  426  mv choinka.sh choinka_kolor.sh
  427  touch choinka_kolor.sh
  428  nano choinka_kolor.sh 
  429  chmod a+x choinka_kolor.sh 
  430  nano choinka_kolor.sh 
  431  ./choinka_kolor.sh 
  432  nano choinka_kolor.sh 
  433  ./choinka_kolor.sh 
  434  nano choinka_kolor.sh 
  435  ./choinka_kolor.sh 
  436  ls
  437  cd ~
  438  ls -a 
  439  nano .bashrc 
  440  ls
  441  cd skrypty/
  442  ls
  443  cd .
  444  cd ..
  445  cd 2TA
  446  mkdir skrypty
  447  cd skrypty/
  448  clear
  449  touch skrypt.sh
  450  nano skrypt.sh 
  451  skrypt.sh
  452  ./skrypt.sh
  453  ls -l
  454  chmod a+x skrypt.sh 
  455  ls -l
  456  ./skrypt.sh 
  457  nano skrypt.sh 
  458  ./skrypt.sh 
  459  cd ..
  460  ls choinka_kolor.sh 
  461  ./choinka_kolor.sh 
  462  nmcli
  463  sudo apt install network-manager
  464  nmcli
  465  man nmcli
  466  nmtui
  467  df
  468  df -h
  469  df -h /mnt/c
  470  df -h /mnt/c/
  471  du
  472  cd 2TA/
  473  du
  474  du -h
  475  cd /mnt/c/
  476  ls
  477  cd Users/marci/
  478  du -h
  479  ls
  480  cd Do
  481  cd Downloads/
  482  du -h
  483  du -h | sort
  484  man sort
  485  du -h | sort -h
  486  du -h | sort -hr
  487  cd ..
  488  du -h | sort -hr
  489  du -h | sort -hr | head
  490  cd Downloads/
  491  du -h | sort -hr | head
  492  du -hr | sort -hr | head
  493  man du
  494  du -ha | sort -hr | head
  495  du -ha | sort -hr
  496  du -ha | sort -hr | head
  497  history
  498  history | less
  499  cd ~
  500  touch zdjecie{2022..2023}{1..12}.jpg
  501  ls
  502  history | grep zdjecie*
  503  history | grep zdjecie
  504  touch zdjecie{1..10}.jpg
  505  history 
  506  history > /mnt/c/Users/marci/Desktop/history.txt
