# sf2-opitmization

```php

La seule requête importante est la master request 
Le test ci dessous nous fait économiser du temps en ne s'occupant pas des sub-requests qui sont souvent nombreuses
---

public function onKernelRequest(GetResponseEvent $event) {
        if (!$event->isMasterRequest()) {
            // don't do anything if it's not the master request
            return;
        }
        
        // write your code here
 }
 ```
