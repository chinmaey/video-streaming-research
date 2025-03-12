# Video Streaming Research

## 📌 Overview  
This repository compiles my research and publications related to video streaming optimization, adaptive bitrate (ABR) algorithms, and network performance. The work focuses on overcoming challenges in reducing data usage while enhancing user Quality of Experience (QoE) in video streaming services through innovative frameworks and cross-layer techniques.

*Note: This work is done in collaboration with AT&T. Due to AT&T restrictions, the code and demos for these projects are not publicly available.*

## 📄 Research Publications

### 1. DataPlanner: Data-Budget Driven Approach to Resource-Efficient ABR Streaming  
- **Publication:** [ACM MMSys 2021](https://dl.acm.org/doi/abs/10.1145/3458305.3459596)  
- **Focus:**  
  Over-the-top (OTT) video streaming consumes a significant portion of cellular data. Instead of only focusing on quality improvements, this work uses data budget information to manage data usage while maintaining QoE.  
  - A novel framework for quality-aware ABR streaming is proposed, involving a per-session data budget constraint based on user preference.
  - Two planning-based strategies are developed: one leveraging fine-grained perceptual quality information, and one without it.
  - Integrated with existing ABR algorithms in a simulated environment and in the popular open-source ABR player, ExoPlayer, on Android.
  - Evaluations show that when network bandwidth is high and data budgets are low, **traditional schemes use 90-93% more data than our methods—achieving comparable low-quality segment percentages and lower rebuffering**.

### 2. Cross-Layer Network Bandwidth Estimation for Low-Latency Live ABR Streaming  
- **Publication:** [ACM MMSys 2023](https://dl.acm.org/doi/abs/10.1145/3587819.3590990) (**DASH-IF Excellence in DASH Awards 2023, 2nd Place**)🏆 
- **Focus:**  
  Accurate bandwidth estimation is critical for low-latency live ABR streaming.  
  - Proposes a novel cross-layer approach combining coarse-grained application-level semantics with fine-grained kernel-level packet capture.
  - The technique leverages packet timing and size information captured at the kernel, leading to significantly more accurate bandwidth estimates.
  - In highly dynamic cellular environments, 74%-78% of the estimation errors fall within 10%—compared to only **10-17% for state-of-the-art** method.
  - Improved bandwidth estimation results in better prediction accuracy and significantly enhanced QoE for end users.

### 3. C2: Consumption Context Cognizant ABR Streaming for Improved QoE and Resource Usage Tradeoffs  
- 📄 **Patents:**
  - **Method and Apparatus for Adaptive Bit Streaming Using Consumption Context**  
    - **Patent Application:** US Patent App. 18/064,163  
    - **Description:** This patent outlines a method that leverages consumption context to optimize adaptive bitrate streaming, significantly reducing data usage while maintaining or enhancing Quality of Experience (QoE).
- **Publications:**  
  - [ACM MMSys 2022](https://dl.acm.org/doi/abs/10.1145/3524273.3528185) (**DASH-IF Excellence in DASH Awards 2022, 3rd Place**)🏆 
  - [ACM TOMM](https://dl.acm.org/doi/abs/10.1145/3652517)  
- **Focus:**  
  Different consumption contexts (C2) such as cellular or WiFi and various playback setups (direct on phone or via peripherals) significantly impact resource usage and QoE.  
  - This work argues that a user’s specific consumption context is crucial in ABR streaming.
  - Examined current practices in four popular ABR players, identifying limitations that negatively affect network resource usage and user experience.
  - Developed practical best-practice guidelines for C2-cognizant ABR streaming.
  - A proof-of-concept implementation in the ExoPlayer platform demonstrates **significantly improved tradeoffs between QoE and resource usage**.

### **Implementation details**  
- **Optimized Video Encoding Pipelines:** Using **H.264, H.265, AV1** codecs, **FFMpeg**, AWS Elemental MediaConvert.  
- **Cloud & Microservices:** **AWS ECS, EKS, EC2, S3**, Kubernetes, Docker for scalable deployments.  
- **Multi-Platform Support:** **dash.js, Shaka Player, ExoPlayer**, and MATLAB-based simulations.  
- **Network Optimization:** Cross-layer **bandwidth estimation, QoE monitoring**, CDN configuration.  
- **QoE Metrics & Evaluation:** **VMAF, AVQT, Pyshark, ScaPy, tc (traffic control)**.  

## 📊 Research Topics  
- Adaptive Bitrate Streaming (ABR) Optimization  
- Low-Latency DASH/HLS Streaming  
- Machine Learning for Video QoE Prediction  

## 🔗 Connect  
For more details on my research, please refer to my [Google Scholar profile](https://scholar.google.com/citations?user=TCaP5BQAAAAJ&hl) or visit my [https://sites.google.com/view/chinmaey-shende](#).

