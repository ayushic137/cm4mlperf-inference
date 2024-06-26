# Image Classification using ResNet50 

## Dataset

The benchmark implementation run command will automatically download the validation and calibration datasets and do the necessary preprocessing. In case you want to download only the datasets, you can use the below commands.

=== "Validation"
    ResNet50 validation run uses the Imagenet 2012 validation dataset consisting of 50,000 images.

    ### Get Validation Dataset
    ```
    cm run script --tags=get,dataset,imagenet,validation -j
    ```
=== "Calibration"
    ResNet50 calibration dataset consist of 500 images selected from the Imagenet 2012 validation dataset. There are 2 alternative options for the calibration dataset.

    ### Get Calibration Dataset Using Option 1
    ```
    cm run script --tags=get,dataset,imagenet,calibration,_mlperf.option1 -j
    ```
    ### Get Calibration Dataset Using Option 2
    ```
    cm run script --tags=get,dataset,imagenet,calibration,_mlperf.option2 -j
    ```

## Model
The benchmark implementation run command will automatically download the required model and do the necessary conversions. In case you want to download only the official model, you can use the below commands.
Get Official MLPerf ResNet50 Model
=== "Tensorflow"
    ### Tensorflow
    ```
    cm run script --tags=get,ml-model,resnet50,_tensorflow -j
    ```
=== "Onnx"
    ### Onnx
    ```
    cm run script --tags=get,ml-model,resnet50,_onnx -j
    ```

## Benchmark Implementations
=== "MLCommons-Python"
    ### MLPerf Reference Implementation in Python

    === "edge"
        #### Edge category
        In the edge category, ResNet50 has Offline, SingleStream, and MultiStream scenarios and all the scenarios are mandatory for a closed division submission.

        === "Onnxruntime"
            ##### Onnxruntime
            === "CPU"

                ###### CPU
                === "Offline"
                    ####### Offline scenario
                    Performance Estimation Command

                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "Offline", "cpu", "test", "500") }}
                    ```
                    Actual Run Command
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "Offline", "cpu", "valid") }}
                    ```
                === "SingleStream"
                    ####### SingleStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "SingleStream", "cpu", "valid" ) }}
                    ```

                === "MultiStream"
                    ####### MultiStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "MultiStream", "cpu", "valid") }}
                    ```
                === "All Scenarios"
                    ####### All scenarios
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "All Scenarios", "cpu", "valid") }}
                    ```

            === "CUDA"
                ###### Nvidia GPU
                === "Offline"
                    ####### Offline scenario
                    Performance Estimation Command

                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "Offline", "cuda", "test", "200000") }}
                    ```
                    Actual Run Command
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "Offline", "cuda", "valid") }}
                    ```
                === "SingleStream"
                    ####### SingleStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "SingleStream", "cuda", "valid" ) }}
                    ```

                === "MultiStream"
                    ####### MultiStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "MultiStream", "cuda", "valid") }}
                    ```
                === "All Scenarios"
                    ####### All scenarios
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "All Scenarios", "cuda", "valid") }}
                    ```

            === "ROCm"
                ###### AMD GPU
                === "Offline"
                    ####### Offline scenario
                    Performance Estimation Command

                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "Offline", "rocm", "test", "50000") }}
                    ```
                    Actual Run Command
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "Offline", "rocm", "valid") }}
                    ```
                === "SingleStream"
                    ####### SingleStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "SingleStream", "rocm", "valid" ) }}
                    ```

                === "MultiStream"
                    ####### MultiStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "MultiStream", "rocm", "valid") }}
                    ```
                === "All Scenarios"
                    ###### All scenarios
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "onnxruntime", "edge", "All Scenarios", "rocm", "valid") }}
                    ```

        === "Tensorflow"
            ##### Tensorflow
            === "CPU"

                ###### CPU
                === "Offline"
                    ####### Offline scenario
                    Performance Estimation Command

                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "Offline", "cpu", "test", "500") }}
                    ```
                    Actual Run Command
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "Offline", "cpu", "valid") }}
                    ```
                === "SingleStream"
                    ####### SingleStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "SingleStream", "cpu", "valid" ) }}
                    ```

                === "MultiStream"
                    ####### MultiStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "MultiStream", "cpu", "valid") }}
                    ```
                === "All Scenarios"
                    ####### All scenarios
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "All Scenarios", "cpu", "valid") }}
                    ```

            === "CUDA"
                ###### Nvidia GPU
                === "Offline"
                    ####### Offline scenario
                    Performance Estimation Command

                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "Offline", "cuda", "test", "200000") }}
                    ```
                    Actual Run Command
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "Offline", "cuda", "valid") }}
                    ```
                === "SingleStream"
                    ####### SingleStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "SingleStream", "cuda", "valid" ) }}
                    ```

                === "MultiStream"
                    ####### MultiStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "MultiStream", "cuda", "valid") }}
                    ```
                === "All Scenarios"
                    ####### All scenarios
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "All Scenarios", "cuda", "valid") }}
            === "ROCm"
                ###### AMD GPU
                === "Offline"
                    ####### Offline scenario
                    Performance Estimation Command

                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "Offline", "rocm", "test", "50000") }}
                    ```
                    Actual Run Command
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "Offline", "rocm", "valid") }}
                    ```
                === "SingleStream"
                    ####### SingleStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "SingleStream", "rocm", "valid" ) }}
                    ```

                === "MultiStream"
                    ####### MultiStream scenario
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "MultiStream", "rocm", "valid") }}
                    ```
                === "All Scenarios"
                    ###### All scenarios
                    Run Command
            
                    ```bash
                    {{ mlperf_inference_run_command(20, "resnet50", "reference", "tensorflow", "edge", "All Scenarios", "rocm", "valid") }}
                    ```



    === "datacenter" 
        #### Datacenter category 
        In the datacenter category, ResNet50 has Offline and Server scenarios and all the scenarios are mandatory for a closed division submission.
        
        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            {{ mlperf_inference_run_command(12, "resnet50", "reference", "tensorflow", "datacenter", "Offline") }}
            ```

        === "Server"
            ##### Server scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=reference \
               --category=datacenter \
               --scenario=Server
            ```
        === "All scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=reference \
               --category=datacenter
            ```

=== "Nvidia"
    ### Nvidia MLPerf Inference Implementation

    === "edge"
        #### Edge category
        In the edge category, ResNet50 has Offline, SingleStream, and MultiStream scenarios and all the scenarios are mandatory for a closed division submission.

        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=nvidia \
               --category=edge \
               --scenario=Offline
            ```

        === "SingleStream"
            ##### SingleStream scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=nvidia \
               --category=edge \
               --scenario=SingleStream
            ```

        === "MultiStream"
            ##### MultiStream scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=nvidia \
               --category=edge \
               --scenario=MultiStream
            ```
        === "All Scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=nvidia \
               --category=edge
            ```

    === "datacenter" 
        #### Datacenter category 
        In the datacenter category, ResNet50 has Offline and Server scenarios and all the scenarios are mandatory for a closed division submission.
        
        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=nvidia \
               --category=datacenter \
               --scenario=Offline
            ```

        === "Server"
            ##### Server scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=nvidia \
               --category=datacenter \
               --scenario=Server
            ```
        === "All scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=nvidia \
               --category=datacenter
            ```

