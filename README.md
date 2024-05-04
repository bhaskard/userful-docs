# userful-docs

Flask - Gunicorn - Nginx setup - https://aws.plainenglish.io/deploying-a-flask-application-on-ec2-54cfeb396fa1

SSL certi - https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/

Subdomains - https://www.namecheap.com/support/knowledgebase/article.aspx/9776/2237/how-to-create-a-subdomain-for-my-domain/ 
          https://stackoverflow.com/questions/21763205/how-can-i-find-my-nameservers-on-amazon-ec2-server

Commands: 
celery -A app.shortsgenie worker --loglevel INFO -E

sudo apt-get update && sudo apt-get install ffmpeg libsm6 libxext6  -y

export NODE_OPTIONS=--openssl-legacy-provider npm run build cp -r build/* /var/www/notioncharty/html/

gunicorn --certfile notioncharty.com.crt --keyfile notioncharty.com.key -b 0.0.0.0:5000 app:app -w 6 --daemon --reload

