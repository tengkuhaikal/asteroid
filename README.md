# Algorithm Analysis for Moira Market Selection & Asteroid Labyrinth

## **1. Moira Market Selection Using Greedy Algorithm**
### **Approach**
The selection process follows a **Greedy Algorithm**, which prioritizes durability while maintaining price constraints.

### **Steps**
1. **Filtering:** Excludes items where durability ≤ 85 or price > 800. `O(n)`
2. **Sorting:** Arranges filtered items in descending order of durability using **Timsort** (default in Pandas). `O(m log m)`
3. **Selection:** Picks the most durable first. `O(m)`

### **Complexity Analysis**
- **Filtering Step:** `O(n)`
- **Sorting Step:** `O(m log m)`
- **Selection Step:** `O(m)`
- **Overall Complexity:** `O(n log n)` (worst-case scenario)

### **Strengths & Limitations**
✅ **Strengths**
- Fast execution  
- Simple logic, easy to implement  
- Works well for **independent choices**  

❌ **Limitations**
- May **not** find the absolute best combination  
- **Ignores** compatibility or synergy between items  

---

## **2. Asteroid Labyrinth Grid Mapping**
### **Approach**
This implementation **divides** the asteroid field into a **10×10 grid**, calculating total asteroid density in each sector.

### **Steps**
1. **Define Grid:** Creates a **fixed 10×10 mapping** `O(1)`
2. **Assign Asteroid Sizes:** Iterates through `n` asteroids and increments danger grid values. `O(n)`
3. **Classification:** Marks sectors as **safe (green)** or **unsafe (red)** based on total density. `O(1)`

### **Complexity Analysis**
- **Grid Definition:** `O(1)`
- **Asteroid Processing:** `O(n)`
- **Classification:** `O(1) per grid`
- **Overall Complexity:** `O(n)` (worst-case scenario)

### **Strengths & Limitations**
✅ **Strengths**
- **Efficient hazard identification**  
- Simple **grid-based visualization**  
- Works well for **real-time mapping**  

❌ **Limitations**
- Grid resolution may **lack precision** for asteroid clusters  
- Doesn’t compute **optimal safe paths**, requiring an additional algorithm like **A***  

---

## **3. Future Enhancements**
🚀 **Moira Market Selection:**  
- Consider **synergy-based selection models** to optimize choices beyond simple durability.  
- Explore **dynamic programming** for **long-term strategic selection**.  

🚀 **Asteroid Navigation:**  
- Implement **A* pathfinding** to dynamically find the safest route through asteroid fields.  
- Increase **grid granularity** to improve precision in high-density asteroid zones.  

---

## **Conclusion**
Both implementations provide **efficient solutions** with **simple yet powerful algorithms**.  
Further **optimizations** and **integrations** can enhance their performance for **dynamic problem-solving scenarios**.

Let me know if you'd like refinements or additional sections! 🚀😃

---

# Moira Market Dataset Analysis

## Introduction
This project focuses on selecting the best items from the *Moira Market dataset* using the **Greedy Algorithm**.

### **Selection Criteria**
1. **Durability > 85**
2. **Price ≤ 800**

### **Approach**
The greedy method picks the **most durable item first**, ensuring a fast and efficient selection process.

---

## Dataset Overview
The dataset consists of **200+ futuristic components**, each with unique attributes:

- **Stall ID:** Location of the item in the market  
- **Item Name:** Sci-fi themed tech piece  
- **Price:** Cost of the item  
- **Durability:** Strength & longevity of the item  
- **Compatibility:** Suitability with existing systems  

---

## Applying Greedy Algorithm

### **Steps for Selection**
1. **Filter:** Remove items where durability ≤ 85 or price > 800.  
2. **Sort:** Arrange remaining items by durability (descending order).  
3. **Pick:** Always choose the most durable first—**greedy strategy**!

### **Sample Selection**
Using the greedy algorithm, the top items based on durability are:

| Stall ID  | Item Name       | Price | Durability | Compatibility |
|-----------|---------------|------|-----------|--------------|
| STALL-158 | Ion Core      | 205  | 98        | 0.94         |
| STALL-151 | Ion Filter    | 625  | 93        | 0.94         |
| STALL-190 | Neutron Lens  | 113  | 93        | 0.92         |
| STALL-091 | Neutron Shield | 101  | 87        | 0.64         |
| STALL-181 | Plasma Relay  | 629  | 87        | 0.96         |

---

## Complexity Analysis
- **Filtering Step:** `O(n)`
- **Sorting Step:** `O(m log m)` (Timsort in Pandas)
- **Selection Step:** `O(m)`
- **Overall Complexity:** `O(n log n)` in worst-case

---

## Pros & Cons of Greedy Selection

✅ **Pros**
- Fast execution  
- Simple logic  
- Works well for independent choices  

❌ **Cons**
- Doesn't always find the absolute best combination  
- Ignores compatibility or synergy between items  

---

## Conclusion
- **Greedy algorithms** are effective for **quick decision-making**.
- Alternative approaches (like **dynamic programming**) may find better overall solutions.
- Further optimizations could integrate **compatibility weighting** into the selection!

🚀 **Future Work:** Incorporate **synergy-based selection models** for better decision-making.

---

## Author
Project by *Haikal & Team*  
📅 **Date:** May 2025  
💻 **Tools Used:** Python (Pandas), Timsort, Algorithm Analysis
