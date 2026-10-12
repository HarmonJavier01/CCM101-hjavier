cat > security-audit-report.md <<'EOF'
# Security Audit Report

## Principle of Least Privilege (PoLP)
PoLP means a user or service should only get the access it needs and nothing extra. In the cloud this matters because if an account gets hacked or someone makes a mistake, the damage stays small.

## Attack Surface
The attack surface of a VM is everything an attacker could try to get into, like open ports, running services, and user accounts. The more of these are exposed, the more chances there are to find a weak spot, so I should keep only what is needed.

## Default Deny Policy
Default deny blocks all traffic unless I specifically allow it. It is safer than blocking hackers one by one because attackers can change IP addresses easily and I would never finish the block list. With default deny, anything I did not approve is rejected automatically.
EOF