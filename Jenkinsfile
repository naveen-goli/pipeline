pipeline {
    agent any
           stages {
                 stage('build') {
                              steps {
                                    echo "building"
                                    }
                               }
                 stage('test') {
                             steps {
                                    input ('Do you want to continue?')
                                    }
                               }
               stage('three') {
                   when {
                       not {
                              branch 'master'
                           }
                       }
                   steps {
                       echo "hello"
                        }
                 }
               stage('four') {
                   parallel {
                       stage('four-1') {
                           steps
                           {
                               echo "four-1"
                           }
                       }
                       stage('four-2') {
                           steps
                           {
                               echo "four-2"
                           }
                       }
                   }
                 }
       }
