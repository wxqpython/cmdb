# cmdb
```
import subprocess
>>> p1 = subprocess.Popen(['df', '-Th'], stdout=subprocess.PIPE)
>>> p2 = subprocess.Popen(['grep', 'data'], stdin=p1.stdout, stdout=subprocess.PIPE)
>>> out,err = p2.communicate()
# p2.stdout.read()
```

Django视图函数免除csrf_token
```
from django.views.decorators.csrf import csrf_exempt

@csrf_exempt
def index(request):
    return HttpResponse("post data...")
```
