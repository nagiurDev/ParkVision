### **Project Structure:**

```
ParkVision/
│
├── documentation
│   ├── dev_process.md
│   ├── git_commits_darft.md
│   ├── project_structure.md
│   └── reference.md
|
├── data/                                  # All data-related files and directories
│   ├── raw_videos/                        # Raw video footage
│   ├── extracted_frames/                  # Frames extracted from the videos
│   ├── annotations/                       # YOLO annotation files (.txt format)
│   ├── model_weights/                     # Trained YOLO model weights (.pt or .pth)
│   └── processed_videos/                  # Processed videos (with detection results)
|
│
├── notebooks/                             # Jupyter notebooks for experiments, EDA, etc.
│   ├── eda.ipynb                          # Exploratory Data Analysis (EDA) notebook
│   ├── model_training.ipynb               # YOLO training and evaluation
│   ├── metrics_extraction.ipynb           # Metrics extraction and visualization
│   └── visualization.ipynb                # Generating graphs, charts, and heatmaps
│
├── src/                                   # Python scripts for various project tasks
│   ├── extract_frames.py                  # Script to extract frames from video
│   ├── train_yolo.py                      # Script to train YOLO on custom dataset
│   ├── evaluate_yolo.py                   # Script to evaluate YOLO model performance
│   ├── vehicle_detection.py               # Script to detect vehicles in video
│   ├── zone_configuration.py              # Script for parking zone configuration
│   ├── generate_visuals.py                # Script for generating visual outputs (graphs, heatmaps)
│   └── create_report.py                   # Script to compile all results into a report
│
├── models/                                # YOLO and other trained models
│   └── yolo/                              # YOLO-specific models and configs
│       ├── yolov5/                        # YOLOv5 model architecture
│       └── custom_yolo.yaml               # Custom YOLO configuration file
│
├── supervision/                           # Object tracking and supervision logic
│   ├── object_tracking.py                 # Script for vehicle tracking across frames
│   └── zone_supervision.py                # Supervision logic to monitor parking zones
│
├── configs/                               # Configurations for the project
│   ├── yolo_config.yaml                   # YOLO training and model configuration
│   ├── zone_config.yaml                   # Configuration for parking zone coordinates
│   └── video_processing_config.yaml       # Video processing settings and parameters
│
├── output/                                # Final outputs for presentation and visualization
│   ├── final_video_with_detections.mp4    # Final processed video with detection and annotations
│   ├── presentation/                      # Output for presentation purposes
│   │   ├── presentation.pptx              # PowerPoint or Google Slides presentation
│   │   └── video_clips/
│   └── reports/                           # Generated metrics, stats, and graphs
│       ├── summary_stats.csv              # CSV summary of quantitative metrics
│       ├── graphs/                        # Visual graphs (vehicle counts, occupancy, etc.)
│       ├── heatmaps/                      # Heatmaps showing occupancy trends
│       └── final_report.pdf                    # Short video clips for presentation
│
├── requirements.txt                       # Python package dependencies
├── README.md                              # Project overview and setup instructions
└── main.py                                # Main script to run the full pipeline (from data to presentation)

```

---

### **Updated Breakdown with Output Presentation:**

1. **`data/`:**

   - Stores all raw data, processed videos, and results. 

2. **`notebooks/`:**

   - Jupyter notebooks for easy experimentation, including separate notebooks for data analysis, model training, metrics extraction, and visualization.

3. **`src/`:**

   - Python scripts for performing core tasks like extracting frames, training models, detecting vehicles, and generating output visuals. **`create_report.py`** pulls everything together into a final PDF report with stats, graphs, and insights.

4. **`models/`:**

   - Houses trained YOLO models and their configurations, making it easy to update and reuse different YOLO versions.

5. **`supervision/`:**

   - Object tracking and parking zone supervision logic live here. This is where zone occupancy is tracked and calculated based on vehicle detections.

6. **`configs/`:**

   - Contains configuration files for the project, such as model training parameters, zone coordinates, and video processing settings.

7. **`output/`:**

   - This folder is crucial for presenting the final output:
     - **`final_video_with_detections.mp4`**: A video file showing real-time detection and tracking, with vehicle bounding boxes and parking zone occupancy highlighted.
     - **`presentation/`**: For creating a presentation, this subfolder includes PowerPoint slides (**`presentation.pptx`**) with embedded visuals, along with short video clips to showcase the results.
     - **`dashboard/`**: If an interactive dashboard is needed, the folder contains code to set up a web dashboard using **Flask/Dash**, allowing for live or post-hoc visualization of metrics and insights (e.g., parking zone occupancy, vehicle counts).

     - The **`reports/`** subfolder includes all graphs, heatmaps, and summary statistics, alongside a final **`PDF report`** summarizing the findings and insights.

8. **`requirements.txt`:**

   - Lists the Python dependencies needed to run the project, ensuring easy setup across environments.

9. **`README.md`:**

   - Provides a project overview, along with detailed instructions on how to set up and run the project.

10. **`main.py`:**
    - The central script that runs the entire pipeline: video processing, YOLO model inference, zone supervision, metrics extraction, and final output generation. You can run this script to generate the final report, video, and visuals in one go.

---

### **Output Presentation Strategy:**

1. **Video Demonstration:**

   - The **final processed video** will showcase the entire system in action, highlighting vehicle detection with bounding boxes, color-coded parking zones (free/occupied), and occupancy changes over time. This can be shared as part of the presentation or on its own.

2. **Interactive Dashboard:**

   - If real-time or interactive viewing is needed, the **dashboard** will provide live statistics and graphs showing vehicle detections and zone occupancy. Users can interact with graphs, change views, or view specific zone data.

3. **Presentation Slides:**

   - The **presentation folder** will contain the **PowerPoint slides** that summarize the project, including video clips, charts (e.g., occupancy rate, vehicle counts), and key metrics. The slides will make it easy to present in meetings, demos, or competitions.

4. **Final Report:**
   - The **PDF report** in the **reports/** folder will compile all metrics, graphs, and insights, such as total vehicles detected, average zone occupancy times, and peak usage periods. It will provide stakeholders with a detailed summary for review.
