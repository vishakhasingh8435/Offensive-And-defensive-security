# Experiment 9: Hydra Password Guessing

## Aim

To perform a controlled password-guessing demonstration using Hydra in an authorized lab environment and to document the observed results through screenshots.

## Scope and Safety

This experiment was carried out only in a lab setup with consent and proper authorization. Hydra is a powerful password-cracking tool and must be used only against systems that the tester owns or has explicit permission to assess. The screenshots included below are evidence of the lab activity and should be used only for educational and authorized security-practice purposes.

## Requirements

- Kali Linux / Linux-based penetration testing system
- Hydra installed
- A target host or service in a lab environment
- Wordlist or username/password list
- A terminal for command execution

## Procedure

### Step 1: Launch Hydra against the target service

The first screenshot shows Hydra being executed from the terminal with the target service configured. The command is used to test authentication attempts against the lab target in a controlled environment.

![Hydra command launched in the terminal](<experiment9(hydra)/screenshot/Screenshot 2026-11-15 185221.png>)

### Step 2: Attempt password guessing

The second screenshot shows the authentication attempts being processed by Hydra. It records the tool trying multiple credentials against the target service, which is the core step in password guessing.

![Hydra attempting login combinations against the target](<experiment9(hydra)/screenshot/Screenshot 2026-11-15 185319.png>)

### Step 3: Confirm the successful login result

The third screenshot captures the successful result returned by Hydra. This confirms that a valid credential pair was found during the authorized lab exercise.

![Hydra result showing the recovered valid credentials](<experiment9(hydra)/screenshot/Screenshot 2026-11-15 185337.png>)

## Result

The lab demonstrated the use of Hydra to test a target service using a list of possible credentials. The screenshots show the execution flow from the command launch to the successful login attempt. The key observation is that Hydra successfully identified a valid username/password pair in the controlled lab environment.

## Conclusion

This experiment helped understand the workflow and impact of password guessing tools like Hydra. It also highlighted the importance of strong authentication, password policies, layered security controls, and ethical use of security-testing tools. Hydra should only be used in authorized, isolated lab environments and never against systems without permission.