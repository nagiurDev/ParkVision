# **Step-by-Step Plan for ParkVision**

## **Step 1: Data Collection and Preparation**

1.1 **Collect Video Data**

- Record or obtain custom video footage of the parking lot for training and testing.
- Ensure a variety of scenarios (daytime, nighttime, different weather conditions, etc.).

1.2 **Extract Frames from Video**

- Use a frame extraction tool to generate images from the video for annotation and training.
- Save extracted frames in the `data/extracted_frames/` directory.

1.3 **Annotate Frames for YOLO**

- Annotate the extracted frames to mark vehicles for YOLO training.
- Save annotations in YOLO format in the `data/annotations/` folder.

## **Step 2: Training the YOLO Model**

2.1 **Configure YOLO for Custom Data**

- Set up YOLO configuration (e.g., labels, input size) for the custom parking lot dataset.
- Prepare the dataset split into training, validation, and testing sets.

2.2 **Train the YOLO Model**

- Train YOLO on your custom dataset using the annotated images.
- Save the trained weights in the `data/model_weights/` directory.

2.3 **Evaluate the Model**

- Evaluate the trained YOLO model using the test set.
- Check performance metrics such as precision, recall, and mAP (mean Average Precision).
- Fine-tune the model if needed.


## **Step 3: Vehicle Detection and Parking Zone Setup**

3.1 **Set Up Trained YOLO Model for Detection**

- Load the trained YOLO model to detect vehicles in the raw video footage.
- Apply the model to the video and save the processed video with detected vehicles.

3.2 **Configure Parking Zones**

- Manually define parking zones by specifying the coordinates in the `configs/zone_config.yaml` file.
- These zones will be used to track vehicle occupancy.

3.3 **Test Vehicle Detection on the Video**

- Run the vehicle detection and parking zone setup to verify that vehicles are correctly detected and assigned to their respective zones.



## **Step 4: Metrics Extraction and Visualization**

4.1 **Extract Occupancy Metrics**

- Track vehicle occupancy within the defined zones.
- Extract key metrics, including total vehicles, time spent in each zone, and occupancy rates.

4.2 **Generate Visual Outputs**

- Create graphs to visualize vehicle count over time, zone occupancy rates, and peak usage hours.
- Produce heatmaps showing which parking zones are most frequently occupied.

4.3 **Process Final Video**

- Produce a final video with overlays (e.g., bounding boxes, color-coded parking zones) showing vehicle detection and parking status in real time.



## **Step 5: Output Presentation**

5.1 **Create Interactive Dashboard (Optional)**

- Develop an interactive dashboard to display real-time or post-processed statistics and visualizations (e.g., vehicle count, zone occupancy trends).

5.2 **Compile Final Report**

- Generate a PDF report with detailed insights, including vehicle counts, zone occupancy times, peak hours, and visual summaries (graphs, heatmaps).
- Include the final processed video in the report.

5.3 **Prepare Presentation**

- Create presentation slides with key insights and outputs, such as vehicle detection clips, graphs, and occupancy metrics.
- Embed short video clips and highlight important data points.

---

## **Step 6: Testing, Feedback, and Iteration**

6.1 **Run Full Tests on Different Data**

- Test the system on various parking lot scenarios (daytime, nighttime, different parking lot sizes).
- Ensure consistent performance across different conditions.

6.2 **Gather Feedback**

- Share the results and insights with stakeholders (clients, peers, etc.) to gather feedback on performance and usability.

6.3 **Refinement and Optimization**

- Based on feedback, optimize the detection pipeline, refine zone configurations, or add new features such as predictive analysis.
