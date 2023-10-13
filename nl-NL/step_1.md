Je kan `SetActive(true)` gebruiken om een GameObject te activeren, en `SetActive(false)` om het te deactiveren zodat het niet verschijnt.

Je kan `SetActive` gebruiken op een public variabele en een GameObject naar de Inspector slepen:

--- code ---
---
language: cs
---

public GameObject hart;

void Start()
{
    hart.setActive(false);
}

public void SpelerKlaar()
{
    hart.SetActive(true);
}

--- /code ---

Je kunt `SetActive` ook gebruiken op alle GameObjects met dezelfde tag:

--- code ---
---
language: cs
---

public GameObject sterren;

void Start()
{
    sterren = GameObject.FindGameObjectsWithTag("Ster");
    foreach (var ster in sterren)
    {
        ster.SetActive(false);
    }
}

public void SpelerKlaar()
{
    isKlaar = true;
    startTijd = Time.time;
    canvas.SetActive(false);
    
    foreach (var ster in sterren)
    {
        ster.SetActive(true);
    }
}

--- /code ---