=== "Intel"
    ### Intel MLPerf Inference Implementation

    === "edge"
        #### Edge category
        In the edge category, ResNet50 has Offline, SingleStream, and MultiStream scenarios and all the scenarios are mandatory for a closed division submission.

        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=intel \
               --category=edge \
               --scenario=Offline
            ```

        === "SingleStream"
            ##### SingleStream scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=intel \
               --category=edge \
               --scenario=SingleStream
            ```

        === "MultiStream"
            ##### MultiStream scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=intel \
               --category=edge \
               --scenario=MultiStream
            ```
        === "All Scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=intel \
               --category=edge
            ```

    === "datacenter" 
        #### Datacenter category 
        In the datacenter category, ResNet50 has Offline and Server scenarios and all the scenarios are mandatory for a closed division submission.
        
        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=intel \
               --category=datacenter \
               --scenario=Offline
            ```

        === "Server"
            ##### Server scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=intel \
               --category=datacenter \
               --scenario=Server
            ```
        === "All scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=intel \
               --category=datacenter
            ```

=== "Qualcomm"
    ### Qualcomm MLPerf Inference Implementation

    === "edge"
        #### Edge category
        In the edge category, ResNet50 has Offline, SingleStream, and MultiStream scenarios and all the scenarios are mandatory for a closed division submission.

        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=edge \
               --scenario=Offline
            ```

        === "SingleStream"
            ##### SingleStream scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=edge \
               --scenario=SingleStream
            ```

        === "MultiStream"
            ##### MultiStream scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=edge \
               --scenario=MultiStream
            ```
        === "All Scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=edge
            ```

    === "datacenter" 
        #### Datacenter category 
        In the datacenter category, ResNet50 has Offline and Server scenarios and all the scenarios are mandatory for a closed division submission.
        
        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=datacenter \
               --scenario=Offline
            ```

        === "Server"
            ##### Server scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=datacenter \
               --scenario=Server
            ```
        === "All scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=qualcomm \
               --category=datacenter
            ```

=== "MLCommons-C++"
    ### MLPerf Modular Implementation in C++

    === "edge"
        #### Edge category
        In the edge category, ResNet50 has Offline, SingleStream, and MultiStream scenarios and all the scenarios are mandatory for a closed division submission.

        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            {{ mlperf_inference_run_command(12, "resnet50", "cpp", "onnxruntime", "edge", "Offline") }}
            ```

        === "SingleStream"
            ##### SingleStream scenario
            Run Command
            
            ```bash
            {{ mlperf_inference_run_command(12, "resnet50", "cpp", "onnxruntime", "edge", "SingleStream") }}
            ```

        === "MultiStream"
            ##### MultiStream scenario
            Run Command
            
            ```bash
            {{ mlperf_inference_run_command(12, "resnet50", "cpp", "onnxruntime", "edge", "MultiStream") }}
            ```
        === "All Scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            {{ mlperf_inference_run_command(12, "resnet50", "cpp", "onnxruntime", "edge", "All Scenarios") }}
            ```

    === "datacenter" 
        #### Datacenter category 
        In the datacenter category, ResNet50 has Offline and Server scenarios and all the scenarios are mandatory for a closed division submission.
        
        === "Offline"
            ##### Offline scenario
            Run Command

            ```bash
            {{ mlperf_inference_run_command(12, "resnet50", "cpp", "onnxruntime", "datacenter", "Offline") }}
            ```

        === "Server"
            ##### Server scenario
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference \
               --model=resnet50 \
               --implementation=reference \
               --category=datacenter \
               --scenario=Server
            ```
        === "All scenarios"
            ##### All scenarios
            Run Command
            
            ```bash
            cm run script --tags=run-mlperf,inference,_all-scenarios \
               --model=resnet50 \
               --implementation=reference \
               --category=datacenter
            ```

