---
description: macOS로 django 실습
---

# Django 시작하기

## 가상환경 생성

```python
python -m venv venv
```

But Why do we need Virtual Environment

가상환경을 생성하는 이유:&#x20;

1\) 프로젝트를 진행하면서 여러 패키지들을 생성하는데, 가상환경을 사용하지않으면 나중에 pip install을 할때  다른 프로젝트에서 사용했던 패키지들 까지 설치하는 불필요한 공간 차지 와 작업을 한다. 특히 유료 서버를 사용한다고 했을때 불필요한 비용을 절감할수있다.

2\) 호환성, 패키지들이 업데이트를 하면서 호환이 안되는일을 많이 경험했다. 그때 당시 버전문제라고 정확하게 에러를 알려주지않아서 삽질만 여러번했는데 결국 패키지들간에 호환된 버전 문제였다. 이러한 문제들을 덜발생하기위해서 가상환경을 사용한다.&#x20;

<pre><code><strong>source venv/bin/activate //가상환경 activate
</strong><strong>//터미널에서 앞에 (venv)가 나타나면 가상환경 실행중
</strong><strong>deacitve//가상환경 빠져나오기 
</strong></code></pre>

## Django 설치&#x20;

```
python3 -m pip install django
djaango-admin startproject **프로젝트이름**  **경로**
```

## env 생성

프로젝트에 필요하지만 가려야하는 내용들을 저장하기위해서 env파일 만들어서 관리해준다.

```
cp env.template .env
```

## requirement.txt&#x20;

필요한 패키들의 버전을 txt 파일로 지정하여 버전을 맞추는 작업을 해야한다

```
pip install -r backend/requirements.txt
```

해당 강의에서 사용한 requirements:&#x20;

```
asgiref==3.5.2
Django==4.1.3
django-extensions==3.2.1
django-filter==22.1
djangorestframework==3.14.0
djangorestframework-jsonapi==6.0.0
inflection==0.5.1
python-dotenv==0.21.0
pytz==2022.6
sqlparse==0.4.3
tzdata==2022.6
```

## 서버실행

```
python3 manage.py runserver **port**
```

## 실행되는 흐름

![](../../.gitbook/assets/image.png)

## App 생성

```
django-admin startapp **앱이름** 
```



## Reference

{% embed url="https://opentutorials.org/course/4886/31113" %}
섕활코딩&#x20;
{% endembed %}

{% embed url="https://www.youtube.com/watch?v=tujhGdn1EMI" %}
Django 실습
{% endembed %}

