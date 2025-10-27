# TCG_Locker_Shopify

## Table of Contents

<!--ts-->

* [First Install](#first-install-)
    * [1. Install the TCG Locker App](#1-install-the-tcg-locker-app-)
    * [2. Configure General Settings](#2-configure-general-settings-)
    * [3. Configure Address Settings](#3-configure-address-settings-)
    * [4. Select TCG Locker Source Locker](#4-select-tcg-locker-source-locker-)
    * [5. Enter Company Address](#5-enter-company-address-)
    * [6. Enter Contact Details](#6-enter-contact-details-)
    * [7. Select Locker Size](#7-select-locker-size-)
    * [8. Optional Settings](#8-optional-settings-)
        * [8.1 Add Carrier Rates to Shopify on Save](#81-add-carrier-rates-to-shopify-on-save-)
        * [8.2 Enable TCG Locker Confirmation](#82-enable-tcg-locker-confirmation-)
    * [9. Save Settings](#9-save-settings-)
    * [10. Finishing Steps](#10-finishing-steps-)
        * [10.1 Shipping Address Phone Number](#101-shipping-address-phone-number-)
        * [10.2 Shipping Address Email](#102-shipping-address-email-)
        * [10.3 Flat-Rate Shipping Methods](#103-flat-rate-shipping-methods-)
        * [10.4 Locker Confirmation Thank You Page](#104-locker-confirmation-thank-you-page-)
* [Testing the Configuration](#testing-the-configuration-)
    * [1. Prime Checkout](#1-prime-checkout-)
    * [2. Select TCG Locker Method](#2-select-tcg-locker-method-)
    * [3. Complete TCG Locker Destination Selection](#3-complete-tcg-locker-destination-selection-)
    * [4. Enter OTP and Confirm](#4-enter-otp-and-confirm-)

<!--te-->

## First Install [🔼](#table-of-contents)

### 1. Install the TCG Locker App [🔼](#table-of-contents)

Install the TCG Locker app on your Shopify site by [clicking here](https://apps.shopify.com/pudo-1). Click the "Install"
button. If you have multiple Shopify sites linked to your account, select the relevant website first. Once your
dashboard appears, click the "Install" button again. After installation, you will be redirected to TCG Locker settings
page.

> ![TCG Locker Guide](/assets/tcg-locker/1-install-the-shopify-app.png)

### 2. Configure General Settings [🔼](#table-of-contents)

Under the "General" tab, fill in **Company Name**, **The Courier Guys Locker API URL** and **The Courier Guys Locker API
Key**. The other fields in the general
tab are optional.

> ![TCG Locker Guide](/assets/tcg-locker/2-configure-general-settings.png)

### 3. Configure Address Settings [🔼](#table-of-contents)

Expand the "Address" tab and choose a preferred value for the “The Courier Guys Locker Source” dropdown (either Locker
or Street Address).

> ![TCG Locker Guide](/assets/tcg-locker/3-configure-address-settings.png)

### 4. Select TCG Locker Source Locker [🔼](#table-of-contents)

In the “Locker Number” field, select your preferred TCG Locker source locker. This is required so clients can choose
**Locker** -> **Door or Locker** -> **Locker** at checkout.

> ![TCG Locker Guide](/assets/tcg-locker/4-select-tcg-locker-source-locker.png)

### 5. Enter Company Address [🔼](#table-of-contents)

Fill in your **Street Address**, **Suburb**, **City**, **Province**, **Postal Code**. The “Country” field is restricted
to “South Africa.”

> ![TCG Locker Guide](/assets/tcg-locker/5-enter-company-address.png)

### 6. Enter Contact Details [🔼](#table-of-contents)

Fill in your **Contact Name**, **Email** and **Phone**.

> ![TCG Locker Guide](/assets/tcg-locker/6-enter-contact-details.png)

### 7. Select Locker Size [🔼](#table-of-contents)

Under the “Locker” dropdown, choose the locker size that all orders will be restricted to (Extra Small, Small, Medium,
Large, Extra Large). You can only have one locker size attached to your Shopify website.

> ![TCG Locker Guide](/assets/tcg-locker/7-select-locker-size.png)

### 8. Optional Settings [🔼](#table-of-contents)

> ![TCG Locker Guide](/assets/tcg-locker/8-optimal-settings.png)

#### 8.1 Add Carrier Rates to Shopify on Save [🔼](#table-of-contents)

Available for most Shopify Plans (excludes monthly Basic Plan). It adds dynamic rates to your shipping.

#### 8.2 Enable TCG Locker Confirmation [🔼](#table-of-contents)

This notifies the merchant whether the customer has selected a locker. Once the order is placed, the customer can select
their locker on the Thank You page.

> ![TCG Locker Guide](/assets/tcg-locker/8-2-enable-tcg-locker-confirmation.png)

### 9. Save Settings [🔼](#table-of-contents)

Click the **Save Settings** button to save your configuration.

> ![TCG Locker Guide](/assets/tcg-locker/9-save-settings.png)

### 10. Finishing Steps [🔼](#table-of-contents)

These finishing steps help to ensure the plugin is configured correctly.

> ![TCG Locker Guide](/assets/tcg-locker/10-finishing-steps.png)

#### 10.1 Shipping Address Phone Number [🔼](#table-of-contents)

Click the notification for **Shipping Address Phone Number** to load a popup with Shopify checkout settings. Ensure that
the phone number for shipping addresses is required.

> ![TCG Locker Guide](/assets/tcg-locker/10-1-shipping-address-phone-number.png)

#### 10.2 Shipping Address Email [🔼](#table-of-contents)

Ensure that the Customer contact method is set to 'Email'.

> ![TCG Locker Guide](/assets/tcg-locker/10-2-shipping-address-email.png)

#### 10.3 Flat-Rate Shipping Methods [🔼](#table-of-contents)

If you are on a Basic Plan or don't wish to use Carrier Rates, create 2 flat-rate shipping methods for your South
African shipping zone, ensuring they include “Locker” or "locker" in their names (e.g., The Courier Guy Locker or The
Courier Guy Locker to
Door).

> ![TCG Locker Guide](/assets/tcg-locker/10-3-flat-rate-shipping-methods.png)

#### 10.4 Locker Confirmation Thank You Page [🔼](#table-of-contents)

Navigate to **Settings** → **Checkout** → **Customize** to configure the Thank You page. Enable the
**checkout-locker-select** block under **Apps** to allow customers to select their locker destination after purchase.

> ![TCG Locker Guide](/assets/tcg-locker/10-4-locker-confirmation-thank-you.png)

## Testing the Configuration [🔼](#table-of-contents)

### 1. Prime Checkout [🔼](#table-of-contents)

Navigate to the front end of your Shopify store, add a product to your cart and navigate to the Checkout page.

> ![TCG Locker Guide](/assets/tcg-locker/1-prime-checkout.png)

### 2. Select TCG Locker Method [🔼](#table-of-contents)

Add your shipping address and select the TCG Locker method at checkout. You will be able to confirm your TCG Locker
selection on the Thank You page after completing your order. Ensure you have access to the email used at checkout, as it
will receive the OTP pin required to submit your shipment.

> ![TCG Locker Guide](/assets/tcg-locker/2-select-tcg-locker-method.png)

### 3. Complete TCG Locker Destination Selection [🔼](#table-of-contents)

On the Thank You page, click the **Confirm** button.

> ![TCG Locker Guide](/assets/tcg-locker/3-complete-tcg-locker-destination-selection.png)

### 4. Enter OTP and Confirm [🔼](#table-of-contents)

Navigate to your email to retrieve the OTP, enter it, select your Locker destination, and click **Continue**.

> ![TCG Locker Guide](/assets/tcg-locker/4-enter-otp-and-confirmation.png)
