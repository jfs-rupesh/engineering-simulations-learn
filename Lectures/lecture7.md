Here’s a super clear and simple summary for **Lecture 9 – How to Find Nodal Temperatures**, based on your uploaded content.

Save this file as:

```
Introduction/lecture9.md
```

---

````markdown
# Lecture 9 – How to Find Nodal Temperatures (Made Simple)

## 🎯 What’s the Goal?

We want to find the **temperature at each node** (selected points) in a 1D bar using **Finite Element Method (FEM)**.

We already:
- Created a mathematical model (differential equation)
- Discretized the bar into **4 nodes**

Now we need to **calculate the temperature** at each node: `T1`, `T2`, `T3`, `T4`.

---

## 🧮 How We Do It – In Simple Steps

### 1️⃣ Start With the Governing Equation
- We already derived the **heat equation** (from the previous lecture)
- But that’s a **calculus** (differential) equation — we can't solve it directly by hand

### 2️⃣ Convert to Algebra
- FEM turns the big equation into **smaller equations**
- Each equation only connects a node to its neighbors:
  - Example: `T2` depends only on `T1` and `T3`
- This forms a **system of algebraic equations**

### 3️⃣ Write It as a Matrix
You get a system like this:
```text
[K] * [T] = [F]
````

Where:

* `[K]` = stiffness matrix (comes from FEM)
* `[T]` = vector of unknown temperatures (`T1`, `T2`, `T3`, `T4`)
* `[F]` = force or source vector (includes heat input, boundary conditions, etc.)

### 4️⃣ Solve It

* This becomes a simple **matrix problem**
* You can solve it like a regular system of equations to get all the temperatures

---

## 🧊 Then What?

Once you have the temperatures at the 4 nodes:

* You can **interpolate** to find temperature at any point in between
* You can also **differentiate** to find **heat flow** (called heat flux)

This is called **post-processing**.

---

## 🧠 Summary Table

| Step             | What Happens                            |
| ---------------- | --------------------------------------- |
| Create Model     | Start with the heat equation            |
| Discretize       | Break bar into 4 nodes                  |
| Set Up Equations | One equation per node, using neighbors  |
| Matrix Form      | Write system as `[K]*[T] = [F]`         |
| Solve            | Find T1, T2, T3, T4                     |
| Post-process     | Use these values to get everything else |

---

## ✅ Final Thought

> Instead of solving a hard equation everywhere, we just solve for a few points.
> FEM makes this possible — and efficient!

Everything the simulation tool shows you (color plots, charts) starts from these **nodal values**.

```

---

Let me know if you'd like:
- A diagram showing 4 nodes and temperature arrows
- The next lecture summarized
- Help creating a GitHub-friendly folder of all your lectures so far!
```
