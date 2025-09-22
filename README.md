# MonoCheckout Extension by MaGuru

![Magento 2](https://img.shields.io/badge/Magento-2.4%2B-brightgreen)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-blue)

<img width="150" height="100" src="documentation/images/made_in_ukraine.jpeg">

---

## About Mono Checkout

An express ordering tool for online stores that automatically fills in the buyer's payment and delivery details.

### Who is it for?

Every business that sells physical goods requiring delivery (or pickup) and has the capability for **online payment on the website**.

### How does it work?

There are two options:

*   **Full integration** - All orders are processed through Mono Checkout, and the store doesn't need to set up a separate checkout process on the site.
*   **One of the purchase buttons** - Your customer can choose how to place the order: through the traditional path of entering all data, or use the Mono Checkout button to make an order in a few clicks. The button is added to product pages and in the cart.

<div>
    <figure>
        <img src="https://3547059287-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FDOWL3CIGZNGqYkWbO4hr%2Fuploads%2Fvs91ydsXZpIhUNU7pt98%2FiPhone%2013%20mini%20-%201168.png?alt=media&token=1b20472b-d3b6-4685-b5fb-1e2398b8f13a" alt="Full integration example" width="375">
        <figcaption>Full Integration</figcaption>
    </figure>
    <figure>
        <img src="https://3547059287-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FDOWL3CIGZNGqYkWbO4hr%2Fuploads%2FPz0ETgiy4NVAuZrIvN1p%2FiPhone%2013%20mini%20-%201167.png?alt=media&token=8947c7aa-779d-4b8d-ac47-979ee7217a2e" alt="Button purchase example" width="375">
        <figcaption>One of the purchase buttons</figcaption>
    </figure>
</div>

In each of these options, the subsequent steps from the customer's side will look like this:

#### 1. Authorization

Mono Checkout works for customers of any bank, and at the authorization step, two methods are available:

*   Via the Monobank app (for those who have it)
*   Via phone number (for everyone else)

<figure>
    <img src="https://3547059287-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FDOWL3CIGZNGqYkWbO4hr%2Fuploads%2FjuG5uGVU33NlL0yWKpeG%2F1st%20enter.png?alt=media&token=8290a396-4400-4483-b6b2-9f32c439cfed" alt="Authorization screen" width="188">
    <figcaption>Authorization Step</figcaption>
</figure>

#### 2. Delivery

The seller can add various options - pickup, Nova Poshta mail terminals, Nova Poshta branches, or address delivery.

> ✅ Mono Checkout will suggest the nearest post office branch to the customer, making the order even simpler.

<figure>
    <img src="https://3547059287-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FDOWL3CIGZNGqYkWbO4hr%2Fuploads%2F9HjI1yP0EKKRnq3sO5Oe%2FiPhone%20X.png?alt=media&token=c5318277-9ad5-4105-ad57-9332192ed001" alt="Delivery selection screen" width="188">
    <figcaption>Delivery Selection</figcaption>
</figure>

#### 3. Payment

The seller can add different payment methods for the goods. There are options to pay in full or in parts.

*   Online card payment
*   Payment upon receipt of the order
*   Purchase in Parts by Mono (commission on the seller's side)

<figure>
    <img src="https://3547059287-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FDOWL3CIGZNGqYkWbO4hr%2Fuploads%2FtDGoZX9vqpPjAQ3Wymg1%2FiPhone%20X%20(1).png?alt=media&token=bb4af44a-7ba0-435b-b182-b85eda204cdf" alt="Payment screen" width="188">
    <figcaption>Payment Step</figcaption>
</figure>

#### Age Verification

With Mono Checkout, the seller can add age restrictions to orders. If the goods are not intended for minors, we will verify the buyer's age.

<figure>
    <img src="https://3547059287-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FDOWL3CIGZNGqYkWbO4hr%2Fuploads%2FLKItcBznUEJMEXC5UibR%2F1st%20enter%20(1).png?alt=media&token=141b6d0b-a279-4ced-a05e-5316deda0387" alt="Age verification screen" width="188">
    <figcaption>Age Verification</figcaption>
</figure>

---

## 📚 Documentation

- [Installation Guide](documentation/INSTALLATION.md)
- [Configuration Admin](documentation/CONFIGURATION.md)
- [Usage Guide](documentation/USAGE.md)
- [Rest Api Guide](documentation/API.md)
- [Connecting in mono](https://acquiring.monobank.ua/mono-checkout/pidklyuchennya)

## ⚖️ Legal

- [Privacy Policy](legal/PRIVACY.md)
- [Refund Policy](legal/REFUND.md)
- [Terms of Service](legal/TERMS.md)

## 🧾 License

- [The code is licensed](LICENSE.txt).

## 🆘 Support

- **Email:** maguru.sup@gmail.com
- **Issues:** [GitHub Issues](https://github.com/MaGuruDev/MonoCheckout/issues)

---

> ✅ Note
>> Mono Checkout can be used by customers of any bank.

> ❗ Important
>> Mono Checkout only supports payments in Ukrainian Hryvnia (UAH). If your online store uses a different currency, you must change it to Hryvnia to use mono checkout (and accordingly adjust product prices by setting them in Hryvnia).

> ❗ Important
>> The Mono Checkout button is an alternative to your online store's regular shopping cart. This means that if a customer chooses to create an order using mono checkout, any data entered in the fields of the regular cart will not be taken into account during order placement. 