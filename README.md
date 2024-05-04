# userful-docs

Flask - Gunicorn - Nginx setup - https://aws.plainenglish.io/deploying-a-flask-application-on-ec2-54cfeb396fa1

SSL certi - https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/

Subdomains - https://www.namecheap.com/support/knowledgebase/article.aspx/9776/2237/how-to-create-a-subdomain-for-my-domain/ 
          https://stackoverflow.com/questions/21763205/how-can-i-find-my-nameservers-on-amazon-ec2-server

Celery daemon - https://medium.com/@dipghoshraj/run-background-jobs-in-python-with-celery-and-redis-0988d2381fe8#:~:text=save%20and%20move%20this%20file,celery%20worker%20in%20the%20background.&text=Celery%20and%20Redis%20allow%20you%20to%20track%20task%20status%20and%20store%20results.
Commands: 
celery -A app.shortsgenie worker --loglevel INFO -E

sudo apt-get update && sudo apt-get install ffmpeg libsm6 libxext6  -y

export NODE_OPTIONS=--openssl-legacy-provider npm run build cp -r build/* /var/www/notioncharty/html/

gunicorn --certfile notioncharty.com.crt --keyfile notioncharty.com.key -b 0.0.0.0:5000 app:app -w 6 --daemon --reload

