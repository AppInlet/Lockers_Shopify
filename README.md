# TCG_Lockers_Shopify

## Table of Contents

<!--ts-->

* [First Install](#first-install-)
    * [1. Install the TCG Lockers App](#1-install-the-tcg-lockers-app-)
    * [2. Configure General Settings](#2-configure-general-settings-)
    * [3. Configure Address Settings](#3-configure-address-settings-)
    * [4. Select TCG Lockers Source Locker](#4-select-tcg-lockers-source-locker-)
    * [5. Enter Company Address](#5-enter-company-address-)
    * [6. Enter Contact Details](#6-enter-contact-details-)
    * [7. Select Locker Size](#7-select-locker-size-)
    * [8. Optional Settings](#8-optional-settings-)
        * [8.1 Add Carrier Rates to Shopify on Save](#81-add-carrier-rates-to-shopify-on-save-)
        * [8.2 Enable TCG Lockers Locker Confirmation](#82-enable-tcg-lockers-locker-confirmation-)
    * [9. Save Settings](#9-save-settings-)
    * [10. Finishing Steps](#10-finishing-steps-)
        * [10.1 Shipping Address Phone Number](#101-shipping-address-phone-number-)
        * [10.2 Shipping Address Email](#102-shipping-address-email-)
        * [10.3 Flat-Rate Shipping Methods](#103-flat-rate-shipping-methods-)
        * [10.4 Locker Confirmation Post-Purchase](#104-locker-confirmation-post-purchase-)
* [Testing the Configuration](#testing-the-configuration-)
    * [1. Prime Checkout](#1-prime-checkout-)
    * [2. Select TCG Lockers Method](#2-select-tcg-lockers-method-)
    * [3. Complete TCG Lockers Destination Selection](#3-complete-tcg-lockers-destination-selection-)
    * [4. Enter OTP and Confirm](#4-enter-otp-and-confirm-)

<!--te-->

## First Install [🔼](#table-of-contents)

### 1. Install the TCG Lockers App [🔼](#table-of-contents)

Install the TCG Lockers app on your Shopify site by [clicking here](https://apps.shopify.com/pudo-1). Click the "Install"
button. If you have multiple Shopify sites linked to your account, select the relevant website first. Once your
dashboard appears, click the "Install" button again. After installation, you will be redirected to TCG Lockers settings page.

> ![TCG Lockers Guide](/assets/tcg-lockers/1-install-the-shopify-app.png)

### 2. Configure General Settings [🔼](#table-of-contents)

Under the "General" tab, fill in **Company Name**, **The Courier Guys Lockers API URL** and **The Courier Guys Lockers API Key**. The other fields in the general
tab are optional.

> ![TCG Lockers Guide](/assets/tcg-lockers/2-configure-general-settings.png)

### 3. Configure Address Settings [🔼](#table-of-contents)

Expand the "Address" tab and choose a preferred value for the “The Courier Guys Lockers Source” dropdown (either Locker or Street Address).

> ![TCG Lockers Guide](/assets/tcg-lockers/3-configure-address-settings.png)

### 4. Select TCG Lockers Source Locker [🔼](#table-of-contents)

In the “Locker Number” field, select your preferred TCG Lockers source locker. This is required so clients can choose
**Locker** -> **Door or Locker** -> **Locker** at checkout.

> ![TCG Lockers Guide](/assets/tcg-lockers/4-select-tcg-lockers-source-locker.png)

### 5. Enter Company Address [🔼](#table-of-contents)

Fill in your **Street Address**, **Suburb**, **City**, **Province**, **Postal Code**. The “Country” field is restricted
to “South Africa.”

> ![TCG Lockers Guide](/assets/tcg-lockers/5-enter-company-address.png)

### 6. Enter Contact Details [🔼](#table-of-contents)

Fill in your **Contact Name**, **Email** and **Phone**.

> ![TCG Lockers Guide](/assets/tcg-lockers/6-enter-contact-details.png)

### 7. Select Locker Size [🔼](#table-of-contents)

Under the “Lockers” dropdown, choose the locker size that all orders will be restricted to (Extra Small, Small, Medium,
Large, Extra Large). You can only have one locker size attached to your Shopify website.

> ![TCG Lockers Guide](/assets/tcg-lockers/7-select-locker-size.png)

### 8. Optional Settings [🔼](#table-of-contents)

> ![TCG Lockers Guide](/assets/tcg-lockers/8-optimal-settings.png)

#### 8.1 Add Carrier Rates to Shopify on Save [🔼](#table-of-contents)

Available for most Shopify Plans (excludes monthly Basic Plan). It adds dynamic rates to your shipping.

#### 8.2 Enable TCG Lockers Locker Confirmation [🔼](#table-of-contents)

This notifies the merchant on the submission page whether the customer has selected a locker. Once submitted, the
customer's selection is pre-populated on the Submission page.

> ![TCG Lockers Guide](/assets/tcg-lockers/8-2-enable-tcg-lockers-locker-confirmation.png)

### 9. Save Settings [🔼](#table-of-contents)

Click the **Save Settings** button to save your configuration.

> ![TCG Lockers Guide](/assets/tcg-lockers/9-save-settings.png)

### 10. Finishing Steps [🔼](#table-of-contents)

These finishing steps help to ensure the plugin is configured correctly.

> ![TCG Lockers Guide](/assets/tcg-lockers/10-finishing-steps.png)

#### 10.1 Shipping Address Phone Number [🔼](#table-of-contents)

Click the notification for **Shipping Address Phone Number** to load a popup with Shopify checkout settings. Ensure that
the phone number for shipping addresses is required.

> ![TCG Lockers Guide](/assets/tcg-lockers/10-1-shipping-address-phone-number.png)

#### 10.2 Shipping Address Email [🔼](#table-of-contents)

Ensure that the Customer contact method is set to 'Email'.

> ![TCG Lockers Guide](/assets/tcg-lockers/10-2-shipping-address-email.png)

#### 10.3 Flat-Rate Shipping Methods [🔼](#table-of-contents)

If you are on a Basic Plan or don't wish to use Carrier Rates, create 2 flat-rate shipping methods for your South
African shipping zone, ensuring they include “The Courier Guy Lockers Locker” in their names (e.g., The Courier Guy Lockers Locker L2D or The Courier Guy Lockers Locker to
Door).

> ![TCG Lockers Guide](/assets/tcg-lockers/10-3-flat-rate-shipping-methods.png)

#### 10.4 Locker Confirmation Post-Purchase [🔼](#table-of-contents)

> ![TCG Lockers Guide](/assets/tcg-lockers/10-4-locker-confirmation-post-purchase.png)

## Testing the Configuration [🔼](#table-of-contents)

### 1. Prime Checkout [🔼](#table-of-contents)

Navigate to the front end of your Shopify store, add a product to your cart and navigate to the Checkout page.

> ![TCG Lockers Guide](/assets/tcg-lockers/1-prime-checkout.png)

### 2. Select TCG Lockers Method [🔼](#table-of-contents)

Add your shipping address and select the TCG Lockers method (Confirm TCG Lockers Locker on the next page) at checkout. Ensure you have
access to the email used at checkout, as it will receive the OTP pin required to submit your shipment.

> ![TCG Lockers Guide](/assets/tcg-lockers/2-select-tcg-lockers-method.png)

### 3. Complete TCG Lockers Destination Selection [🔼](#table-of-contents)

On the post-purchase page, click the **Confirm** button.

> ![TCG Lockers Guide](/assets/tcg-lockers/3-complete-tcg-lockers-destination-selection.png)

### 4. Enter OTP and Confirm [🔼](#table-of-contents)

Navigate to your email to retrieve the OTP, enter it, select your Locker destination, and click **Continue**.

> ![TCG Lockers Guide](/assets/tcg-lockers/4-enter-otp-and-confirmation.png)
