#!groovy

stage 'setJava'
node {

    // env.JAVA_HOME = "C:\\Program Files\\Java\\jdk1.8.0_66"
     env.JAVA_HOME = "C:\\Program Files (x86)\\Java\\jdk1.8.0_11"
     echo env.JAVA_HOME

}
stage 'Checkout'
node {
git 'https://github.com/exorcist007/JenkinsWorkflowBuild.git'
//stage 'clean'
//bat 'gradle clean --info'
stage 'build'
bat 'gradle build --info'
//stage 'jar'
//bat 'gradle jar --info'
}
stage 'Checkout'
node {
git 'https://github.com/exorcist007/TDF-IDF-CascadingDateFormatConversion.git'
//stage 'clean'
//bat 'gradle clean --info'
stage 'build'
bat 'gradle build --info'
//stage 'jar'
//bat 'gradle jar --info'
}
//stage 'customTask'
//node{
  //  sleep time: 15000, unit: 'NANOSECONDS'
//this is a custom task that gets called irrespective of the repositories being called
//bat 'gradle sayHello'
//}
//stage 'jar'
//node{
//extra batch command called: may be ignored
//bat 'gradle clean jar --info'
//}
stage name: 'Production', concurrency: 1
node {
 echo 'Production server looks to be alive'
 echo "Deployed to production"
}