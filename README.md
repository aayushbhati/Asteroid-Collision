# Asteroid Collision

## Problem Description

You are given an integer array `asteroids`, where each element represents an asteroid in space:

- The **absolute value** of each number is the **size** of the asteroid.
- The **sign** represents the **direction**:
  - Positive (`+`) means the asteroid is moving **right**.
  - Negative (`-`) means it is moving **left**.

All asteroids move at the **same speed**.

### Rules for Collisions:
- Only **opposite direction** asteroids can collide (a right-moving asteroid and a left-moving one).
- When they collide:
  - The **smaller asteroid explodes**.
  - If both are of **equal size**, **both explode**.
  - Asteroids moving in the **same direction** never collide.

Return the **final state** of the asteroids after all collisions.

---

## Examples

### Example 1:

**Input:**  
`asteroids = [5,10,-5]`  
**Output:**  
`[5,10]`  

**Explanation:**
- `10` and `-5` collide → `10` survives (larger)
- `5` and `10` never collide (same direction)

---

### Example 2:

**Input:**  
`asteroids = [8,-8]`  
**Output:**  
`[]`  

**Explanation:**
- `8` and `-8` are equal → both explode

---

### Example 3:

**Input:**  
`asteroids = [10,2,-5]`  
**Output:**  
`[10]`  

**Explanation:**
- `2` and `-5` collide → `-5` survives (larger)
- `10` and `-5` collide → `10` survives (larger)

---

## Constraints

- `2 <= asteroids.length <= 10⁴`
- `-1000 <= asteroids[i] <= 1000`
- `asteroids[i] != 0` (no zero-sized asteroids)
