# Exercise Outcomes Submission Template

**Student/Group Name**: Blanca Abril
**Level Completed**: master
**Date**: 03/01/2026

---

## 📋 Exercise Summary

### Exercise: Rewriting History (Rebase and Amend Commits)
**Status**: ✅ Completed

**What I did**:
Aprendí a usar `git commit --amend` para corregir commits, `git rebase -i` para limpiar el historial fusionando commits, y `git rebase` para mantener historias lineales al actualizar ramas feature. Además analicé cómo cambian los SHAs al reescribir historia y comprendí los riesgos de reescribir historia pública.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
echo "version=1.0" > config.txt
git add config.txt
git commit -m "Add configuration file"
echo "environment=production" >> config.txt
git add config.txt
git commit --amend -m "Add complete configuration file"
git log --oneline -n 3
echo "Feature A" > featureA.txt
git add featureA.txt
git commit -m "Add feature A"
echo "Feature B" > featureB.txt
git add featureB.txt
git commit -m "Add feature B"
echo "Fix typo in A" >> featureA.txt
git add featureA.txt
git commit -m "Fix typo"
git config --global core.editor "nano"
git rebase -i HEAD~3
git log --oneline -n 5
git checkout -b feature/awesome-feature
echo "Awesome Feature" > awesome.txt
git add awesome.txt
git commit -m "Add awesome feature"
git checkout master
echo "Master update" > master-update.txt
git add master-update.txt
git commit -m "Update on master branch"
git checkout feature/awesome-feature
git rebase master
git log --graph --oneline --all -n 10
git reflog
git log origin/master..master --oneline
```

**Results/Output**:
```
PART 1 

$ git log --oneline -n 3
87b3512 (HEAD -> master) Add complete configuration file
d4af8aa fallo al pisar el readme
2af724d Add configuration file

PART 2

$ git log --oneline -5
13041cc (HEAD -> master) Add feature B
0db0e76 Add feature A
87b3512 Add complete configuration file
d4af8aa fallo al pisar el readme
2af724d Add configuration file

PART 3

$ git log --graph --oneline --all -n 10
* 162feb7 (HEAD -> feature/awesome-feature) Add awesome feature
* 5fe4331 (master) Update on master branch
* 13041cc Add feature B
* 0db0e76 Add feature A
* 87b3512 Add complete configuration file
* d4af8aa fallo al pisar el readme
* 2af724d Add configuration file
* b5d8eb6 (origin/master) refactor: consolidate master exercises...

$ git reflog
162feb7 HEAD@{0}: rebase (finish): returning to refs/heads/feature/awesome-feature
d1cde86 HEAD@{5}: commit: Add awesome feature (SHA original antes de rebase)
a0c27be HEAD@{17}: commit: Fix typo (SHA original antes de fixup)
e7ed1a8 HEAD@{23}: commit: fallo al pisar el readme (SHA original antes de amend)

# Verificar commits privados:
$ git log origin/master..master --oneline
5fe4331 (master) Update on master branch
13041cc Add feature B
0db0e76 Add feature A
87b3512 Add complete configuration file
d4af8aa fallo al pisar el readme
2af724d Add configuration file


```


---

## 🎯 Key Learnings

**Main concepts I learned**:
1. Cómo funciona la reescritura del historial en Git 
2. El uso de commit --amend para corregir el último commit sin crear uno nuevo.
3. La diferencia crítica entre commits que ya has pusheado (públicos/compartidos) y commits locales (privados)

**Skills I improved**:
- Distinguir entre commits privados y públicos
- Análisis y recuperación de cambios usando git reflog.

---

## 🚧 Challenges Faced

### Challenge 1: [Brief title]
**Problem**: El editor de base no sabía utilizarlo ya que es vim

**Solution**: Configuré Git para usar nano como editor por defecto con `git config --global core.editor "nano"`, que es más intuitivo.

**Commands/Approach**:
```bash
git config --global core.editor "nano"
git rebase -i HEAD~3
```

---

### Challenge 2: [Brief title]
**Problem**: No tenía claro cuándo es seguro reescribir historia y cuándo es peligroso.

**Solution**: Aprendí a usar `git log origin/master..master --oneline` para ver qué commits son solo locales. Si el comando muestra commits, son privados. Si está vacío, están en origin y es peligroso reescribirlos.

---

## 💭 Personal Reflection

**What surprised me**:
Me sorprendió lo potente que es Git para modificar el historial

**What I found most difficult**:
Lo más complicado fue entender las consecuencias de reescribir el historial y ver cuándo puede afectar negativamente al trabajo de otros desarrolladores.

**What I found most useful**:
El uso de rebase para mantener un historial limpio me parece especialmente útil para proyectos profesionales.

**How I would apply this in real projects**:
Aplicaría estas técnicas únicamente en ramas privadas o antes de integrar cambios en ramas principales.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | 5 | Tengo dominio con los comandos básicos|
| Branching & merging | 4 | Me defiendo bien|
| Remote operations | 4 | Me defiendo bien y he podido solucionar los problemas correctamente |
| Conflict resolution | 4 | Los que ha habido, los he resuelto correctamente|
| History rewriting | 3 | Lo entiendo pero me ha costado |
| Git hooks | 1 | No hecho aún|
| Security practices | 2 | Entiendo los riesgos, ahora solo falta practicarlo |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/blancabgz/taller-master-ugr/tree/group-16-outcomes/master`
- Key commits demonstrating your work:
  - Update on master branch (5fe4331)
  - Add feature B (13041cc)
  - Add feature A (0db0e76)
  - Add complete configuration file (87b3512)
  

**Additional files created** (if any):
- config.txt
- featureA.txt
- featureB.txt
- awesome.txt
- master-update.txt

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [x] Completed the exercise for your chosen level (including all parts)
- [x] Documented all commands used with their outputs
- [x] Described challenges and how you resolved them
- [x] Provided a thoughtful reflection on your learning
- [x] Self-assessed your confidence in each topic
- [x] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

Lo mismo que anteriormente, el grupo que he puesto es el 16 pero estoy sola. 

---

**Submission Date**: [03/01/2026]  
**Ready for Review**: ✅ Yes
