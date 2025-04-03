# Movement: Support For Kalman Filters (Deepak Goel)

## Personal Details
- **Full Name:** Deepak Goel  
- **Email:** [deepak.goel.pro@gmail.com](mailto:deepak.goel.pro@gmail.com)  
- **GitHub Username:** [deepakpro190](https://github.com/deepakpro190)  
- **Zulip Username:** Deepak Goel  
- **Location & Time-zone:** Delhi, India (IST, UTC+5:30)  
- **Personal Website / Project Portfolio:** deepakpro190  
- **Proposal Discussion Link:** [GitHub PR](https://github.com/neuroinformatics-unit/gsoc/pull/47/files)  

---

## Project Proposal

### **Synopsis**
This project aims to enhance the Movement library by integrating an optimized multi-object tracking system that ensures accurate position, velocity, and acceleration smoothing while effectively handling identity switches in Multi-Animal Tracking.

At its core, the system will utilize an advanced **Kalman Filter framework**, rigorously benchmarked to select the most efficient configuration for the Movement dataset. The implementation will incorporate state-of-the-art identity association techniques, including:

- **Mahalanobis Distance & Hungarian Algorithm** for optimal detection-to-track assignment, minimizing incorrect identity associations.
- **Joint Probabilistic Data Association (JPDA)** to enhance stability in complex scenarios, where multiple animals interact or occlusions occur.
- **Re-Identification (Re-ID) with Deep Learning** to extract deep feature embeddings from animal appearances, ensuring long-term identity tracking.

To further improve decision-making, the tracking pipeline will compute a **dynamic confidence score** for each frame, integrating:
- **Motion Consistency Score**, derived from Kalman Filter-based trajectory predictions.
- **Appearance Similarity Score**, leveraging deep CNN feature embeddings for Re-ID.
- **Final Fusion Score**, a weighted combination of motion and appearance cues for robust identity resolution.

By the project's completion, the **Movement library** will feature a highly accurate, AI-powered multi-animal tracking pipeline capable of handling occlusions, identity switches, and non-linear motion.

---

## **Implementation Timeline**

### **Deliverables**
-  **Integration of a Kalman Filter** for position, velocity, and acceleration smoothing.
-  **Identity switch correction** using Mahalanobis Distance & Hungarian Algorithm.
-  **Joint Probabilistic Data Association (JPDA)** for complex tracking scenarios.
-  **Re-Identification (Re-ID) Module** with deep learning-based feature extraction.
-  **Benchmarking & testing** of tracking algorithms on real & synthetic datasets.
-  **Comprehensive documentation** with integration guides & example use cases.
-  **Unit tests** to ensure correctness and stability.

### **Stretch Goals**
-  Extending the Kalman Filter to support **automatic parameter tuning** (e.g., Expectation-Maximization or Adaptive Noise Expectation).
-  Implementing **additional identity correction heuristics**, if needed.

---

##  **Weeks & Phase Distribution (12 Weeks)**

### **Pre-GSoC Phase 1 (March 24 – April 8)**
- Submit final GSoC proposal.
- Explore Movement codebase & documentation.
- Fix minor bugs & implement test cases.

### **Pre-GSoC Phase 2 (April 9 – May 8)**
- Compare **Kalman Filter** (KF) implementations: PyKalman, NFoursid, Dynamax, MovingPandas.
- Implement & evaluate basic KF on synthetic noisy data.
- Select the best approach based on experiments.

### **Community Bonding Period (May 8 – June 1)**
- Finalize KF approach with mentors.
- Research identity switch correction techniques.
- Plan integration of confidence scores for re-identification.

---

## 🔹 **Coding Phase 1: Kalman Filtering for Multi-Entity Motion Tracking**

### **Week 1 (June 2 – June 8)**
- Implement **basic Kalman Filter** for position smoothing.
- Generate synthetic position data & evaluate filtering accuracy.

### **Week 2 (June 9 – June 15)**
- Extend KF to smooth **velocity & acceleration data**.
- Validate on **Movement datasets** & optimize performance.

### **Week 3 (June 16 – June 22)**
- Implement **Expectation-Maximization (EM)** for parameter tuning.
- Conduct thorough review & integrate mentor feedback.
- Develop **unit tests** for Kalman Filter smoothing.

### **Week 4 (June 23 – June 29)**
- Write detailed **documentation & docstrings** for the KF module.
- Create **example use cases** for Movement’s gallery.

### **Week 5 (June 30 – July 6)**
- Final optimizations to Kalman Filter implementation.
- Prepare for **mid-term evaluations** & submit reports.

---

## 🔹 **Coding Phase 2: Identity Association & Re-Identification**

### **Week 6 (July 7 – July 13) — Mid-Term Evaluation**
- Submit mid-term evaluation.
- Conduct final testing & performance evaluation for Kalman Filter.

### **Week 7 (July 14 – July 20)**
- Research & experiment with **Hungarian Algorithm & Mahalanobis Distance**.
- Gather relevant datasets & discuss **Re-ID** approach.

### **Week 8 (July 21 – July 27)**
- Implement **identity switch correction** using Hungarian Algorithm & Mahalanobis Distance.
- Validate with test cases & refine.

### **Week 9 (July 28 – August 3)**
- Improve identity tracking for **occlusions & path crossings**.
- Introduce **confidence scores** for re-identification.

### **Week 10 (August 4 – August 10)**
- Develop **unit tests** for identity switch correction.
- Integrate correction module into Movement’s **tracking pipeline**.

---

## 🔹 **Final Weeks**
### **Week 11 (August 11 – August 17)**
- Implement **JPDA** for complex tracking cases.
- Create **detailed use case examples**.
- Write **documentation & integration guide**.

### **Final Week (August 18 – September 1)**
- Codebase freeze & **final performance evaluation**.
- Conduct extensive **testing & mentor reviews**.
- Submit **final GSoC report**.

---

## **Communication Plan with Mentors**
- **Weekly Meetings**: Sync-up meetings for progress discussions.
- **GitHub Discussions**: Use issues & PRs for code reviews.
- **Google Docs**: Collaborative documentation & mentor feedback.
