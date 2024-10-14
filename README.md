# Symptom-Parsing-Project-
GenAI Symptom Parsing project
# Symptom Parsing Project

This project aims to build and enhance a **symptoms dictionary** by parsing patient symptoms data from a CSV file. It progresses through multiple stages of improving the dictionary to allow for more accurate symptom matching based on severity levels (mild, low, high). The final output shows how the enhanced dictionary improves the accuracy of parsing and matching symptoms in a dataset.

## Project Structure

### Step 1: Initial Data Reading and Dictionary Creation
- **Objective**: Read a CSV file containing patient symptoms and create an initial symptoms dictionary.
- **Details**:
  - The dataset contains information about patients, including symptoms like **Fever**, **Cough**, and **Cold**.
  - For each symptom, different severity levels (Mild, Low, High) are recorded.
  - The dictionary is initially constructed based on these symptoms and their severities.

### Step 2: Dictionary Enhancement and Loss Calculation
- **Objective**: Enhance the dictionary by comparing it with the dataset and identify missing symptoms.
- **Details**:
  - The script identifies any missing symptoms in the dictionary by comparing it against the dataset.
  - A quantified "loss" value is calculated, representing the symptoms from the dataset that are not present in the dictionary.
  - This step helps highlight gaps in the dictionary that need to be filled.

### Step 3: Severity Mapping and Complete Dictionary Enhancement
- **Objective**: Add severity levels (Mild, Low, High) for all symptoms and reduce the loss to zero.
- **Details**:
  - The dictionary is further improved by ensuring that all symptoms from the dataset are covered with appropriate severity levels.
  - The enhanced dictionary is saved as `symptoms_dict.json`, which now contains a comprehensive mapping of symptoms with their respective severities.

### Step 4: Symptom Parsing and Manual Updates
- **Objective**: Use the `SymptomParser` class to parse the dataset, enhance the dictionary, and allow for manual additions of symptoms.
- **Details**:
  - A Python class, `SymptomParser`, is created to handle the entire parsing process:
    - `read_data()`: Reads the dataset to parse patient symptoms.
    - `enhance_dictionary()`: Automatically adds missing symptoms from the dataset to the dictionary.
    - `manual_update()`: Allows users to manually add new symptoms that may not be in the dataset.
    - `print_data_based_on_dict()`: Displays the patient data based on the symptoms found in the dictionary.
    - `dump_dictionary()`: Saves the updated dictionary to `symptoms_dict.json`.
  - This step ensures that the dictionary evolves over time to include newly discovered symptoms, improving the parsing accuracy.

## Data Files
- **symptoms_dict.json**: This JSON file stores the final symptoms dictionary with mappings of symptoms and their severity levels (e.g., Fever: mild, low, high).
- **data.csv**: The dataset containing patient symptoms along with other attributes like fever, cough, body ache, shivering, etc.
- **Step4_Output.png**: An image file that demonstrates the output of the `SymptomParser` class, showing symptom matching before and after dictionary enhancement.

## Running the Project

1. **Step 1**: Run `Step1.ipynb` to read the dataset and create an initial symptoms dictionary.
2. **Step 2**: Execute `Step2.ipynb` to enhance the dictionary, print missing symptoms, and calculate the loss value.
3. **Step 3**: Use `Step3.ipynb` to complete the dictionary enhancement by adding severity levels and saving the final dictionary to `symptoms_dict.json`.
4. **Step 4**: Run `Step4.py` to instantiate the `SymptomParser` class, parse the dataset, print matched data, enhance the dictionary, and allow manual updates.

## Conclusion

The **Symptom Parsing Project** demonstrates a multi-step approach to constructing and refining a symptoms dictionary. By iteratively enhancing the dictionary with missing symptoms and adding severity levels, the project allows for improved parsing and analysis of patient data. The project also includes a mechanism for manual symptom additions, ensuring flexibility in handling new or custom symptoms.
