The nginx njs module allows javascript to process the code. The module is dynamic for Nginx Plus https://docs.nginx.com/nginx/admin-guide/dynamic-modules/dynamic-modules/ while for the community nginx it needs to be precompiled.


![image](https://github.com/user-attachments/assets/c838f0c0-ef85-4de1-b8ce-ac510b636779)



I have used the example rate limiter from https://github.com/nginx/njs-examples and modified it to be based on the reques body.


It works as expected. The "r.internalRedirect('@app-backend');" internal redirect is needed as nginx by default does not populate or save the request body and this is why the request needs to pass 2 times in nginx!


The nginx plus rootless container is a great option for F5 XC RE where root containers are not accepted. 
