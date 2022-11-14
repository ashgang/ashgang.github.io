---
layout: page
title: WiPeR
description: Wireless, Pervasive & Reliable Monitoring of Industrial Internet of Things Systems
img: assets/img/wipernode.jpg
importance: 1
category: work
---

The WiPeR project intents to develop an innovative solution for condition-based monitoring that eliminates sensor power and network cables without compromising data quality or reliability.

## Challenges
WiPeR is a combination of hybrid platform that is derived from the design of <a href="https://dl.acm.org/doi/10.1145/3410992.3411028">HyPer</a>. Such a hybrid design and the associated software stack delivers a deterministic sensor lifetime. However, monitoring and transmitting raw data of the observed phenomena (in this case vibration) will drastically increase the latency of fault identification. Below is the P-F curve that show vibration monitoring as one of the preventive maintenance approach that demands data is continuously available, which is infeasible under the lifetime constraints of the device. To tackle this challenge, we re-evaluate the classic algorithms that are applied to identify faults in rotating machines. We essentially ask the research question: "Can front-end processing in combination with on-node analysis of vibration signals achieve preventive maintenance targets without compromising node lifetime?".

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/PFcurve.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    P-F Curve.*
</div>

## Near-sensor Processing
The traditional approach to vibration monitoring of faults such as bearing is by using an approach called envelope analysis. The vibration monitoring signal is a cyclo-stationary signal, which means it is essentially a non-stationary signal with properties of stationary signal embedded within. The envelope analysis algorithm applies a pipeline of filters, singal processing and domain transform to extract the embedded stationary signal. The primary challenge in doing envelope analysis on the low power MCU is memory constraints. However, combining the computational capabilities of the embedded sensor along with the low power MCU, the envelope analysis pipeline can be fulfilled (of course with some tradeoffs). And we show in <a href="https://ieeexplore.ieee.org/document/9600072">ReFrAEN</a> that such an approach can achieve low latency fault diagnosis within stage-3 of the PFcurve that provides 3 - 6 weeks of lead time to schedule maintenance. The software block diagram of HyPer and ReFrAEN is shown below.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/hyper.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
	
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/refraen.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    HyPer and ReFrAEN software block diagram.
</div>

Revisiting our research question, by combining the hybrid energy harvesting approach along with intelligent processing on-node we can achieve low latency fault identification.

## Publications
- Thangarajan, A.S., Yang, F., Joosen, W. and Hughes, D., 2020, October. Deterministic 40 year battery lifetime through a hybrid perpetual sensing platform (HyPer). In Proceedings of the 10th International Conference on the Internet of Things (pp. 1-8).
- Thangarajan, A.S., Yang, F., Joosen, W., Michiels, S. and Hughes, D., 2021, July. ReFrAEN: a Reconfigurable Vibration Analysis Framework for Constrained Sensor Nodes. In 2021 17th International Conference on Distributed Computing in Sensor Systems (DCOSS) (pp. 124-131). IEEE.



**Ref: Image is taken from <a href="https://www.isa.org/intech-home/2019/march-april/features/improving-maintenance-by-adopting-a-p-f-curve-meth">Improving maintenance by adopting a P-F curve methodology</a>*
