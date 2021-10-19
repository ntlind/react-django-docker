web: gunicorn starter_app.wsgi --chdir backend --limit-request-line 8188 --log-file -
worker: REMAP_SIGTERM=SIGQUIT celery --workdir backend --app=starter_app worker --loglevel=info
beat: REMAP_SIGTERM=SIGQUIT celery --workdir backend --app=starter_app beat -S redbeat.RedBeatScheduler --loglevel=info
