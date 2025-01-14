
# Drive.AI
**AI-Powered Driving Learning Assistance**


![image](https://github.com/user-attachments/assets/c4199ed8-af62-4f15-b526-1962ca024be5)


Drive.AI is a cutting-edge AI solution designed to enhance road safety by providing real-time object detection and analysis. Using state-of-the-art technologies, Drive.AI delivers valuable insights and voice instructions to drivers, helping them navigate roads more safely and effectively.
We are proud to announce that Drive.AI won the Theme Prize for Road Safety at HackAthena 2024, recognizing the significant contribution our project makes to enhancing road safety using AI.

## Key Features

### 1. **Object Detection and Analysis**
- **Pedestrian Detection**: Identifies and analyzes pedestrians crossing the road.
- **Vehicle Recognition**: Detects and classifies nearby vehicles, including cars, motorcycles, and trucks.
- **Animal Detection**: Recognizes animals crossing the road.
- **Technology Used**: Powered by **Roboflow**, enabling efficient and accurate object detection.

### 2. **Utilization of YOLOv5 Model**
- **YOLO (You Only Look Once)**: Leverages the YOLOv5 model for fast and accurate object detection and classification.
- **JSON Output**: The model generates a JSON output containing detected objects and their classifications, allowing for further analysis.

### 3. **Response Generation with OpenAI API**
- **JSON Parsing**: Extracts relevant information from the YOLOv5-generated JSON output.
- **AI-Powered Instructions**: Uses **OpenAI's API** to generate dynamic responses based on the detected objects, providing actionable instructions to the driver.
- **Prompting the API**: Sends the class entity and prompt to OpenAI's API for precise instruction generation.

### 4. **Integration with Google Text-to-Speech**
- **Voice Instructions**: Converts generated responses into real-time voice instructions using **Google Text-to-Speech** technology.
- **Real-Time Assistance**: Provides voice-based guidance to drivers based on detected objects, ensuring quick and safe decision-making on the road.

## Road Safety Achievement
We are proud to announce that **Drive.AI** won the **Theme Prize for Road Safety** at [Event/Competition Name], recognizing the significant contribution our project makes to enhancing driver safety using AI.



## Project Structure

The project is organized as follows:

```
Drive.AI/
│
├── data/                   
├── models/                 
├── src/                    
│   ├── object_detection/   
│   ├── response_generation/ 
│   └── text_to_speech/    
│
├── requirements.txt        
├── config.py               
└── README.md               
```



## How to Run the Project

To run **Drive.AI** locally, follow these steps:

### Prerequisites
1. **Python 3.x** – Ensure that Python is installed.
2. **Install Dependencies** – Install the necessary Python libraries using `pip`. Run the following command:

   ```bash
   pip install -r requirements.txt
   ```

3. **API Keys** – Make sure to set up your **OpenAI API** and **Google Text-to-Speech** API keys. Update the `config.py` file with your credentials.

### Running the Application
1. **Load YOLOv5 Model**: Navigate to the `src/object_detection` directory and run the following command to load the YOLOv5 model and start object detection:

   ```bash
   python object_detection.py
   ```

2. **Process Output**: After object detection, the JSON output will be generated, containing information about the detected objects.

3. **Generate Instructions**: The `response_generation` script will parse the JSON output and send it to the OpenAI API for instruction generation.

   ```bash
   python response_generation.py
   ```

4. **Text-to-Speech Output**: Finally, the generated instructions will be converted into live voice instructions using Google Text-to-Speech.

   ```bash
   python text_to_speech.py
   ```

### Running the Entire Workflow
To run the full process in one go, execute the `main.py` script:

```bash
python main.py
```

This will load the model, detect objects, generate instructions, and provide voice-based assistance.

### License
This project is licensed under the MIT License - see the LICENSE file for details.



### Acknowledgments

We would like to extend our heartfelt thanks to the following individuals and organizations who made **Drive.AI** possible:

- **YOLOv5**: For providing the object detection model used in this project, enabling accurate and efficient detection of objects on the road.
- **Roboflow**: For offering tools and resources that helped preprocess and manage the datasets used in our object detection tasks.
- **OpenAI**: For powering our response generation, enabling real-time, context-aware instructions for drivers based on detected objects.
- **Google**: For their Text-to-Speech technology, which allowed us to convert text-based responses into real-time voice instructions.
- **HackAthena 2024**: For recognizing the impact of our project by awarding the **Theme Prize for Road Safety**, highlighting the importance of road safety in AI development.

