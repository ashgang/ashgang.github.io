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
WiPeR is a combination of hybrid platform that is derived from the design of <a href="https://dl.acm.org/doi/10.1145/3410992.3411028">HyPer</a>. Such a hybrid design and the associated software stack delivers a deterministic sensor lifetime. However, monitoring and transmitting raw data of the observed phenomena (in this case vibration) will drastically increase the latency of fault identification. Below is the P-F curve that show vibration monitoring as one of the preventive maintenance approach that demands data is continuously available, which is infeasible under the lifetime constraints of the device. To tackle this challenge, we re-evaluate the classic algorithms that are applied to identify faults in rotating machines.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/PFcurve.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    P-F Curve.*
</div>

## Near-sensor Processing

**Ref: Image is taken from <a href="https://www.isa.org/intech-home/2019/march-april/features/improving-maintenance-by-adopting-a-p-f-curve-meth">Improving maintenance by adopting a P-F curve methodology</a>*
