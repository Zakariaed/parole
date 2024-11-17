
# About the Dataset

## File Naming Convention
Each of the 7356 RAVDESS files has a unique filename. The filename consists of a 7-part numerical identifier (e.g., `02-01-06-01-02-01-12.mp4`). These identifiers define the stimulus characteristics:

### Filename Identifiers
1. **Modality**  
   - `01`: Full-AV  
   - `02`: Video-only  
   - `03`: Audio-only  

2. **Vocal Channel**  
   - `01`: Speech  
   - `02`: Song  

3. **Emotion**  
   - `01`: Neutral  
   - `02`: Calm  
   - `03`: Happy  
   - `04`: Sad  
   - `05`: Angry  
   - `06`: Fearful  
   - `07`: Disgust  
   - `08`: Surprised  

4. **Emotional Intensity**  
   - `01`: Normal  
   - `02`: Strong (NOTE: There is no strong intensity for the 'neutral' emotion)  

5. **Statement**  
   - `01`: "Kids are talking by the door"  
   - `02`: "Dogs are sitting by the door"  

6. **Repetition**  
   - `01`: 1st repetition  
   - `02`: 2nd repetition  

7. **Actor**  
   - `01` to `24`:  
     - Odd-numbered actors are male.  
     - Even-numbered actors are female.  

### Example Filename: `02-01-06-01-02-01-12.mp4`
- **Modality**: Video-only (`02`)  
- **Vocal Channel**: Speech (`01`)  
- **Emotion**: Fearful (`06`)  
- **Emotional Intensity**: Normal (`01`)  
- **Statement**: "Dogs are sitting by the door" (`02`)  
- **Repetition**: 1st repetition (`01`)  
- **Actor**: 12th actor (`12`, female)  

---

