# 🎧 Model Card: Music Recommender Simulation

## 1. Model Name  

VibeMatch Recommender 1.0  

---

## 2. Goal / Task  

The goal of this system is to recommend songs based on a user’s preferences.  
It suggests songs that match the user’s genre, mood, and overall vibe.

---

## 3. Data Used  

The dataset contains 10 songs.  

Each song includes:
- Genre  
- Mood  
- Energy  
- Tempo  
- Valence  
- Danceability  
- Acousticness  

The dataset includes a mix of genres such as pop, lofi, rock, and ambient.  
However, it is small and does not represent all types of music.

---

## 4. Algorithm Summary  

The system compares each song to the user’s preferences and assigns a score.  

- Songs get points for matching genre and mood  
- Songs get additional points if their energy, valence, and danceability are close to the user’s preferences  

The songs are then ranked from highest to lowest score, and the top results are recommended.

---

## 5. Observed Behavior / Biases  

The system tends to favor songs that match the user’s genre.  

During testing, I found that even when mood did not match, songs were still recommended if the genre matched. For example, in an edge-case profile (lofi + sad mood + high energy), the system still recommended mostly lofi songs.

This shows that genre has a stronger influence than mood, which can create a bias and reduce variety in recommendations.

---

## 6. Evaluation Process  

I tested the system using multiple user profiles:
- High-energy pop  
- Chill lofi  
- Intense rock  
- An edge-case with conflicting preferences  

In most cases, the recommendations matched the expected vibe. Pop users received energetic songs, while lofi users received calmer tracks.

The edge-case profile revealed that conflicting preferences can confuse the system, especially when one feature (like genre) dominates the scoring.

---

## 7. Intended Use and Non-Intended Use  

**Intended Use:**
- Learning how recommendation systems work  
- Demonstrating how user preferences affect results  

**Non-Intended Use:**
- Real music recommendation systems  
- Production or large-scale applications  

---

## 8. Ideas for Improvement  

- Add more songs to improve diversity  
- Balance feature weights (reduce genre dominance)  
- Add more features like lyrics or artist similarity  

---

## 9. Personal Reflection  

The biggest learning moment was seeing how small changes in scoring weights can completely change the recommendations.  

AI tools helped me write and debug code faster, but I had to double-check the logic to make sure it made sense.  

What surprised me is how a simple scoring system can still feel like a real recommendation engine.  

If I continued this project, I would expand the dataset and build a simple user interface.