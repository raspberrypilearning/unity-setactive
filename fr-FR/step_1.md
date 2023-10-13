Tu peux utiliser `SetActive(true)` pour activer un GameObject et `SetActive(false)` pour désactiver un GameObject afin qu'il n'apparaisse pas.

Tu peux utiliser `SetActive` sur une variable publique et faire glisser un GameObject dans l'Inspector :

--- code ---
---
language: cs
---

public GameObject cœur;

void Start()
{
    cœur.setActive(false);
}

public void JoueurPret()
{
    cœur.SetActive(true);
}

--- /code ---

Tu peux aussi utiliser `SetActive` sur tous les GameObjects avec le même tag :

--- code ---
---
language: cs
---

public GameObject etoiles;

void Start()
{
    etoiles = GameObject.FindGameObjectsWithTag("Etoile");
    foreach (var etoile in etoiles)
    {
        etoile.SetActive(false);
    }
}

public void JoueurPret()
{
    estPret = true;
    demarrageTemps = Time.time;
    canvas.SetActive(false);
    
    foreach (var etoile in etoiles)
    {
        etoile.SetActive(true);
    }
}

--- /code ---
