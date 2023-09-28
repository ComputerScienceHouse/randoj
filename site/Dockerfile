FROM ninjaclasher/dmoj-base:latest

EXPOSE 8000

COPY uwsgi.ini .

RUN git clone --depth=1 https://github.com/DMOJ/online-judge /site

ENTRYPOINT uwsgi --ini uwsgi.ini
