# UnityObjectPooler
## Simple object pool for Unity

This is a quick and lightweight solution that you can just immediately throw objects at to be pooled.  (.Net 4.6+)

 - No need to pre-define pools (although you can if you want).
 - Calls Spawn/Despawn interface
 - Neatly organized in project hierarchy

###### Instantiating objects (taking them from the pool):
```
var obj = ObjectPooler.Instance.Spawn(prefab, position, rotation);
```

###### Destroying objects (adding them back into the pool):
```
ObjectPooler.Instance.Despawn(gameObject);   
```

###### Preparing objects for re-use. 
```
public class Enemy : MonoBehaviour, IPoolable
{
    public void Spawn()
    {
        // do stuff...
    }

    public void Despawn()
    {
        // do stuff...
    }
}
```
