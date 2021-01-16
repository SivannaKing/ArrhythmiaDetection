# ArrhythmiaDetection
arrhymia detection with tensorflow base on MIT BIH dataset and quantize model with Qkeras or tensorflow lite

file structure:
ECG2(base path) -> Train
                -> TFLite Quantization
                -> Qkeras Quantization
                -> model
                -> MLII
                -> layer_wise_quantization
 
Train:
train FP32 model and save model(.hdf5) in Train/saved
env: TF23
     tensorflow 2.3.0
      
TFLite Quantization:
quantize FP32 model to INT8 model with tensorflow lite
find best model in Train/saved and copy to model
save quantization model(.tflite) in model
env: TFLite
     tf-nightly-cpu 2.3.0
     tensorflow-model-optimization 0.5.0
     
Qkeras Quantization:
quantize FP32 model to low bit quantization model with Qkeras
save quantization model(.h5) and quantization log in model
env: Qkeras
     tensorflow 2.3.0
     Qkeraas 0.8.0
install Qkeras: https://github.com/google/qkeras 
NOTE Qkeras requirements!
