### parent-repo for testing git submodules workflow
 
to clone with all Submodules use

    git clone --recursive <repository>

#### Submoduls workflow 

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

    TODO: make some changes in submodule-repo and commit them origin  
    $ git submodule update --remote
    $ git commit -am "update submodule-example"

    
