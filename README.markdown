Grails, mongoDB and Spring Security Core
========================

This project shows the Spring security core plugin and mongodb plugin integration.


After create the app and install the plugins.

You have to :

 - modify User domain class

    - add static transients = ['authorities']

After create the app and install the plugins. You have to modify User domain class

- add static transients = ['authorities']


- Extend GrailsUserDetailsService (see com.example.secure.MongoUserDetailsService)

- modify UserRole mapping comment id key (composite key are not supported)
    //		id composite: ['role', 'user']

- update the resources.groovy file

    beans = {
    	userDetailsService(com.example.secure.MongoUserDetailsService)
    }


