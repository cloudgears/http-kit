## Rationale

This is a fork of [http-kit](https://github.com/http-kit/http-kit)
in order to make it more fitting for internal needs of CloudGears.

While working on it, try to keep it backward compatible as much as possible.
If backward compatibility is broken, specify it explicitly in this readme.


## Installing to local repository

Run following commands to generate `jar` and related `pom`: 
   
    lein jar; lein pom;
    
Declare local repository in `project.clj`: 

    :repositories [["localrepo" "file:resources/localrepo"]]    

(do not forget to create a folder in the project, i.e. `resources/localrepo`)

Copy files to required project, install with command: 

    lein deploy localrepo http-kit 2.3.0-alpha4-patch1 http-kit-2.3.0-alpha4-patch1.jar pom.xml
    
All set, http-kit should be installed in local repo.
 

## Version history

#### 2.3.0-alpha4-patch1 
Ability to drop connection after sending data via async http requests 
   
#### 2.3.0-alpha4 
Forked from http-kit
      