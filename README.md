# Math-Test
    name: Get User Name

    on:
      workflow_dispatch:
        inputs:
          user_name:
            description: 'Please enter your name'
            required: true
            type: string

    jobs:
      greet:
        runs-on: ubuntu-latest
        steps:
          - name: Greet User
            run: echo "Hello, ${{ github.event.inputs.user_name }}!"
