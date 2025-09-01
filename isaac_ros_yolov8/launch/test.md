#with engine update

ros2 launch isaac_ros_yolov8 my_yolov8.launch.py   model_file_path:=${ISAAC_ROS_WS}/isaac_ros_assets/models/yolov8/td06_a.onnx   engine_file_path:=${ISAAC_ROS_WS}/isaac_ros_assets/models/yolov8/td06_a.plan   network_image_width:=640 network_image_height:=640   input_tensor_names:="['input_tensor']"   input_binding_names:="['images']"   output_tensor_names:="['output_tensor']"   output_binding_names:="['output0']"   num_classes:=1   force_engine_update:=True   verbose:=True  yolov8_decoder_node.confidence_threshold:=0.7

#threshold, no engine update

admin@tndlux-G16:/workspaces/isaac_ros-dev$ ros2 launch isaac_ros_yolov8 my_yolov8.launch.py model_file_path:=${ISAAC_ROS_WS}/isaac_ros_assets/models/yolov8/td06_a.onnx engine_file_path:=${ISAAC_ROS_WS}/isaac_ros_assets/models/yolov8/td06_a.plan network_image_width:=640 network_image_height:=640 input_tensor_names:="['input_tensor']" input_binding_names:="['images']" output_tensor_names:="['output_tensor']" output_binding_names:="['output0']" num_classes:=1 verbose:=True confidence_threshold:=0.7 nms_threshold:=0.5