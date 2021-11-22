You can use `SetActive(true)` to activate a GameObject and `SetActive(false)` to deactive a GameObject so that it doesn't appear. 


You can use `SetActive` on a public variable and drag a GameObject in the Inspector:

```
public GameObject heart;

void Start()
{
    heart.setActive(false)
}

public void PlayerReady()
{
    heart.SetActive(true);
}

```

You can also use `SetActive` on all GameObjects with the same tag:

```
public GameObject stars;

void Start()
{
    stars = GameObject.FindGameObjectsWithTag("Star");
    foreach (var star in stars)
    {
        star.SetActive(false);
    }
}

public void PlayerReady()
{
   IsReady = true;
    ButtonTime = Time.time;
    canvas.enabled = false;
    foreach (var star in stars)
    {
        star.SetActive(true);
    }
}

```
