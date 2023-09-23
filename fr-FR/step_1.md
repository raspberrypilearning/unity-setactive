Tu peux utiliser `SetActive(true)` pour activer un GameObject et `SetActive(false)` pour désactiver un GameObject afin qu'il n'apparaisse pas.

Tu peux utiliser `SetActive` sur une variable publique et faire glisser un GameObject dans l'Inspector :

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

Tu peux aussi utiliser `SetActive` sur tous les GameObjects avec le même tag :

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
