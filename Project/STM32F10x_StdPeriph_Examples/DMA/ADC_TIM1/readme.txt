/**
  @page DMA_ADC_TIM1 DMA_ADC_TIM1
  
  @verbatim
  ******************** (C) COPYRIGHT 2009 STMicroelectronics *******************
  * @file    DMA/ADC_TIM1/readme.txt 
  * @author  MCD Application Team
  * @version V3.1.0
  * @date    06/19/2009
  * @brief   Description of the DMA ADC1 TIM1 example.
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

This example provides a description of how to use a DMA channel to transfer
continuously a data from a peripheral (ADC1) to another peripheral (TIM1) supporting
DMA transfer.
The ADC channel14 is configured to be converted continuously. TIM1_CH1 is configured
to generate a PWM signal on its output.
The dedicated DMA1 channel5 is configured to transfer in circular mode the last ADC 
channel14 converted value to the TIM1_CCR1 register. The DMA channel request is driven
by the TIM1 update event. The duty cycle of TIM1_CH1 output signal is then changed
each time the input voltage value on ADC channel14 pin is modified.
The duty cycle variation can be visualized on oscilloscope on the TIM1_CH1 pin
PA.08 while changing the analog input on ADC channel14 using the potentiometer.

@par Directory contents 

  - DMA/ADC_TIM1/stm32f10x_conf.h  Library Configuration file
  - DMA/ADC_TIM1/stm32f10x_it.c    Interrupt handlers
  - DMA/ADC_TIM1/stm32f10x_it.h    Interrupt handlers header file
  - DMA/ADC_TIM1/main.c            Main program

@par Hardware and Software environment 

  - This example runs on STM32F10x Connectivity line, High-Density, Medium-Density 
    and Low-Density Devices.
  
  - This example has been tested with STMicroelectronics STM3210C-EVAL (STM32F10x 
    Connectivity line), STM3210E-EVAL (STM32F10x High-Density) and STM3210B-EVAL
    (STM32F10x Medium-Density) evaluation boards and can be easily tailored to
    any other supported device and development board.

  - STM3210C-EVAL Set-up 
    - Connect a variable power supply 0-3.3V to ADC Channel14 mapped on pin 
      PC.04 (potentiometer RV1)
    - Connect an oscilloscope to TIM1_CH1 (PA.08) pin  

  - STM3210E-EVAL Set-up 
    - Connect a variable power supply 0-3.3V to ADC Channel14 mapped on pin 
      PC.04 (potentiometer RV1)
    - Connect an oscilloscope to TIM1_CH1 (PA.08) pin  

  - STM3210B-EVAL Set-up 
    - Connect a variable power supply 0-3.3V to ADC Channel14 mapped on pin 
      PC.04 (potentiometer RV1)
    - Connect an oscilloscope to TIM1_CH1 (PA.08) pin       

@par How to use it ? 

In order to make the program work, you must do the following :
- Create a project and setup all project configuration
- Add the required Library files :
  - stm32f10x_dma.c 
  - stm32f10x_rcc.c 
  - stm32f10x_gpio.c 
  - stm32f10x_adc.c 
  - stm32f10x_tim.c
  - system_stm32f10x.c (under Libraries\CMSIS\Core\CM3)
       
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
