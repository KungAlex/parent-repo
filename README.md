### parent-repo for testing git submodules workflow
 
to clone with all Submodules use

    git clone --recursive <repository>

#### Submodules workflow 

Add New Submodule to Parent

    TODO: create a new submodule-repo

    $ git submodule add <repository> <path>
    $ git submodule add https://github.com/KungAlex/submodul-exmaple.git 
    
    $ git status -s
    $ git commit -am "added submodule-example"
    
    now see (mode=160000)
    $ git ls-tree master -r
    $ git submodule status

Update submodule form origin remote repo

    TODO : make some changes in submodule-repo and commit them origin and than run
    $ git submodule update --remote
    $ git status -s
    $ git commit -am "update submodule-example"
    
Update submodule from parent-repo

    TODO: go to submodle dic and checkout a branch (only on first time)
    $ cd submodul-exmaple
    $ git checkout master
    
    TODO: now make some changes and add/commit them
    $ touch some-changes.txt
    $ git add .
    $ git commit -m "add some changes"
    
    TODO: go back to parent-repo an add/commit them
    $ cd parent-repo
    $ git status -s
    $ git add . 
    $ git commit -m "changes in submodule-example"
    
    $ git push --recurse-submodules=check
     --> see notice! TODO: cd in every sub-repo and to push or see other option
     --> make this default by run $ git config push.recurseSubmodules check
     
    $ git push --recurse-submodules=on-demand 
    
     
     

    
    

    
