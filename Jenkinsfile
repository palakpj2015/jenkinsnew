properties([
    parameters([
        [$class: 'ChoiceParameter',
         choiceType: 'PT_SINGLE_SELECT',
         description: 'Select an option',
         filterLength: 1,
         filterable: false,
         name: 'ActiveChoiceParameter',
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
                     return ['Option 1', 'Option 2', 'Option 3']
                 '''
             ]
         ],
         visibleItemCount: 5
        ]
    ])
])
