FROM python:3.8

RUN mkdir /var/www
# workdirの指定
WORKDIR /var/www

# 依存Pythonライブラリ一覧コピー
COPY requirements.txt ./

# 依存Pythonライブラリインストール
RUN pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

COPY . /var/www/ 

CMD ["uwsgi","--ini","/var/www/uwsgi.ini"]


