# watsonx.ai based query Node for Node-RED


## Overview

Query-able node based on watsonx.ai


## Pre-requisite

You need to get account in [IBM Cloud](https://cloud.ibm.com/) first.

You also have to prepare **IAM API Key** of your IBM Cloud account. You also need **Project ID** for your project of IBM Watson Studio and IBM Watson Machine Learning, lite(free) plan would be OK.

At last, you would prepare [Node-RED](https://nodered.org/).


## How to use

1. In Node-RED, you can search [node-red-contrib-dotnsf-watsonxai](https://www.npmjs.com/package/node-red-contrib-dotnsf-watsonxai) node. You need to install this node in your Node-RED.

2. You will see **watsonx.ai** node under `function` category. Drag & Drop this node into Node-RED's canvas.

3. Open properties box. You need to edit **API Key** field with your API Key.

4. You need to input one of followings:

  - If you would use existed(non-tuned) LLM, you need to input ..

    - Project ID: ID specified for Project
    - Model ID: ID specified for LLM

    - You don't need to input Deployment ID

  - If you would use tuned LLM(like this one), you need to input ..

    - Deployment ID: ID specified tuned LLM

    - You don't need to input Proejct ID nor Model ID

5. Connect nodes. You have to input query text as **msg.payload** into watsonx.ai node. Then watsonx.ai node would output generated text in its **msg.payload**.


## Licensing

This code is licensed under MIT.


## Copyright

2023-2024 K.Kimura @ Juge.Me all rights reserved.

