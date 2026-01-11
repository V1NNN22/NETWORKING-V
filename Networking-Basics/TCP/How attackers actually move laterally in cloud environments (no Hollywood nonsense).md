# ❓ How Attackers Actually Move Laterally in Cloud Environments  
*(no Hollywood nonsense)*

## Written By: VINOD RATHOD 

**Short answer:**  
Attackers don’t “hack around”.  
They **walk forward using permissions you already gave them**.

No hoodies.  
No green text.  
Just IAM abuse with confidence.

---

## 🧱 The Fantasy vs Reality Gap

**Fantasy:**

- Exploit
- Root shell
- Pivot
- Hackerman montage

**Reality:**

- Stolen credential
- Legit API calls
- Quiet expansion
- Weeks of undetected access

Cloud lateral movement is **bureaucratic**, not cinematic.

---

## ☁️ Why Lateral Movement Is Easier in Cloud

Because cloud is:

- API-driven  
- Identity-based  
- Over-permissioned  
- Poorly observed  

Once an attacker gets **any identity**, the cloud helps them politely.

---

## 🧠 The Real Attacker Playbook (Step by Step)

### 1️⃣ Initial Foothold (Boring but Effective)

Usually via:

- SSRF  
- Exposed API key  
- Leaked CI token  
- Compromised pod  

No zero-day required.  
Just **one mistake**.

---

### 2️⃣ Identity Discovery

First questions attacker asks:

- “Who am I?”  
- “What can I do?”

They query:

- IAM permissions  
- Metadata endpoints  
- Token scopes  

In Kubernetes:

- Read service account token  
- Call Kubernetes API  

If discovery is allowed, movement begins.

---

### 3️⃣ Permission Expansion (The Quiet Step)

They look for:

- `iam:PassRole`  
- `CreateRole`  
- `AttachPolicy`  
- Overly broad roles  

In cloud IAM:

- AWS IAM  
- Google Cloud IAM  

If one identity can create or modify another, **escalation is inevitable**.

---

### 4️⃣ Lateral Pivot via Services

Attackers don’t jump **hosts**.  
They pivot **services**.

Examples:

- Compromised app → access database  
- Compromised CI → deploy new workload  
- Compromised pod → list secrets  

Internal trust does the work for them.

---

### 5️⃣ Persistence (This Is the Scary Part)

They:

- Create new roles  
- Add new service accounts  
- Deploy backdoor workloads  
- Generate long-lived keys  

Even if you rotate original credentials, attacker stays.

Most teams **never check for this**.

---

## 🚨 Why Network Controls Barely Matter Here

Because:

- Traffic is encrypted  
- Calls are “legitimate”  
- APIs allow it  
- Firewall sees nothing wrong  

Firewall says:

> “Allowed traffic”

IAM says:

> “Allowed action”

Guess which one matters.

---

## 🔐 What Actually Stops Lateral Movement

### 1️⃣ Brutal Least Privilege

If identity **can’t**:

- List roles  
- Read secrets  
- Create resources  

Attacker hits a wall early.

Annoying? Yes.  
Effective? Also yes.

---

### 2️⃣ Identity Isolation

One workload = one identity.

Not:

- Shared roles  
- Shared service accounts  
- Shared tokens  

Attribution matters **after** compromise.

---

### 3️⃣ Default-Deny Internal Traffic

In Kubernetes:

- NetworkPolicies  
- mTLS  

Service meshes help:

- Istio  

If services can’t talk freely, attackers can’t stroll.

---

### 4️⃣ Observability on IAM Actions

You must alert on:

- New roles  
- Permission changes  
- Token creation  
- Service account abuse  

Without this, lateral movement looks like normal operations.

---

## 🧪 Real-World Pattern (Seen Too Often)

- Initial breach: small  
- Lateral movement: massive  
- Detection: late  
- Damage: everywhere  

Teams fix the first bug.  
Attackers already left breadcrumbs in IAM.

---

## 🚨 Hard Truth (Again, Deserved)

If you think:

- “They got in, but limited damage”  
- “Only one service was affected”  

And you **didn’t audit IAM changes**,  
you’re guessing.

Attackers don’t need speed.  
They need patience.

Cloud gives them both.

---

## ~ V1NNN22 ~
## THANKYOU! 