# PUDO_Shopify

## Table of Contents
<!--ts-->
* [First Install](#first-install-)
    * [1. Install the PUDO App](#1-install-the-pudo-app-)
    * [2. Configure General Settings](#2-configure-general-settings-)
    * [3. Configure Address Settings](#3-configure-address-settings-)
    * [4. Select PUDO Source Locker](#4-select-pudo-source-locker-)
    * [5. Enter Company Address](#5-enter-company-address-)
    * [6. Enter Contact Details](#6-enter-contact-details-)
    * [7. Select Locker Size](#7-select-locker-size-)
    * [8. Optional Settings](#8-optional-settings-)
      * [8.1 Add Carrier Rates to Shopify on Save](#81-add-carrier-rates-to-shopify-on-save-)
      * [8.2 Enable PUDO Locker Confirmation](#82-enable-pudo-locker-confirmation-)
    * [9. Save Settings](#9-save-settings-)
    * [10. Finishing Steps](#10-finishing-steps-)
      * [10.1 Shipping Address Phone Number](#101-shipping-address-phone-number-)
      * [10.2 Shipping Address Email](#102-shipping-address-email-)
      * [10.3 Flat-Rate Shipping Methods](#103-flat-rate-shipping-methods-)
      * [10.4 Locker Confirmation Checkout Script](#104-locker-confirmation-checkout-script-)
      * [10.5 Order Confirmation Email Template](#105-order-confirmation-email-template-)
* [Testing the Configuration](#testing-the-configuration-)
    * [1. Prime Checkout](#1-prime-checkout-)
    * [2. Select PUDO Method](#2-select-pudo-method-)
    * [3. Complete PUDO Destination Selection](#3-complete-pudo-destination-selection-)
    * [4. Enter OTP and Confirm](#4-enter-otp-and-confirm-)
<!--te-->

## First Install [🔼](#table-of-contents)

### 1. Install the PUDO App [🔼](#table-of-contents)

Install the PUDO app on your Shopify site by [clicking here](https://apps.shopify.com/pudo-1). Click the "Install" button. If you have multiple Shopify sites linked to your account, select the relevant website first. Once your dashboard appears, click the "Install" button again. After installation, you will be redirected to PUDO settings page.

> ![PUDO Guide](../main/assets/pudo/1-install-the-pudo-app.png)


### 2. Configure General Settings [🔼](#table-of-contents)

Under the "General" tab, fill in **Company Name**, **Account Code** and **Account Key**. The other fields in the general tab are optional.

> ![PUDO Guide](../main/assets/pudo/2-configure-general-settings.png)

### 3. Configure Address Settings [🔼](#table-of-contents)

Expand the "Address" tab and choose a preferred value for the “PUDO Source” dropdown (either Locker or Street Address).

> ![PUDO Guide](../main/assets/pudo/3-configure-address-settings.png)

### 4. Select PUDO Source Locker [🔼](#table-of-contents)

In the “Locker Number” field, select your preferred PUDO source locker. This is required so clients can choose **Locker** -> **Door or Locker** -> **Locker** at checkout.

> ![PUDO Guide](../main/assets/pudo/4-select-pudo-source-locker.png)

### 5. Enter Company Address [🔼](#table-of-contents)

Fill in your **Street Address**, **Suburb**, **City**, **Province**, **Postal Code**. The “Country” field is restricted to “South Africa.”

> ![PUDO Guide](../main/assets/pudo/5-enter-company-address.png)

### 6. Enter Contact Details [🔼](#table-of-contents)

Fill in your **Contact Name**, **Email** and **Phone**.

> ![PUDO Guide](../main/assets/pudo/6-enter-contact-details.png)

### 7. Select Locker Size [🔼](#table-of-contents)

Under the “Lockers” dropdown, choose the locker size that all orders will be restricted to (Extra Small, Small, Medium, Large, Extra Large). You can only have one locker size attached to your Shopify website.

> ![PUDO Guide](../main/assets/pudo/7-select-locker-size.png)

### 8. Optional Settings [🔼](#table-of-contents)

> ![PUDO Guide](../main/assets/pudo/8-optimal-settings.png)

#### 8.1 Add Carrier Rates to Shopify on Save [🔼](#table-of-contents)

Available only for Shopify Advanced Plans. It adds dynamic rates to your shipping.

#### 8.2 Enable PUDO Locker Confirmation [🔼](#table-of-contents)

This notifies the merchant on the submission page whether the customer has selected a locker. Once submitted, the customer's selection is pre-populated on the Submission page.

> ![PUDO Guide](../main/assets/pudo/8-2-enable-pudo-locker-confirmation.png)

### 9. Save Settings [🔼](#table-of-contents)

Click the **Save Settings** button to save your configuration.

> ![PUDO Guide](../main/assets/pudo/9-save-settings.png)

### 10. Finishing Steps [🔼](#table-of-contents)

These finishing steps help to ensure the plugin is configured correctly.

> ![PUDO Guide](../main/assets/pudo/10-finishing-steps.png)

#### 10.1 Shipping Address Phone Number [🔼](#table-of-contents)

Click the notification for **Shipping Address Phone Number** to load a popup with Shopify checkout settings. Ensure that the phone number for shipping addresses is required.
    
> ![PUDO Guide](../main/assets/pudo/10-1-shipping-address-phone-number.png)

#### 10.2 Shipping Address Email [🔼](#table-of-contents)

Ensure that the Customer contact method is set to 'Email'.

> ![PUDO Guide](../main/assets/pudo/10-2-shipping-address-email.png)

#### 10.3 Flat-Rate Shipping Methods [🔼](#table-of-contents)

If you are on a Basic Plan or don't wish to use Carrier Rates, create 2 flat-rate shipping methods for your South African shipping zone, ensuring they include “PUDO Locker” in their names (e.g., PUDO Locker D2D or PUDO Locker to Door).
    
> ![PUDO Guide](../main/assets/pudo/10-3-flat-rate-shipping-methods.png)

#### 10.4 Locker Confirmation Checkout Script [🔼](#table-of-contents)

If **Enable PUDO Locker Confirmation** is checked, go to **Settings** -> **Checkout** and add the following code to the **Order status page additional scripts** field:

```html
<script>
    function getShippingMethodFromOrderDetails() {
      return Shopify.checkout.shipping_rate.handle;
    }
    let selectedShippingMethod = getShippingMethodFromOrderDetails();
    
    if (selectedShippingMethod.includes('PUDO') && selectedShippingMethod.includes('Locker')) {
      const URL = "https://shp.pudo.co.za/otp_confirmation?shop=" + Shopify.shop + "&orderID=" + Shopify.checkout.order_id;
      Shopify.Checkout.OrderStatus.addContentBox('<h2>PUDO Locker Destination</h2>', '<p>Please select your locker destination in the link below: <a href="' + URL + '">Click here</a></p>');
    }
</script>
````

> ![PUDO Guide](../main/assets/pudo/10-4-locker-confirmation-checkout-script.png)

#### 10.5 Order Confirmation Email Template [🔼](#table-of-contents)

If **Enable PUDO Locker Confirmation** is checked, select **Notifications** -> **Customer notifications** -> **Order Confirmation** -> **Edit Code** and paste the code from below the shipping info table (+-line 854 in the unedited template). Save your changes.

````
    {% if shipping_method and shipping_method.handle contains 'PUDO' and shipping_method.handle contains 'Locker' %}
    
      
    {% assign shopName = shop.domain %}
    {% assign orderID = order.id %}
    
    {% capture URL %}
      https://shp.pudo.co.za/otp_confirmation?shop={{ shopName }}&orderID={{ orderID }}
    {% endcapture %}
    
    <p>Please select your locker destination in the link below: <a href="{{ URL }}">Click here</a></p>
    {% endif %}
````

NOTE: For merchants still verifying their sender email, navigate to **Notifications**, click **Resend Verification**, and complete the email verification process.

> ![PUDO Guide](../main/assets/pudo/10-5-order-confirmation-email-template-0.png)
> ![PUDO Guide](../main/assets/pudo/10-5-order-confirmation-email-template.png)

## Testing the Configuration [🔼](#table-of-contents)

### 1. Prime Checkout [🔼](#table-of-contents)

Navigate to the front end of your Shopify store, add a product to your cart and navigate to the Checkout page.

> ![PUDO Guide](../main/assets/pudo/1-prime-checkout.png)

### 2. Select PUDO Method [🔼](#table-of-contents)

Add your shipping address and select the PUDO method (Confirm PUDO Locker on the next page) at checkout. Ensure you have access to the email used at checkout, as it will receive the OTP pin required to submit your shipment.

> ![PUDO Guide](../main/assets/pudo/2-select-pudo-method.png)

### 3. Complete PUDO Destination Selection [🔼](#table-of-contents)

On the Thank You page, navigate to the PUDO Destination Section and click **Click here.**

> ![PUDO Guide](../main/assets/pudo/3-complete-pudo-destination-selection.png)

### 4. Enter OTP and Confirm [🔼](#table-of-contents)

Navigate to your email to retrieve the OTP, enter it, select your Locker destination, and click **Continue**. Alternatively, this process can be done via the order confirmation email.

> ![PUDO Guide](../main/assets/pudo/4-enter-otp-and-confirmation.png)
