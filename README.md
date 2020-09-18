# Linux service cli
Following are multiple ways to manage services
- systemctl
    - ubuntu 18.4, debian etc uses this. This is standard 
- service
- init.d
    - deprecated

# systemd
systemd calls daemon units. Following are part of sustemd suite
- systemctl
- journalctl
# systemctl
- Check status of all services
    ```
    systemctl stauts
    ```
- Check status of individual service
    ```
    systemctl status apache2
    ```
- Stop service
    ```
    systemctl stop apache2
    ```
- Start the service
    ```
    systemctl start apache2
    ```
- Restart the service
    ```
    systemctl restart apache2
    ```
# service
- Check status of all services
```
service --status-all
```
- Check status of specific service
```
service apache2 status
```
- Stop service
```
service apache2 stop
```
- Start service
```
service apache2 start
```
- Restart service
```
service apache2 restart
```
# init.d
- Get status
```
sudo  /etc/init.d/apache2 status
```
- Stop service 
```
sudo /etc/init.d/apache2 stop
```
- Start service
```
sudo /etc/init.d/apache start
```
- Restart service
```
sudo /etc/init.d/apache restart
```
# journalctl
Part of systemd suite. 
```
journalctl -b
journalctl -u kubelet
```
