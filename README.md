## Jenkins intro
1. What's jenkins
    - pros
      + No.1 CI/CD tool
      + flexbility and extensibility, have a 1000 ecosystem of plugins
      + open source and free
      + scalablity and distributed builds
      + Strong integration Capabilities
    - cons
      + hard to debug
      + hard to implement complicate logics
      + not so stable, always small bugs
2. Jenkins usage
    - Installation
    - SCM - git
    - parameterized
    - notificaiton
    - API integrations
    - Call another build
    - workflow as code
        - groovy pipelines
    - 1000+ plugins to do most of everythings
3. How to design a workflow
    - trigger
        - type
            - UI
            - API
            - On schedule
            - By conditions ( e.g. code change, traffic increasing )
        - params definitions 
    - worker
        - checkout
        - compile
        - testing
        - package
        - deployment

    - post action
        - notification (good or ng )
        - call downstream build
4. Best practices of pipelines
    - Logging
    - Comments
    - Modularizing
    - Error handling and retry
    - Notification and alert
    - Parallelize builds
    - Cost saving
    - Security
