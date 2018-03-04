#!/usr/bin/env groovy
pipeline {
    agent {
        label 'android'
    }
    stages {
        stage('Clean') {
            when {
                anyOf { branch 'master'; branch 'release-*'; branch 'hotfix-*' }
            }
            steps {
                sh './gradlew clean'
            }
        }
        stage('Assemble') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Unit Test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('UI Test') {
            steps {
                sh './gradlew connectedAndroidTest'
            }
        }
        stage('Check') {
            steps {
                sh './gradlew check'
            }
        }
        stage('Archive') {
            when {
                anyOf { branch 'master'; branch 'release-*'; branch 'hotfix-*' }
            }
            steps {
                archiveArtifacts artifacts: 'app/build/outputs/apk/**/*.apk',
                        excludes: '**/*unsigned*.apk,**/*-androidTest.apk',
                        fingerprint: true
            }
        }
    }
}
