# ChohoCloud JavaScript Sample

Please note: This code is provided solely as a programming reference under Node.js. Do not include Chaohou Cloud Service API calls in browser frontend code unless your website can only be accessed from within the company. Otherwise, your API account information can be easily obtained by users for other purposes, and you will be charged for unauthorized usage.

**Polling should not be used in the production environment** to determine the completion of tasks as shown in the sample code. Instead, **callbacks should be used** to receive task completion information (i.e., configure the `notification` field in the task startup information).

To get started quickly or view more algorithm invocation examples, we suggest starting with our Python sample to understand HTTP request methods and request parameters: [https://gitee.com/chohotech/api_python_sample](https://gitee.com/chohotech/api_python_sample) (Github: [https://github.com/choho-tech/api_python_sample](https://github.com/choho-tech/api_python_sample))

## Usage Steps

Simply access `index_en.html` in your browser, fill in the corresponding information along with the semi-mandible 3D model to start the tooth segmentation task.

The `start_seg` function in `index_en.html` can also be used in Node.js.

After running, the webpage will generate segmented results `processed_mesh.stl` and `seg_labels.txt` and provide download links.

## Example

- This example demonstrates:
  1. How to create a new task JSON
  2. How to create a new task on the server
  3. How to query task status from the server and wait for task completion
  4. How to retrieve task results
  5. How to parse task results
- Please note that while we demonstrate how to perform a tooth segmentation task here, other tasks follow similar patterns, and users can easily adapt them with simple modifications.
- This example demonstrates how to segment an STL semi-mandible file and save the results as a blob.

## Code License

This repository is open source under the AGPL v3.0 license. If you use code from this repository in your project, you must provide the source code to users (including SaaS users). If you are a paying customer of Chohotech, this code is licensed to you according to our subscription agreement, and you are not obligated to comply with the AGPL v3.0 open-source license.
