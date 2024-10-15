# **Git Commit List `Darft`:**

**Step 1: Data Collection and Preparation**

- `01. data_collection: collected raw video footage`
- `01. data_preparation: extracted frames from video`
- `01. data_preparation: annotated frames for YOLO`
- `01. data_preparation: saved annotations in YOLO format`

**Step 2: Training the YOLO Model**

- `02. yolo_configuration: configured YOLO for custom parking lot dataset`
- `02. yolo_training: split dataset into training, validation, and test sets`
- `02. yolo_training: trained YOLO model on custom dataset`
- `02. yolo_evaluation: saved YOLO model weights`
- `02. yolo_evaluation: evaluated YOLO model on test set`
- `02. yolo_evaluation: fine-tuned YOLO model based on evaluation`

**Step 3: Vehicle Detection and Parking Zone Setup**

- `03. detection_setup: loaded trained YOLO model for vehicle detection`
- `03. detection_setup: applied YOLO model to video`
- `03. detection_setup: saved processed video with detected vehicles`
- `03. zone_configuration: defined parking zones in configuration file`
- `03. zone_configuration: tested vehicle detection and zone setup`

**Step 4: Metrics Extraction and Visualization**

- `04. metrics_extraction: tracked vehicle occupancy in zones`
- `04. metrics_extraction: extracted total vehicle count and occupancy rates`
- `04. metrics_extraction: generated vehicle count and zone occupancy graphs`
- `04. visualization: produced heatmaps for zone occupancy`
- `04. video_processing: processed final video with detection overlays`

**Step 5: Output Presentation**

- `05. dashboard_setup: created interactive dashboard for real-time statistics`
- `05. report_generation: compiled PDF report with metrics and graphs`
- `05. report_generation: included final processed video in report`
- `05. presentation_preparation: created slides with key insights and outputs`
- `05. presentation_preparation: embedded video clips and graphs in slides`

**Step 6: Testing, Feedback, and Iteration**

- `06. testing: tested system on different parking lot scenarios`
- `06. testing: ensured consistent performance across scenarios`
- `06. feedback: gathered feedback from stakeholders`
- `06. optimization: optimized detection pipeline based on feedback`
- `06. optimization: refined parking zone configurations`

---

This commit list ensures that the development process is well-documented with clear and concise messages, making it easier to track progress and collaborate with others.
