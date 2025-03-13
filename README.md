# Organic Smoothie Co. - Optimization Using Excel Solver

## Overview
This project utilizes **Excel Solver** to determine the optimal production plan for **Organic Smoothie Co.**, which is launching a range of smoothie bowls. The goal is to **maximize profit** while ensuring ingredient availability, product demand, and recipe constraints are met.

The model incorporates:
- **Decision Variables**: Number of each smoothie bowl produced.
- **Objective Function**: Maximizing profit.
- **Constraints**: Ingredient availability, product demand, and recipe composition.

## Objectives
- Use **Excel Solver** to optimize the production mix.
- Apply **linear programming** to maximize profits while adhering to constraints.
- Conduct **sensitivity analysis** on ingredient costs.

## Ingredients & Availability
| Ingredient | Cost per Unit | Max Available |
|------------|--------------|--------------|
| Organic Greek Yogurt | $2.00 per cup | 500 cups |
| Fresh Mixed Berries | $3.00 per cup | 400 cups |
| Organic Honey | $1.00 per tbsp | 300 tbsp |
| Organic Granola | $1.50 per cup | 600 cups |

## Smoothie Bowls & Constraints
| Smoothie Bowl | Selling Price | Max Production | Key Composition Constraints |
|---------------|--------------|---------------|-----------------------------|
| Very Berry Blast | $13.00 | 700 bowls | At least 50% berries, 10% honey |
| Protein Punch | $10.00 | 500 bowls | 70% Greek yogurt, no honey |
| Energy Boost | $9.00 | 450 bowls | Under 20% granola, at least 25% berries |
| Sweet Crunch | $10.50 | 300 bowls | 20% honey, 40% granola |

## Constraints Used in Solver
1. **Ingredient Availability**: Cannot exceed stock limits.
   - `y1 ≤ 500`, `y2 ≤ 400`, `y3 ≤ 300`, `y4 ≤ 600`
2. **Product Demand Constraints**: Production cannot exceed maximum demand.
   - `x1 ≤ 700`, `x2 ≤ 500`, `x3 ≤ 450`, `x4 ≤ 300`
3. **Product Composition Constraints**: Each smoothie bowl must follow its recipe composition.
   - Very Berry Blast: `50% berries`, `10% honey`
   - Protein Punch: `70% Greek yogurt`, `No honey`
   - Energy Boost: `<20% granola`, `≥25% berries`
   - Sweet Crunch: `20% honey`, `40% granola`

## Results
- **Total Revenue**: `$20,657.00`
- **Total Production Costs**: `$3,380.50`
- **Staffing & Operational Costs** (32.5% of revenue): `$6,713.53`
- **Total Profit**: `$10,562.98`

| Smoothie Bowl | Optimal Production |
|---------------|-------------------|
| Very Berry Blast | 700 bowls |
| Protein Punch | 500 bowls |
| Energy Boost | 387 bowls |
| Sweet Crunch | 200 bowls |

## Sensitivity Analysis: Impact of Greek Yogurt Price Increase
The project evaluates how increasing the cost of Greek Yogurt from **$2.00 to $5.00** (in $0.50 increments) affects profit using **SolverTable**.

## Files in This Repository
```
📂 Organic_Smoothie_Solver/
 ├── 📜 Organic_Smoothie_Solver.xlsx  # Excel file with Solver optimization model
 ├── 📜 README.md  # Project documentation (this file)
```

## How to Use
1. Open `Organic_Smoothie_Solver.xlsx` in **Microsoft Excel**.
2. Go to the `Data` tab and open **Solver**.
3. Click **Solve** to run the optimization model.
4. Review the solution and profit calculations.

## Tools & Technologies Used
- **Microsoft Excel Solver**
- **Linear Programming**
- **Sensitivity Analysis** (SolverTable)

## Author
**Satkar Karki**  
[LinkedIn](https://www.linkedin.com/in/satkarkarki)  
[GitHub](https://github.com/satkar605)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
