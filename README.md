# bouteille
4 Thruster ROV with water bottle as water tight compactment  
|Feature|Approach|
|-------|--------|
|DOF|3|
|No. of Thruster|4|
|VIN|12V|
|Protocol|UART|
|Interface|Touch|


HEX ASSignment  
|Action|HEX|GPIO PWM signal|
|------|---|---------------|
|riseFast|aaaaff|8fF 9fF 10sP 11sP|
|riseSlow|aabbff| 8fS 9fS 10sP 11sP|
|sinkFast|aaccff|8rF 9rF 10sP 11sP|
|sinkSlow|aaddff|9rS 9rS 10sP 11sP|
|fwdFast|ccaaff|8sP 9sP 10fF 11fF|
|fwdSlow|ccbbff|8sP 9sP 10fS 11fS|
|revFast|ddaaff|8sP 9sP 10rF 11rF|
|revSlow|ddbbff|8sP 9sP 10rS 11rS|
|turnLeft|bbbbff|8sP 9sP 10fS 11rS|
|turnRight|bbaaff|8sP 9sP 10rS 11fS|
|fullStop|eeeeff||
|clawOpen|eeaaff|12fF|
|clawClose|eebbff|12rF|

*8fF 9rS 10sP 11sP = GP8 fwdFast(PWM1900ms) / GP9 revSlow(PWM1300ms) / GP10 stayPut(PWM1500ms) / GP11 stayPut(PWM 1500ms) 
