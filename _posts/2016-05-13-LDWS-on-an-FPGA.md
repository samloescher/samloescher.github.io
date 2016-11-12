---
layout: post
title:  Lane Departure Warning System on an FPGA
date:   2016-05-13
author: Sam Loescher
categories: academic
---

![Example](/images/ldws/example.jpg){: .center-image }

During my 3rd taught year at Bath, the second semester was dedicated to a group design and business project. In this we chose to make lane departure warning IP for a fictitious company, iM2g(our group was M2). The design was broken up roughly into sections as shown below. I worked closely with another member to improve contrast in the image and also a convolutional filter module to help with noise reduction.

![Flow](/images/ldws/flow.jpg){: .center-image }

The entire IP was targeting an FPGA, which have many benefits over microcontrollers and typically wins out in latency, speed, and power consumption. The only catch to this is the increased complexity in writing the code to define how to lay out the FPGA. We chose Verilog as this seems to be well adopted by industry, however it will depend on who you ask as many people would argue VHDL is the language of choice.

The input of the submodule I was designing, would be a grayscale image which I would ideally increase the contrast so much so that only the road markings remained. We created a myriad of different solutions however found an histogram adjustment module to be the best quality filter in both robustness(different lighting conditions) and contrast enhancement(removing clutter).

![Flow](/images/ldws/histogram_adjustment.jpg){: .center-image }

We later included a inverse perspective warping filter into the pipeline and achieved much better results

![Flow](/images/ldws/ideal_out.jpg){: .center-image }

The image was then passed to a neural network implemented by other members in the group for classification. The result would then be fed back to the user in the form of an audiovisual alert to the driver if the car was drifting between lanes.

___

Code : Available on request