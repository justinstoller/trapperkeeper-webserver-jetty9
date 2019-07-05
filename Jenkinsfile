stage("Build") {
  node("worker") {
    sh "echo success"
  }
}

//
// https://jenkins.io/doc/pipeline/examples/#parallel-from-list
//
// jdks = ["openjdk8" "openjdk11"]
// cells = [:]
//
// def script = """
// source ~/jdk_switcher.sh
// jdk_switcher use ${jdk}
// lein with-profile +ci -U test :all
// """
//

stage("Test") {
  node("worker") {
    sh '''
      # source ~/jdk_switcher.sh
      # jdk_switcher use openjdk8
      lein with-profile +ci -U test :all
    '''
  }
}

stage("Deploy") {
  node("worker") {
    sh "echo success"
  }
}
