Tensorflow 1.8 
- git clone https://github.com/tensorflow/tensorflow
- cd tensorflow
- git checkout v1.8.0

C++ GPU setup
  ```
  auto options = tensorflow::SessionOptions();
  options.config.mutable_gpu_options()->set_visible_device_list("0");
  // session_ is a unique_ptr to a tensorflow::Session
  session_->reset(tensorflow::NewSession(options));
  ```
