# us-insurance-cost-analysis
"Analysis of US health insurance costs using PostegreSQL"
Strategic Insurance Risk & Pricing Analysis using PostgreSQL / Postgre SQL تحلیل استراتژیک ریسک و قیمت‌گذاری بیمه با
Project Structure/ساختار پروژه:The entire analysis workflow is transparent and organized; all PostgreSQL scripts reside in the SQL_Queries/ directory, and the raw Kaggle data is stored in the Data/ directory
تمامی مراحل تحلیل با شفافیت کامل ارائه شده است؛ کدهای PostgreSQL در پوشه SQL_Queries/ و داده‌های خام Kaggle در پوشه Data/ در دسترس هستند.
Metodology / روش کار : The project data was sourced from the Kaggle platform (Insurance Dataset). After standardizing the data encoding to UTF8, it was loaded into a PostgreSQL database. All structured business analyses, including risk segmentation and pricing metrics calculation, were performed using optimized SQL queries/////
 داده‌های مورد نیاز پروژه از پلتفرم Kaggle (مجموعه داده Insurance) تهیه و پس از استانداردسازی کدگذاری (UTF8)،در دیتابیس PostgreSQL بارگذاری شدند. تمام تحلیل‌های ساختاریافته‌ی کسب‌وکار، از جمله بخش‌بندی ریسک(Segmentation) و محاسبه‌ی شاخص‌های قیمت‌گذاری (Pricing Metrics)، با استفاده از کوئری‌های بهینه‌سازی‌شده‌ی SQL انجام گرفت.
Key Findings/یافته های کلیدی :  The deep dive analysis of the insurance data identified three core risk segments and delivered actionable insights for immediate pricing optimization:

1.BMI & Profit Margin: The Obese (BMI > 30) segment is the primary cost driver, with average charges approximately 50% higher than the normal weight group. This justifies an immediate, data-driven premium increase for this high-risk segment.
### 2. BMI Segmentation & Pricing Insight

| BMI Category             | Avg. Charges (USD) | Total Individuals |
| :---                     | :---:              | :---: |
| Obese (Over 30)          | $15,560.93         | 705 |
| Overweight (25-30)       | $10,410.47         | 386 |
| Normal Weight (18.5-25)  | $8,527.27          | 221 |
| Underweight (Under 18.5) | $8,143.08          | 26 |
link:


2.Hidden Family Risk: We found a significant correlation where the cost per child is drastically higher in smoker households. This demands targeted risk penalties on family coverage to accurately reflect and cover this aggregated health risk.

3.Strategic Customer Acquisition: Smoker Status is 4–5 times more critical than gender. To enhance profit stability and acquire the lowest-risk base, our acquisition strategy should strategically prioritize Non-Smoking Females.
Analysis Focus :
1. Primary Risk Driver (Smoker)Smoker Status is a Cost Multiplier: Average charges for smokers are 4x to 5x higher than non-smokers. This gap is the most critical pricing inefficiency and requires immediate, data-justified premium adjustments.
2. BMI SegmentationFocus on Obese Segment: Customers classified as Obese (BMI > 30) are the dominant high-cost segment, generating average charges 50% higher than the Normal Weight group. Pricing must strictly reflect this increased cost.
3. Hidden Family RiskAggregated Family Risk: Cost per child is significantly higher in smoker households. This validates the need to price risk not just by individual, but by accumulated household risk to prevent profit leakage.
4. Geographical AnalysisResource Optimization: The highest average cost per customer is located in the [Southeast] area. Marketing efforts should pivot to lower-risk regions, while intensive health programs should target this high-cost region.
5. Gender & StrategyLow-Risk Acquisition Target: While smoker status is the ultimate determinant of cost, among non-smokers, non-smoking females represent the lowest overall risk baseline and should be prioritized for profit-margin stabilization.
محور تحلیل:
1.ریسک کلیدی (سیگار)	: سیگار یک عامل ریسک نیست، بلکه یک ضریب ریسک است: میانگین هزینه‌های افراد سیگاری ۴ تا ۵ برابر بیشتر از غیرسیگاری‌هاست. این شکاف باید مستقیماً در نرخ‌های حق بیمه‌ی پایه اعمال شود.
2. تقسیم بندی BMI     :	تمرکز منابع روی چاقی: مشتریان با BMI بالای ۳۰ (Obese) بزرگترین کانون ریسک هستند و به طور متوسط ۵۰٪ هزینه‌های بالاتری ایجاد می‌کنند. قیمت‌گذاری ما باید این افزایش هزینه را به طور کامل پوشش دهد.
3.ریسک پنهان خانواده‌ها	:  نفوذ ریسک در خانواده: هزینه‌های به ازای هر فرزند در خانواده‌های سیگاری به وضوح بالاتر است. ما باید ریسک کل خانواده را تجمیع کنیم و برنامه‌های مدیریت سلامت را روی این خانواده‌ها متمرکز سازیم.
4.تحلیل جغرافیایی      :	بهینه‌سازی توزیع ریسک: منطقه [منطقه پرهزینه در خروجی شما] بالاترین میانگین هزینه را دارد. باید بودجه‌ی بازاریابی به سمت مناطق کم‌ریسک هدایت شده و در منطقه پرهزینه، استراتژی‌های کاهش ریسک اجرا شود.
5.ریسک بر اساس جنسیت:	استراتژی جذب کم‌ریسک: عامل سیگاری بودن، مهم‌ترین جداکننده‌ی ریسک است. در گروه غیرسیگاری‌ها، زنان غیرسیگاری به‌طور کلی کمترین ریسک پایه را دارند و بهترین هدف برای جذب مشتریان جدید و سودآور هستند.
