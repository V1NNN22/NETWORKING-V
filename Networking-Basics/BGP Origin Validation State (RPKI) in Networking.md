---

# BGP Origin Validation State (RPKI) in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is BGP Origin Validation State?  
- **Definition:** BGP Origin Validation is a security mechanism that uses Resource Public Key Infrastructure (RPKI) to verify whether an Autonomous System (AS) is authorized to originate a particular IP prefix.
- **Purpose:** It helps prevent accidental or malicious BGP route hijacking by checking advertised prefixes against cryptographically signed Route Origin Authorizations (ROAs).
- **Analogy:** Imagine a company checking an official authorization certificate before allowing someone to claim ownership of a property.

---  

## The 4 Core Steps of BGP Origin Validation  

### 1. Create Route Origin Authorization (ROA)  
- **Function:** An IP address holder publishes a ROA specifying which AS is authorized to originate a prefix and the maximum permitted prefix length.
- **Role:** Establishes the authorized origin information.
- **Examples:** A ROA authorizes AS `65001` to originate `203.0.113.0/24`.

---  

### 2. Validate RPKI Data  
- **Function:** A router or validator obtains and verifies RPKI data, including ROAs, through the RPKI validation process.
- **Role:** Checks the cryptographic validity of the authorization information.
- **Examples:** A validator confirms that a ROA is correctly signed and issued by the appropriate resource holder.

---  

### 3. Check the BGP Route  
- **Function:** The router compares the BGP route's prefix and origin AS with the validated ROA information.
- **Role:** Determines whether the route is authorized by the published ROAs.
- **Examples:** A route for `203.0.113.0/24` originated by AS `65001` matches the authorization.

---  

### 4. Assign Validation State  
- **Function:** The router assigns one of three origin validation states to the route.
- **Role:** Allows routing policy to treat routes differently based on authorization status.
- **Examples:**
  - **Valid:** The route matches an applicable ROA.
  - **Invalid:** An applicable ROA exists, but the route violates its origin AS or maximum prefix length.
  - **NotFound:** No applicable ROA exists.

---  

## Key Features  
- **Cryptographic Authorization:** Uses digitally signed ROAs.
- **Three Validation States:** Valid, Invalid, and NotFound.
- **Prefix-Length Checking:** Verifies whether the advertised prefix length is permitted.
- **Policy Integration:** Routers can reject or deprioritize Invalid routes through routing policy.
- **Origin Protection:** Helps detect unauthorized route-origin announcements.

---  

## Why It Matters  
- **Prevents Route Hijacking:** Helps identify unauthorized BGP origin announcements.
- **Improves Routing Security:** Adds an authorization check to BGP route selection.
- **Reduces Accidental Misconfiguration:** Helps detect incorrect origin AS announcements.
- **Supports Internet Stability:** Encourages more trustworthy global routing.

**Important:** RPKI origin validation checks the originating AS, not the entire AS-PATH. It does not prevent every form of BGP hijacking or route leak.

---  

## Quick Recap (Mnemonic)  
- **Authorize → Validate → Compare → Classify**  
  - **Create ROA → Verify RPKI data → Check BGP announcement → Assign validation state**  

---  


# THANK YOU!  
# ~ **V1NNN22**