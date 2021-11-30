You can use `SetActive(true)` to activate a GameObject and `SetActive(false)` to deactive a GameObject so that it doesn't appear. 


You can use `SetActive` on a public variable and drag a GameObject in the Inspector:

--- code ---
---
language: cs
---
public GameObject heart;

void Start()
{
    heart.setActive(false);
}

public void PlayerReady()
{
    heart.SetActive(true);
}

--- /code ---

You can also use `SetActive` on all GameObjects with the same tag:

--- code ---
---
language: cs
---
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
    canvas.SetActive(false);
    foreach (var star in stars)
    {
        star.SetActive(true);
    }
}
--- /code ---
