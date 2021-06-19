# Read : 32

## Permissions in Django REST Framework (DRF)

- Permissions are used for different classes of users and for different parts of the API. 

- DRF always check permissions before running any code in views.

- Permissions in DRF represent a list of classes that must be checked before any code executes. 

- There are 7 pre-built permission classes in DRF:

    - `AllowAny`
    - `IsAuthenticated`
    - `IsAdminUser`
    - `IsAuthenticatedOrReadOnly`
    - `DjangoModelPermissions`
    - `DjangoModelPermissionsOrAnonReadOnly`
    - `DjangoObjectPermissions`

- You can either build custom classes by yourself.

- Permissions in Django REST Framework may be set in 3 different ways:

    1. Globally to all API endpoints.
    2. Into the views or viewsets.
    3. On an object level.

1.
```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.AllowAny',
    ]
}
```

2.
```
from rest_framework.permissions import IsAuthenticated
class UserViewSet(viewsets.ModelViewSet):
    queryset = User.objects.all().order_by('-date_joined')
    serializer_class = UserSerializer
    permission_classes = [IsAuthenticated]
```

3.
```
from rest_framework import permissions
class IsAssigned(permissions.BasePermission): 
    def has_object_permission(self, request, view, obj):
		# check if user who launched request is object owner 
        if obj.assigned_to == request.user: 
            return True
        else:
            return False
```

##### [Go Back](code_401_reading_notes.md)