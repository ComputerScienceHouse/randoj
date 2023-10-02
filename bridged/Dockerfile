FROM ninjaclasher/dmoj-base:latest

EXPOSE 9999
EXPOSE 9998

RUN git clone --depth=1 https://github.com/DMOJ/online-judge.git /site

ENV HOST=localhost
ENV DEBUG=1
ENV SECRET_KEY=chom
ENV DJANGO_SETTINGS_MODULE=dmoj.settings

WORKDIR /site

RUN git submodule update --init --recursive
RUN mkdir /pdfcache

COPY local_settings.py /site/dmoj/local_settings.py

ENTRYPOINT python3 manage.py runbridged
