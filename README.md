# 📱 Mobile Price Classification with Machine Learning

این پروژه به کمک چند الگوریتم یادگیری ماشین، قیمت موبایل‌ها را بر اساس ویژگی‌های سخت‌افزاری آن‌ها پیش‌بینی و طبقه‌بندی می‌کند.  
در نهایت با استفاده از **رأی‌گیری (Voting Classifier)** پیش‌بینی نهایی انجام می‌شود.  

---

## 📂 فایل‌های موجود
- 📘 **CLF_project.ipynb** → نوت‌بوک اصلی شامل کدها و تحلیل‌ها  
- 📊 **Classification task _Train Dataset.csv** → دیتاست آموزش (Training Dataset)  
- 📊 **Classification task _Test Dataset.csv** → دیتاست تست (Test Dataset)  
- 📊 **Predict.xlsx** → خروجی برچسب‌گذاری تست با مدل‌ها و رأی‌گیری  

---

## 📑 ویژگی‌های دیتاست
**Train Dataset (Classification task _Train Dataset.csv):**  
این دیتاست شامل مشخصات سخت‌افزاری موبایل‌ها و برچسب قیمت است.  
ویژگی‌ها:  

- `battery_power` → ظرفیت باتری (mAh)  
- `blue` → پشتیبانی از بلوتوث (0/1)  
- `clock_speed` → سرعت پردازنده (GHz)  
- `dual_sim` → پشتیبانی از دو سیم‌کارت (0/1)  
- `fc` → مگاپیکسل دوربین جلو  
- `four_g` → پشتیبانی از 4G (0/1)  
- `int_memory` → حافظه داخلی (GB)  
- `m_dep` → ضخامت موبایل (cm)  
- `mobile_wt` → وزن موبایل (g)  
- `n_cores` → تعداد هسته‌های پردازنده  
- `px_height` → ارتفاع تصویر (px)  
- `px_width` → عرض تصویر (px)  
- `ram` → مقدار رم (MB)  
- `sc_h` → ارتفاع صفحه‌نمایش (cm)  
- `sc_w` → عرض صفحه‌نمایش (cm)  
- `talk_time` → مدت مکالمه (ساعت)  
- `three_g` → پشتیبانی از 3G (0/1)  
- `touch_screen` → صفحه‌نمایش لمسی (0/1)  
- `wifi` → پشتیبانی از WiFi (0/1)  
- `price_range` → محدوده قیمت (0 تا 3) ← **برچسب هدف (Target Variable)**  

---

## ⚙️ وابستگی‌ها
برای اجرای پروژه نیاز به کتابخانه‌های زیر دارید:

```bash
numpy
pandas
matplotlib
seaborn
scikit-learn
````

---

## 🤖 مدل‌های پیاده‌سازی‌شده

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)

برای هر مدل از چند **هایپرپارامتر مختلف** استفاده شده و بهترین‌ها انتخاب شده‌اند.

---

## 🚀 نحوه اجرا

1. ریپازیتوری را کلون کنید یا فایل‌ها را دانلود کنید:

   ```bash
   git clone https://github.com/amirii/Mobile_Price_Classification.git
   ```
2. فایل **CLF\_project.ipynb** را در **Google Colab** یا **Jupyter Notebook** باز کنید.
3. دیتاست‌ها را در پوشه پروژه قرار دهید.
4. سلول‌ها را به ترتیب اجرا کنید تا نتایج و خروجی‌ها تولید شوند.

---

## ✅ نتایج مقایسه مدل‌ها

| مدل                    | بهترین پارامترها          | دقت (Accuracy) |
| ---------------------- | ------------------------- | -------------- |
| Logistic Regression    | `C=1.0, solver=lbfgs`     | 96.5%          |
| Decision Tree          | `entropy, max_depth=10`   | 88%            |
| Random Forest          | `200 trees, max_depth=15` | 89%            |
| Support Vector Machine | `C=1.0, kernel=rbf`       | 89.5%          |
| K-Nearest Neighbors    | `k=5`                     | 87%            |

---

## 📊 پیش‌بینی روی داده تست

* سه مدل **Logistic Regression، SVM، Random Forest** انتخاب شدند.
* برچسب‌گذاری تست در فایل **Predict.xlsx** ذخیره شد.
* پیش‌بینی نهایی با روش **رأی‌گیری (Voting Classifier)** انجام شد.

📈 نمودار مقایسه پیش‌بینی مدل‌ها و رأی‌گیری رسم شده است.

---

## 🔎 تحلیل ویژگی‌ها

با استفاده از **Random Forest Feature Importance**:

* **RAM** بیشترین تأثیر را روی قیمت دارد.
* بعد از آن **قدرت باتری** در رتبه دوم قرار می‌گیرد.



می‌خوای من یه **requirements.txt** هم بسازم که فقط با یه دستور `pip install -r requirements.txt` همه وابستگی‌ها نصب شن؟
```
