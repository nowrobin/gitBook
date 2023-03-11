# Django s3 연동

```
s3 package install : pip install boto3 
django storage: pip install django-storages
```



```
# settings.py

# Static files (CSS, JavaScript, Images)
STATIC_URL = '/static/'

AWS_ACCESS_KEY_ID = '엑세스 키'
AWS_SECRET_ACCESS_KEY =  '엑세스 Secret 키'
AWS_REGION = 'ap-northeast-2'

###S3 Storages
AWS_STORAGE_BUCKET_NAME = '버킷이름' 
AWS_S3_CUSTOM_DOMAIN = '%s.s3.%s.amazonaws.com' % (AWS_STORAGE_BUCKET_NAME,AWS_REGION)
AWS_S3_OBJECT_PARAMETERS = {
    'CacheControl': 'max-age=86400',
}
DEFAULT_FILE_STORAGE = 'storages.backends.s3boto3.S3Boto3Storage'
```





