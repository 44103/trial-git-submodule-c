# Submodule Side C

## Working Sequence
1. init repositories
   - in A repository
      1. git init
      1. git add
      1. git commit
   - in B repository
      1. git init
      1. git add
      1. git commit
1. init submodules
   - in A repository
      1. git submodule add B
      1. git submodule init
      1. git add B .gitmodules
      1. git commit
   - in B repository
      1. git submodule add A
      1. git submodule init
      1. git add A .gitmodules
      1. git commit
1. add submodules
   - in A repository
      1. cd B
      1. git pull
      1. cd ..
      1. git add A
      1. git commit
   - in B repository
      1. cd A
      1. git pull
      1. cd ..
      1. git add B
      1. git commit
1. create third repository
   - in C repository
      1. git init
      1. git submodule add A
      1. git submodule add B
      1. git submodule update --init
