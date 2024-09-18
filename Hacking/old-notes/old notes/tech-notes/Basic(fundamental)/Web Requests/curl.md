curl https://web.com

curl -o output.txt

curl -v site.com  :    **to see all headers and information**

curl -vvv              :    **to see more information and headers  (test for use of many -vvvvvvvv )**

curl -I -v              :     **to see request headers**

curl -i                   :      **to see request and responde headers**

curl -A 'Mozilla/5.0'   :    **to set own user agent**

curl -u admin:pass site.com : **to give credencials**