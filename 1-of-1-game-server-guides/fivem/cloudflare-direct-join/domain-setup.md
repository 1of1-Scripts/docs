# Domain Setup

### Step 1: Sign Up for a Cloudflare Account

Create an account at Cloudflare:

🔗 [Sign up here](https://dash.cloudflare.com/sign-up)

***

### Step 2: Get a Domain or Manage Your Current DNS

If you don't have a domain:

* You can order a domain from us.

If you already have a domain:

* Proceed to the next step.

***

### Step 3: Modify Your Current DNS Settings

1. **Log in to the Cloudflare dashboard**:\
   Go to [dash.cloudflare.com](https://dash.cloudflare.com), select your account and domain.
2. **Add a New Site**:
   * Choose the **FREE** plan option when prompted.
   * Follow the guided setup.
3. **Update Nameservers**:
   * On the **Overview** page, copy the two **Cloudflare Nameservers** provided.
   * Replace your domain registrar’s current nameservers with the ones from Cloudflare.
4.  **Disable DNSSEC on Your Registrar's Panel**:

    > ⚠️ _Important: Disable DNSSEC before changing nameservers to avoid downtime._

***

### DNS Propagation

* DNS changes usually take **1–2 hours** to propagate.
* In rare cases, it may take up to **24 hours**.
* Cloudflare will send a confirmation email once your domain is active.

***

### Step 4: Secure Your Domain

Once your domain is active on Cloudflare:

* **Re-enable DNSSEC** within the Cloudflare dashboard to protect against domain spoofing.

***

### You're All Set!

Your DNS is now secured and optimized via Cloudflare.

{% hint style="danger" %}
We do not offer any support other than what is found on this guide. Please do not ask us for any support or open tickets about this, they will be auto closed.&#x20;
{% endhint %}
