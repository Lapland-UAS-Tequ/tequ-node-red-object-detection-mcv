tequ-node-red-object-detection-mcv
=====================

Detect objects from image using Tensorflow.js model trained in Microsoft Azure Custom Vision service.

## Install

Run the following command in your Node-RED user directory - typically `~/.node-red`

        npm install tequ-node-red-object-detection-mcv

## Information

Run prediction on input image using Tensorflow.js model trained and exported from Microsoft Custom Vision.

Input image must be image buffer in **'msg.payload'**.

Outputs:
- Prediction result
- Manifest
- Metadata

Excepts following content in model folder:
- model.json (Tensorflow.js model)
- weights.bin (Tensorflow.js model)
- cvexport.manifest (Custom Vision manifest file)
- variables (folder that might include files for saved model)
- labels.txt (labels, one label on each row)
- metadata_properties.json (metadata of used model in JSON-format)

Supported image formats:
- JPG

Supports:
- TensorFlow.js object detection model exported from Microsoft Custom Vision (General compact S1 domain)

To train and export a model, please look:

https://www.customvision.ai/

Dependencies:
- https://www.npmjs.com/package/@microsoft/customvision-tfjs-node
- https://flows.nodered.org/node/node-red-contrib-image-info

