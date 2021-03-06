/**
  @page CortexM3_Mode_Privilege CortexM3_Mode_Privilege
  
  @verbatim
  ******************** (C) COPYRIGHT 2009 STMicroelectronics *******************
  * @file    CortexM3/Mode_Privilege/readme.txt 
  * @author  MCD Application Team
  * @version V3.1.0
  * @date    06/19/2009
  * @brief   Description of the CortexM3 Mode_Privilege Example.
  ******************************************************************************
  * THE PRESENT FIRMWARE WHICH IS FOR GUIDANCE ONLY AIMS AT PROVIDING CUSTOMERS
  * WITH CODING INFORMATION REGARDING THEIR PRODUCTS IN ORDER FOR THEM TO SAVE
  * TIME. AS A RESULT, STMICROELECTRONICS SHALL NOT BE HELD LIABLE FOR ANY
  * DIRECT, INDIRECT OR CONSEQUENTIAL DAMAGES WITH RESPECT TO ANY CLAIMS ARISING
  * FROM THE CONTENT OF SUCH FIRMWARE AND/OR THE USE MADE BY CUSTOMERS OF THE
  * CODING INFORMATION CONTAINED HEREIN IN CONNECTION WITH THEIR PRODUCTS.
  ******************************************************************************
   @endverbatim

@par Example Description 

This example shows how to modify CortexM3 Thread mode privilege access and stack.
CortexM3 Thread mode is entered on Reset, and can be entered as a result of an
exception return.  

The associated program is used to:

1. Switch the Thread mode stack from Main stack to Process stack

2. Switch the Thread mode from Privileged to Unprivileged

3. Switch the Thread mode from Unprivileged back to Privileged

To monitor the stack used and the privileged or unprivileged access level of code
in Thread mode, a set of variables is available within the program. It is also
possible to use the 'Cortex register' window of the debugger.

@par Directory contents 

  - CortexM3/Mode_Privilege/stm32f10x_conf.h  Library Configuration file
  - CortexM3/Mode_Privilege/stm32f10x_it.c    Interrupt handlers
  - CortexM3/Mode_Privilege/stm32f10x_it.h    Header for stm32f10x_it.c
  - CortexM3/Mode_Privilege/main.c            Main program

@par Hardware and Software environment 

  - This example runs on STM32F10x Connectivity line, High-Density, Medium-Density 
    and Low-Density Devices.
  
  - This example has been tested with STMicroelectronics STM3210C-EVAL (STM32F10x 
    Connectivity line), STM3210E-EVAL (STM32F10x High-Density) and STM3210B-EVAL
    (STM32F10x Medium-Density) evaluation boards and can be easily tailored to
    any other supported device and development board.
    
@par How to use it ? 

In order to make the program work, you must do the following :
- Create a project and setup all project configuration
- Add the required Library files :
  - system_stm32f10x.c (under Libraries\CMSIS\Core\CM3)
   - core_cm3.c (under Libraries\CMSIS\Core\CM3)
    
- Edit stm32f10x.h file to select the device you are working on.
  
@b Tip: You can tailor the provided project template to run this example, for 
        more details please refer to "stm32f10x_stdperiph_lib_um.chm" user 
        manual; select "Peripheral Examples" then follow the instructions 
        provided in "How to proceed" section.   
- Link all compiled files and load your image into target memory
- Run the example

@note
 - Low-density devices are STM32F101xx and STM32F103xx microcontrollers where
   the Flash memory density ranges between 16 and 32 Kbytes.
 - Medium-density devices are STM32F101xx and STM32F103xx microcontrollers where
   the Flash memory density ranges between 32 and 128 Kbytes.
 - High-density devices are STM32F101xx and STM32F103xx microcontrollers where
   the Flash memory density ranges between 256 and 512 Kbytes.
 - Connectivity line devices are STM32F105xx and STM32F107xx microcontrollers.
    
 * <h3><center>&copy; COPYRIGHT 2009 STMicroelectronics</center></h3>
 */
