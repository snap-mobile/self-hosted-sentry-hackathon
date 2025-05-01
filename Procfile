web: uwsgi --ini=uwsgi.ini --http=0.0.0.0:$PORT -p1
worker: sentry --config=sentry.conf.py celery worker --loglevel=DEBUG -c1
beat: sentry --config=sentry.conf.py celery beat --loglevel=DEBUG
worker_plus_beat: sentry --config=sentry.conf.py celery worker -c1 -B --loglevel=DEBUG