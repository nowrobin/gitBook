# DRF  URL vs.  Router



URL  과 viewset 과 연결시켜줘야 한다, 따라서 viewset 에서 작성시에 필요로한 메소드들을 직접적으로 작성 해야한다.

````
```python url.py
urlpatterns = [
    path('api/v1/recruits/<uuid:pk>/comments/', recruit_views.CommentViewSet.as_view()), # 
]
````



### but how about the router:&#x20;

Routers provide a convenient and consistent way of **automatically**\
**determining the URL conf for your API**.

URL의 config를 자동적으로 연동? 시켜주기때문에 따러 GET, POST등의 필수적인 메소드들을 사용하지않고 오버라이딩을 통해 진행된다.







