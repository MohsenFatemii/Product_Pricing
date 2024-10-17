# Pricing Calculator

## Mathematical Concepts

### 1. Initial Price Calculation
The base price for each item is calculated using the following formula:

$$\text{Initial Price} = \text{Base Cost} \times \text{Base Multiplier} \times (1 + \text{Target Profit Margin})$$

where:

$$\text{Base Multiplier} = \frac{1}{1 - \text{Tax Rate} - \text{Other Expenses Rate}}$$

This formula ensures that after accounting for taxes and expenses, the desired profit margin is maintained.

### 2. Volume-Based Price Adjustment

Each item's price is adjusted based on its sales volume:

$$\text{Volume Discount} = \min(0.15, \frac{\text{Item Daily Sales}}{\text{Total Daily Sales}} \times 0.2)$$

$$\text{Adjusted Price} = \text{Initial Price} \times (1 - \text{Volume Discount})$$

This creates a maximum discount of 15% for high-volume items.

### 3. Rent Distribution
Rent is distributed proportionally based on sales volume:

$$\text{Rent Portion per Item} = \frac{\text{Daily Rent} \times (\text{Item Sales} / \text{Total Sales})}{\text{Item Sales}}$$

$$\text{Final Base Price} = \text{Adjusted Price} + \text{Rent Portion}$$

### 4. Profit Calculation

The total profit is calculated through several steps:

$$\text{Total Revenue} = \sum (\text{Price}_i \times \text{Sales}_i)$$

$$\text{Total Base Costs} = \sum (\text{Base Cost}_i \times \text{Sales}_i)$$

$$\text{Temporary Revenue} = \text{Total Revenue} - \text{Total Base Costs} - \text{Daily Rent}$$

$$\text{Tax Amount} = \text{Temporary Revenue} \times \text{Tax Rate}$$

$$\text{Other Expenses} = \text{Temporary Revenue} \times \text{Other Expenses Rate}$$

$$\text{Final Profit} = \text{Temporary Revenue} - \text{Tax Amount} - \text{Other Expenses}$$

### 5. Price Optimization
The calculator uses gradient descent to optimize prices:
- Learning Rate: 0.01
- Maximum Iterations: 100
- Convergence Threshold: 0.001 (0.1% difference from target margin)

The adjustment formula is:

$$\text{New Price} = \text{Current Price} \times (1 \pm \text{Learning Rate})$$

where the sign depends on whether the current profit margin is below or above.

# ماشین حساب قیمت‌گذاری

## مفاهیم ریاضیاتی

### ۱. محاسبه قیمت اولیه
قیمت پایه برای هر آیتم با استفاده از فرمول زیر محاسبه می‌شود:

$$\text{Initial Price} = \text{Base Cost} \times \text{Base Multiplier} \times (1 + \text{Target Profit Margin})$$

که در آن:

$$\text{Base Multiplier} = \frac{1}{1 - \text{Tax Rate} - \text{Other Expenses Rate}}$$

این فرمول اطمینان حاصل می‌کند که پس از محاسبه مالیات‌ها و هزینه‌ها، حاشیه سود مطلوب حفظ شود.

### ۲. تنظیم قیمت بر اساس حجم فروش
قیمت هر آیتم بر اساس حجم فروش آن تنظیم می‌شود:

$$\text{Volume Discount} = \min(0.15, \frac{\text{Item Daily Sales}}{\text{Total Daily Sales}} \times 0.2)$$

$$\text{Adjusted Price} = \text{Initial Price} \times (1 - \text{Volume Discount})$$

این تنظیم تخفیف حداکثر ۱۵٪ برای آیتم‌های با حجم فروش بالا ایجاد می‌کند.

### ۳. توزیع اجاره
اجاره بر اساس حجم فروش به صورت نسبتی توزیع می‌شود:

$$\text{Rent Portion per Item} = \frac{\text{Daily Rent} \times (\text{Item Sales} / \text{Total Sales})}{\text{Item Sales}}$$

$$\text{Final Base Price} = \text{Adjusted Price} + \text{Rent Portion}$$

### ۴. محاسبه سود
سود کل در چند مرحله محاسبه می‌شود:

$$\text{Total Revenue} = \sum (\text{Price}_i \times \text{Sales}_i)$$

$$\text{Total Base Costs} = \sum (\text{Base Cost}_i \times \text{Sales}_i)$$

$$\text{Temporary Revenue} = \text{Total Revenue} - \text{Total Base Costs} - \text{Daily Rent}$$

$$\text{Tax Amount} = \text{Temporary Revenue} \times \text{Tax Rate}$$

$$\text{Other Expenses} = \text{Temporary Revenue} \times \text{Other Expenses Rate}$$

$$\text{Final Profit} = \text{Temporary Revenue} - \text{Tax Amount} - \text{Other Expenses}$$

### ۵. بهینه‌سازی قیمت

ماشین حساب از گرادیان نزولی برای بهینه‌سازی قیمت‌ها استفاده می‌کند:
- نرخ یادگیری: ۰.۰۱
- حداکثر تکرار: ۱۰۰
- آستانه همگرایی: ۰.۰۰۱ (اختلاف ۰.۱٪ از حاشیه سود هدف)

فرمول تنظیم:

$$\text{New Price} = \text{Current Price} \times (1 \pm \text{Learning Rate})$$

که علامت آن بستگی به این دارد که حاشیه سود فعلی کمتر یا بیشتر از هدف باشد.

