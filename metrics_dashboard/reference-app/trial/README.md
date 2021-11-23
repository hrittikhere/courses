### setup python env
```
python3.9 -m venv py39_env
source py39_env/bin/activate
pip3 install --upgrade pip
pip install -r requirements.txt
```


### to run locally
```
$ source py39_env/bin/activate
$ gunicorn --access-logfile - --error-logfile - -w 4 -b 0.0.0.0:8080 app:app
```

### docker build and push
```
docker build --no-cache -t jasonwee/metrics-dashboard-trial .
docker push jasonwee/metrics-dashboard-trial
```
