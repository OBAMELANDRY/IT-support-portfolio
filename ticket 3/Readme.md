# INC6157073 – No Internet Access

**Platform:** SysDesks (help desk simulator)
**Category:** Network > Connectivity | **Priority:** P3 Moderate | **Level:** Service Desk Tier 1
**SLA Note:** Ticket was already past its SLA deadline upon pickup.

## Reported Issue
Jordan Reyes is unable to access the Internet; websites are not loading.

## Diagnostic Steps
1. Reviewed the ticket and user communications.
2. Accessed workstation NL-LPT-0447.
3. Renewed DHCP lease: `ipconfig /release` followed by `ipconfig /renew`
   (result: "DHCP lease renewed successfully").
4. Flushed DNS cache: `ipconfig /flushdns`.
5. Connectivity tests:
   - `ping 127.0.0.1`: 100% packet loss. (Note: This local test normally
     responds on a real workstation; this is a limitation of the simulated environment);
   - `ping 8.8.8.8`: 4/4 replies, 0% loss; Internet is reachable.
6. Contacted Jordan via chat to verify the outcome.

## Cause
Outdated network configuration (DHCP lease and/or DNS cache) on the workstation.

## Resolution
- IP renewed and DNS cache flushed.
- Jordan confirmed that the network icon indicates Internet access and
  web pages are loading normally.
- Ticket closed with the code "Solved (Permanently)."

## Demonstrated Skills
Network diagnostic methodology (working from nearest to furthest point),
`ipconfig` and `ping` commands, DHCP/DNS concepts, result interpretation,
and communication/verification with the user prior to closure. ## Screenshots
![Ticket](screenshots/01-ticket.png)
![Diagnostic](screenshots/02-commands.png)
![User confirmation](screenshots/03-chat.png)
![Ticket closed](screenshots/04-completed.png)
