node {
    properties([
        parameters([
            choice(
                choices: ['USA', 'Canada', 'UK'],
                description: 'Select a country',
                name: 'Country'
            ),
            [$class: 'ChoiceParameter',
             choiceType: 'PT_SINGLE_SELECT',
             description: 'Select a city',
             filterable: false,
             name: 'City',
             script: [
                 $class: 'GroovyScript',
                 fallbackScript: [
                     classpath: [],
                     sandbox: false,
                     script: 'return ["Error: Script not executed"]'
                 ],
                 script: [
                     classpath: [],
                     sandbox: false,
                     script: '''
                        def country = Country
                        def cities = []

                        if (country == 'USA') {
                            cities = ['New York', 'Los Angeles', 'Chicago']
                        } else if (country == 'Canada') {
                            cities = ['Toronto', 'Montreal', 'Vancouver']
                        } else if (country == 'UK') {
                            cities = ['London', 'Manchester', 'Birmingham']
                        }

                        return cities
                     '''
                 ]
             ]
            ]
        ])
    ])
    
    // Your pipeline steps go here
}
