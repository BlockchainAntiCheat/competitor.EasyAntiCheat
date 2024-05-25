# competitor.EasyAntiCheat
# in: Singularity Cloud, hypervisor: KVM
sch: https://www.google.com/search?q=steam+%22Cannot+run+under+Virtual+Machine%22 https://www.google.com/search?q=Easy+Anti+Cheat+Cannot+run+under+Virtual+Machine

## Solution:
https://forums.unraid.net/topic/127639-easy-anti-cheat-launch-error-cannot-run-under-virtual-machine/

>after a ton of research i have figured it out.
>
>under <os> put
>```
><smbios mode='host'/>
>```
>directly below that put this under <features>
>```
><kvm> 
>  <hidden state='on'/> 
></kvm>
>```
>under <cpu mode ='host-passthrough'....... put
>```
><feature policy='disable' name='hypervisor'/>
>```
>and i also deleted any lines pertaining to hyper-v
