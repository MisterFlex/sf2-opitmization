# sf2-opitmization


La seule requête importante est la master request
Le test ci dessous nous fait économiser du temps en ne s'occupant pas des sub-requests qui sont souvent nombreuses

---

```php
public function onKernelRequest(GetResponseEvent $event) {
        if (!$event->isMasterRequest()) {
            return;
        }
        
        // write your code here
 }
 ```
