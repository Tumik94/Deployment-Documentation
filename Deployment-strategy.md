##what is tags and how do the differ from branches?
    Git tags are a way to mark specific points in the reposiory's history, usually representing important milestones or release. They are way to creat a permanet reference to a specific commit.
    Inconstrast, branches in Git are a way to creat a separe line of development, allowing multiple features or bug fixes to be worked on simultaneously. Branches are more flexiable and can be merged backinto the main codebase, whereas tags are more static and represent a specific snapshot in time
#How can git tag help in managing and tracking deplyments?
    Git tags can be used to mark specific version or relese of the codebase that have been depolyed to differen environment (eg development, stating, production).
    By tagging the specific commit that was deployed, you can easily identify which version of the code is runnign in each enviromnent. This helps with tracking and troubleshooting issues, as you can quickly determine which version of the code is causing a problem.
    Git tags also allow you to roll back to a previous version of the code in necessary, as you can eaily identify the specific commit that was deployed
#How would you use git tags to ensure a stable and reliable deployment to client's production environment?
    when a new version of the code is ready for deployment to the production environmnet, you would creat a new git tag that represents that specific version
    before deploying production, you would thoroughly test the code in a staging enviroment, ensuring that it is function as expected. Once the code is vaildated, you can deploy the taffed version of the production envionment.
    by using a specific tag for the production depolyment, you can ensure that the same version of the code is deployed consistently, reducing the risk of unexpected issured or inconsistancies betweeen enviromnets.
    if a problem is discovered in production is discovered in production envionment, you can identify the specific tag that was deployed and roll back to a previous , know-good version if necessary.
#what steps should your team take to ensure that the client's prodction environment remain unaffected by ongoing development?
    maintain stric separation between the production enviornment and development/staging enviorments. The production enviroment should be treated as "sacred" environment, with limited access and well-defined deployment process.
    implement a robust tesing strategy, including unit test, integration tests, and end to end tests, to esure that all change are thoroughly validated before they are deployed to production
    use feaure flags ot toggle swithces to safely enable or disable new feauresin the production environment.This allow you to gradually rollout change and roll them back if issues rises.
    Establish a cleal communicaiton plan and ensure that the client's production enviromnet is regularly backed up, and have a well-document disaster recoverly plan in plce in case of unexpected issues
    monitor the production enviromnet closely, using logging, monitoring.
    ###    Depolyment strategy
     Branch  structure:
        main branch: primarly development branch
        Staging branch: pre-production testing and validation of new relese
        production branch: the codebase that is currently depoyed to client's production environment
    ##Deployment Workflow:
        development: developers work on new fearures and bug fixes own feaure branches
        tagging Releases: when a set of features or bug fixer is read for a new realease
        staging deployment: when then merge the tagged commit from the main branch into the stagingbranch
        production deployment: Once the release ha been validate in the staging environment, we merge the taffed commit form the staging branch into the production branch.
    ##Role of Git Tags:
        Traceability
        Consistency
        rollback capability
        collaboration and communication
 
    Example: a new feaure is developed and needs to be deployed to client's produciton environment
    1.Development team need implement a new feature branch and merges it into the main branch.
    2. creat a new Git tag, v1.30, to mark the release of this bersion of the codebase
    3.tagged commit from the main branch is merge into the staging branc, and the new release is        through  test in the staging environment.
    4.merges the v1.3.0 tagged commit form the staging branch into the production branch
    5.the client's production environment is then updated with v1.3.0 release.
has context menu


has context menu