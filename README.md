# ML-Regression-on-Avacado-dataset
Regression models for predicting Avacado prices in US.


### Problem Statement
 - Avacard-corp avocados are sourced from over 1000 growers owning over 65,000 acres across California, Mexico, Chile, and Peru.
 - With generations of experience growing, packing, and shipping avocados, they have a deep understanding of the avocado industry.
 - Their aim is to source quality fruit that’s sustainably grown and handled in the most efficient, shortest supply route possible.
 - They want to increase their supply throughout the United States and need to make sure that they are selling their products at the best possible price.
 - Avocado prices have rocketed in recent years by up to 129%, with the average national price in the US of a single Hass avocado reaching $2.10 in 2019, almost doubling in just one year.
 - Due to this uncertainty in the prices, the company is not able to sell their produce at the optimal price.
 - Our task is to predict the optimal price of the avocado using the previous sales data of avocado according to different regions.

### Dataset and Column Description

|Feature        |	Description                                               |
|---------------| ------------------------------------------------------------| 
|Id	            |   Unique identity of each observation.                      |
| Date 	        |   The date of the observation                               |
| Average Price |   The average price of a single avocado - target variable   |
| Total Volume  |   Total number of avocados sold                             | 
| 4046          |   Total number of avocados with PLU 4046 sold               | 
| 4225          |   Total number of avocados with PLU 4225 sold               |
| 4770          |   Total number of avocados with PLU 4770 sold               |
| Total Bags    |   Total number of bags sold.                                |
| Small Bags    |   Total number of small bags sold.                          |   
| Large Bags    |   Total number of avocados with PLU 4046 sold               | 
| XLarge Bags   |   Total number of avocados with PLU 4225 sold               |
| type          |   Conventional or Organic                                   |
| year 	        |   The year                                                  |
| region 	    |   The city or region of the observation                     |
  

The product/price lookup code (PLU) uniquely identifies a product (mainly produce).
- 4046: non-organic small/medium Hass Avocados (~3-5 oz)
- 4225: non-organic large Hass Avocados (~8-10 oz)
- 4770: non-organic extra large Hass Avocados (~10-15 oz)
----
- The dataset contains weekly retail scan data for National Retail Volume (units) and price.
- Retail scan data comes directly from retailers’ cash registers based on actual retail sales of Hass avocados.
- The column AveragePrice is the average price of a single avocado.
- This is the data that we have to predict for future samples.

### EDA Conclusions

- Every year, prices of avacados are higher in Second half of year, particularly in the September-October month.Prices are increasing year by year. Prices of avacados are higher in Autumn season.
- Most of the Avacados are in the price range 1.0 to 1.5.
- Hart Ford Springfield has highest average price in year 2017. Also, in San Franciso, there was a high rise in prices in year 2016-2017. 
- Organic Avacados are costlier as compared to Conventional ones. But Conventional ones are high in demand may be due to low prices.
- Sales of Avacados with Price Look up code of 4225 are higher.
 
 
### Model Evaluation Results

| Model                       |	MAE | MSE | RMSE | R-Sq | Adj R-Sq |
|-----------------------------|-----|-----|-----|-----|-----|
| Linear Regression	      |0.224|0.084|0.290|0.481|0.479|
| Decision Tree Model 1       |0.137|0.045|0.214|0.717|0.716|                                 
| Decision Tree Model 2       |0.173|0.052|0.228|0.679|0.677|    
| Decision Tree Model 3 (GSCV)|0.144|0.042|0.207|0.736|0.735|                              
| Random Forest Model 1       |0.102|0.021|0.147|0.8667|0.8663|                   
| Random Forest Model 2       |0.108|0.023|0.154|0.852|0.852|
| Random Forest Model 3 (GSCV)|0.102|0.021|0.147|0.8667|0.8662|                  

### Conclusions
- As per the Model Evaluation results section, it is clear that Random Forest Model 1 is giving the best Prediction Results and Random Forest Model 3 is not far behind and also giving equally good prediction results compared to other models used.
