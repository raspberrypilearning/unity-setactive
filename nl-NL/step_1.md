Je kan `SetActive(true)` gebruiken om een GameObject te activeren, en `SetActive(false)` om het te deactiveren zodat het niet verschijnt.

Je kan `SetActive` gebruiken op een public variabele en een GameObject naar de Inspector slepen:

--- code ---
---
language: cs
---

public GameObject heart;

void Start()
{ heart.setActive(false); }

public void PlayerReady()
{ heart.SetActive(true); }

--- /code ---

Je kunt `SetActive` ook gebruiken op alle GameObjects met dezelfde tag:

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
{ isReady = true; startTime = Time.time; canvas.SetActive(false);

    foreach (var star in stars)
    {
        star.SetActive(true);
    }
}

--- /code ---
