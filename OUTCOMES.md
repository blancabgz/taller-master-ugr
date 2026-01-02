# Exercise Outcomes Submission Template

**Student/Group Name**: Blanca Abril Gonzálezz  
**Level Completed**: newbie
**Date**: 02/01/2026

---

## 📋 Exercise Summary

### Exercise: [Exercise Title]
**Status**: ✅ Completed

**What I did**:
En este ejercicio he trabajado con funcionalidad básica de Git para comprender mejor el flujo de trabajo. He configurado mi identidad, he creado y comiteado archivos, he revisado el log de commits, he creado ramas y me he movido entre ellas.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
git clone https://github.com/miguel-oltra/taller-master-ugr
git branch
git config --global user.name "Blanca"
git config --global user.email "blancabrilgonz@correo.ugr.es"
git status
touch hello.txt
git status
git add hello.txt 
git commit -m "Add hello.txt with my name"
git log
git checkout -b feature/my-info
touch my-info.txt
git add my-info.txt
git commit -m "Add personal information"
git remote -v
git remote set-url origin https://github.com/blancabgz/taller-master-ugr
git push origin feature/my-info
git checkout newbie
git push -u origin newbie
git pull origin newbie
git checkout -b group-16-outcomes/newbie
git checkout main -- OUTCOME_TEMPLATE.md
```

**Results/Output**:

git log --oneline -5

88d2a24 (HEAD -> group-16-outcomes/newbie, origin/newbie, newbie) Add hello.txt with my name
360f4a4 refactor: consolidate newbie exercises into single comprehensive exercise
5eedc97 docs: Add submission instructions to newbie level
45e1c31 Update README for newbie level exercises
dc58203 Revert "Update README.md"


git branch -a
  feature/my-info
* group-16-outcomes/newbie
  main
  newbie
  remotes/origin/HEAD -> origin/main
  remotes/origin/feature/my-info
  remotes/origin/intermediate
  remotes/origin/main
  remotes/origin/master
  remotes/origin/master-of-the-universe
  remotes/origin/newbie


---

## 🎯 Key Learnings

**Main concepts I learned**:
1. Como funciona el flujo de trabajo
2. Como crear y cambiar de rama 
3. La diferencia entre rama local y remota

**Skills I improved**:
- Usar mejor Git por terminal
- Gestionar ramas remotas
- Gestionar un fork para cambiar de un proyecto al mio propio

---

## 🚧 Challenges Faced

### Challenge 1: Permiso denegado al intentar hacer push
**Problem**: Cuando intenté hacer git push origin feature/my-info, me dió un error de permiso 403 porque no tenía permisos en el repositorio original.

**Solution**:

Aprendí que cuando no eres colaborador en un repositorio, debes trabajar en un fork. Creé un fork del repositorio en GitHub y actualicé mi control remoto de origen local para apuntar a mi fork en lugar de al del profesor.
**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
git remote set-url origin https://github.com/blancabgz/taller-master-ugr
git push -u origin feature/my-info
```


---

### Challenge 2: Error al hacer pull de una rama inexistente en el remoto
**Problem**: Al ejecutar git pull origin newbie falló porque la rama aún no existía.

**Solution**: 
Para resolverlo, use push para subir la rama local a remoto.

**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
git push -u origin newbie
```
---

## 💭 Personal Reflection

**What surprised me**:
Realmente no me sorprendió nada porque había usado Git anteriormente

**What I found most difficult**:
Lo que se me hizo más complicado fue la gestión de las ramas remotas y locales, es lo que puede ser más lioso de este nivel.

**What I found most useful**:
El uso de ramas y el trabajo con repositorios remotos para proyectos en equipo.

**How I would apply this in real projects**:

Aplicaría estos conocimientos creando ramas para nuevas funcionalidades, trabajando sobre forks cuando no tenga permisos directos y utilizando pull requests para integrar cambios.
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [ 5 ] | He estado cómoda utilizando los comandos básicos de Git|
| Branching & merging | [4] | Antes había hecho uso de ramas pero la parte de local y remota me ha liado un poco |
| Remote operations | [ 4] | He podido solucionar un error con este tema de forma rápida y directa |
| Conflict resolution | [ 5 ] | No ha habido conflictos |
| History rewriting | [ 5] | No he tenido que modificar commits pero en caso de hacerlo, sabría |
| Git hooks | [ 5 ] | No ha sido necesario aplicarlo|
| Security practices | [ 5 ] | No ha sido necesario aplicarlo|

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/blancabgz/taller-master-ugr/tree/group-16-outcomes/newbie`
- Key commits demonstrating your work:
  - 4384c28: Archivo OUTCOMES rellenado

**Additional files created** (if any):
- hello.txt: [Archivo con mi nombre en el interior]
- my-info.txt: [Archivo con mi nombre, cual es mi lenguaje favorito y porqué estoy aprendiendo Git]

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [ x ] Completed the exercise for your chosen level (including all parts)
- [ x ] Documented all commands used with their outputs
- [ x ] Described challenges and how you resolved them
- [ x ] Provided a thoughtful reflection on your learning
- [ x ] Self-assessed your confidence in each topic
- [ x ] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

He puesto el grupo 16 porque soy online y no estoy en ningún grupo. 
No se si tenía que crear la pull request 

---

**Submission Date**: [2/1/2026]  
**Ready for Review**:  Yes
