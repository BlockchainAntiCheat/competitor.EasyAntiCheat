# competitor.EasyAntiCheat
# in: Singularity Cloud, hypervisor: KVM
sch: https://www.google.com/search?q=steam+%22Cannot+run+under+Virtual+Machine%22 https://www.google.com/search?q=Easy+Anti+Cheat+Cannot+run+under+Virtual+Machine

# Solution:
## smbios mode='host'
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

## Change Computer Name
https://forums.unraid.net/topic/127639-easy-anti-cheat-launch-error-cannot-run-under-virtual-machine/#comment-1206050
>The game for some reason thinks your PC is a VM if the name of your computer name starts with a "DESKTOP" within it's name. For example, DESKTOP-123ABC. To fix it, go to System -> Advanced settings -> Computer Name. Click "Change" and change the "DESKTOP" to something else, like Jamal-PC, etc, and then restart your computer and it will be fixed.
