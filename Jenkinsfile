node('master') {
  stage('Test 1') {
    echo 'Hello 1'
  }

  stage('Test 2'){
    echo 'Hello 2'
  }
  
  def parallelStages = [
    "Hello_3": { 
      node {
        echo "Hello 3"
      }
    },
    "Hello_4": { 
      node {
        echo "Hello 4"
      }
    },
    "Hello_5": { 
      node {
        echo "Hello 5"
      }
    }]

  stage('Parallel stages')
  { 
    parallel parallelStages
  }
  
}
