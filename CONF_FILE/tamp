#!/usr/bin/env bash

if [ -f ~/../usr/var/lib/serverkhanh ] 2> /dev/null; then
    clear
    printf "${light_cyan}\n\n Github: https://github.com/khanhnguyen9872\n Facebook: https://fb.me/khanh10a1\n\n"
    printf "${red}\n\nServer Ninja Termux cua Khanh da tat!\n\n Ban khong the truy cap vao tinh nang nay!\n Vui long ket noi Internet de kiem tra Server\n\n${reset}"
    exit 0
fi

option="${1}" 
case ${option} in 
   -start) 
	   if ps -C httpd >/dev/null; then
		   echo "apache2 service still running..."
	   else
	   	echo "Starting MySQL/Apache2...."
		httpd &> /dev/null
		mysqld --skip-grant-tables --general-log &> /dev/null
		printf "\nSQL is stopped!\n";
		echo "";
	   fi
      ;; 
   -stop)
   	   echo "Stopping MySQL/Apache2...."
	   killall httpd
	   killall mysqld &> /dev/null
	   killall /data/data/com.termux/files/usr/bin/mariadbd &> /dev/null
	   killall mysqld_safe &> /dev/null
	   printf "\nSQL is stopped!\n";
	   echo "";

      ;;
   *)  
      echo "KhanhNguyen9872"
      echo "Github: https://github.com/khanhnguyen9872"
      echo "FB: https://fb.me/khanh10a1"
      exit 1
      ;; 
esac
