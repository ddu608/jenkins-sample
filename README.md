# Jenkins intro
1. What's jenkins
    - automation server
    - history
    - pros
      + No.1 CI/CD tool
      + flexbility and extensibility, have a vast ecosystem of plugins, 1000+
      + open source and free
      + scalablity and distributed builds
      + Strong integration Capabilities
      + workflow as code (2016)
    - cons
      + hard to debug
      + hard to implement pipeline if the logics is too complicate
      + not so stable, always small bugs
      + backward compatibility 
2. Jenkins usage
    - Installation
        service
        docker
        war
    - parameterized
    - cron schedule
    - SCM - git
    - workflow as code
        - groovy pipelines
        - pipeline-syntax
    - notificaiton
    - API integrations
    - Call another build
    - 1000+ plugins to do most of everythings
        - plugin management
    - integration with clouds
3. How to design/implement a workflow
    - trigger
        - type
            - UI
            - API
            - On schedule
            - By conditions ( e.g. code change, traffic increasing )
        - params definitions 
    - breakdown the workflow
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
    - Error handling and retry,  
        + idempotent action
    - Notification 
        + feedback 
        + alert
    - Parallelize builds
    - Distributed builds 
        + leverage the clouds
    - Auto-scale and Cost saving
    - Security
        + store credentical 
        + remove cleartext passwords
