# Exercise Outcomes Submission Template

**Student/Group Name**: Blanca Abril González
**Level Completed**: intermediate
**Date**: 02/01/2026

---

## 📋 Exercise Summary

### Exercise: Intermediate Level
**Status**: ⏳ In Progress 

**What I did**:
En este ejercicio trabajé con comandos de dificultad intermedia de Git centrados en integración de ramas en una, resolución de conflictos y el uso de etiquetas. Lo que hice fué crear dos ramas a partir de la rama intermediate, que modificaban el mismo archivo para provocar un conflicto, de forma manual, mediante el editor, resolví el conflicto generado manteniendo ambos cambios y creé el commit. Además cree y comparé etiquetas para comprender el uso.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
git checkout intermediate
git branch
git checkout -b feature/header
git checkout -b feature/footer
git checkout feature/header
git add page.html 
git commit -m "Add header to page"
git checkout feature/footer
git add page.html 
git commit -m "Add footer to page"
git checkout intermediate
git merge feature/header
git merge feature/footer
git add page.html
git commit -m "Merge footer with resolved conflicts"
git log --graph --oneline --all
git tag -a v1.0 -m "First stable version with merged features"
git tag
git show v1.0
git push origin v1.0
git tag v1.0-test
git show v1.0
git show v1.0-test
```

**Results/Output**:
```
git log --graph --oneline --all
*   745d0d5 (HEAD -> intermediate) Merge footer with resolved conflicts
|\  
| * b0d5dc1 (feature/footer) Add footer to page
| * 8876637 Add header to page
* | 949a2cb (feature/header) Add header to page
|/  
* 994450b (origin/intermediate) refactor: consolidate intermediate exercises into single comprehensive exercise
* a1c17e7 docs: Add submission instructions to intermediate level
* 9f25f7a Update README for intermediate level exercises
| * 9526d87 (origin/group-16-outcomes/newbie, group-16-outcomes/newbie) Completado el archivo outcomes
| * 4384c28 Archivo OUTCOMES rellenado
| * 6d49f17 Archivo OUTCOMES rellenado
| | * be20ed8 (origin/feature/my-info, feature/my-info) Add personal information
| |/  
| * 88d2a24 (origin/newbie, newbie) Add hello.txt with my name
| * 360f4a4 refactor: consolidate newbie exercises into single comprehensive exercise
| * 5eedc97 docs: Add submission instructions to newbie level
| * 45e1c31 Update README for newbie level exercises
|/  
| * 9602351 (origin/main, origin/HEAD, main) Adding GenAI guidelines
| * 7ad3af4 docs: update main branch files to reflect consolidated exercise structure (1 per level)
| * 4d9131e chore: remove instructor files from repository tracking
| *   adbb307 Merge pull request #9 from miguel-oltra/patch-gitignore-update
| |\  
| | * e4709e6 Updated CODEOWNERS file
| | * 2a39a02 chore: add INSTRUCTOR_GUIDE.md to gitignore


```

```
git tag
v0.0.1
v1.0
```

```
git show v1.0

tag v1.0
Tagger: Blanca <blancabrilgonz@correo.ugr.es>
Date:   Fri Jan 2 20:08:07 2026 +0100

First stable version with merged features

commit 745d0d57b7d43ffc6877a12a97b4c9577a635f69 (HEAD -> intermediate, tag: v1.0-test, tag: v1.0)
Merge: 949a2cb b0d5dc1
Author: Blanca <blancabrilgonz@correo.ugr.es>
Date:   Fri Jan 2 20:06:41 2026 +0100

    Merge footer with resolved conflicts
```

```
git show v1.0-test
commit 745d0d57b7d43ffc6877a12a97b4c9577a635f69 (HEAD -> intermediate, tag: v1.0-test, tag: v1.0)
Merge: 949a2cb b0d5dc1
Author: Blanca <blancabrilgonz@correo.ugr.es>
Date:   Fri Jan 2 20:06:41 2026 +0100

    Merge footer with resolved conflicts
```

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. Cómo funcionan los merges en Git y por qué se producen conflictos.
2. El uso de etiquetas


**Skills I improved**:
- Resolución manual de conflictos
- Uso del log
- Uso de tags para versionar un proyecto.

---

## 🚧 Challenges Faced

### Challenge 1: Resolución de un conflicto
**Problem**: Al fusionar dos ramas en una creó un conflicto.

**Solution**: Analicé los marcadores de conflicto dentro del archivo, entendí que cambios pertenecían a cada rama, acepté los cambios de ambas ramas para conservar tanto el header como el footer. Por último realicé un commit. 

**Commands/Approach**:
```bash
git merge feature/footer
nano page.html
git add page.html
git commit -m "Merge footer with resolved conflicts"
```

---

## 💭 Personal Reflection

**What surprised me**:
Me sorprendió que Git no sea capaz de manejar este tipo de conflictos y sea el desarrollador el que lo tenga que hacer.

**What I found most difficult**:
Ver en un conflicto que cambio pertenece a qué rama.

**What I found most useful**:
La resolución de conflictos es una habilidad muy útil en proyectos reales donde varias personas pueden modificar el mismo archivo. 

**How I would apply this in real projects**:
En proyectos profesionales usaría ramas para desarrollar funcionalidades independientes para después resolver los conflictos que se generen en caso de haberlos. 

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | 5 | Uso fluido |
| Branching & merging | 5 | He comprendido claramente como funcionaba|
| Remote operations | 3 | La parte de las ramas bien, pero la parte de los tags no lo había hecho nunca|
| Conflict resolution | 5 | Resolución de conflictos|
| History rewriting | 5 | No se ha trabajado en este nivel |
| Git hooks | 5 | No se ha trabajado en este nivel|
| Security practices | 5 | No se ha trabajado en este nivel|

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/blancabgz/taller-master-ugr/tree/group-16-outcomes/intermediate`
- Key commits demonstrating your work:
  - Commit hash: [Short description]
  - Commit hash: [Short description]

**Additional files created** (if any):
- File 1: [Description]
- File 2: [Description]

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- x Completed the exercise for your chosen level (including all parts)
- x Documented all commands used with their outputs
- x Described challenges and how you resolved them
- x Provided a thoughtful reflection on your learning
- x Self-assessed your confidence in each topic
- [] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

Lo mismo que en el primero, el grupo es 16 pero no estoy en ese grupo pero estoy sola por ser online

---

**Submission Date**: 02/01/2026
**Ready for Review**: ❌ No
