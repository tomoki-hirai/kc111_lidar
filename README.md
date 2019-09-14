# kc111_lidar
## raspberry piの設定
### screenのインストール
- バックグラウンドで実行する用
- sudo apt install -y screen
### crontabのログ設定
- /etc/rsyslog.confを開き、*cron.*              /var/log/cron.log*のコメントアウト外す
- sudo /etc/init.d/rsyslog restart
- ログはvar/log/cron.log
### crontabの設定
- MTAがないのでインストール sudo apt-get install postfix
- crontab -e で設定ファイルを開く
- *@reboot sh /home/pi/kc111_lidar/start.sh > /home/pi/cron_log.txt*を末尾に追加
 
 
 
 
 
