FROM ninjaclasher/dmoj-base:latest

EXPOSE 8000

RUN git clone --depth=1 https://github.com/DMOJ/online-judge /site

WORKDIR /site

COPY uwsgi.ini .

ENTRYPOINT uwsgi --ini uwsgi.ini
