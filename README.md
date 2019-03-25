# sf2-opitmization

### OnKernelRequest Optimization

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

### Composer dump optimization

see <https://getcomposer.org/doc/06-config.md#optimize-autoloader>

Ne pas faire ça en mode developpement.

En production ceci va générer un classmap de notre autoloder 
Vérification de l'existance du fichier en moins dans la liste des opérations

---

```
 "config": {
        "optimize-autoloader": true
    },
    
 composer dump-autoload --optimize
 
```
