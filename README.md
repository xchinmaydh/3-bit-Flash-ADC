# 3-bit-Flash-ADC
This project implements a 3 bit flash ADC using Inverter Threshold Comparator technique, which reduces the overall area drastically and does not require any bias voltages.

# Tools and Technology Used
The work is carried out in Cadence Tools, namely
1. Virtuoso Schematic Editor
2. Virtuoso Layout XL
3. MMSIM Spectre
4. Quantus QRC
5. Assura Verification

The whole architecture was implemented in gpdk180 technology node.

# Specifications

1. Supply voltage of 1.2 V
2. Uniform 8 state quantizer, implying delta of 0.15 V
3. Sampling rate of 10 MHz
   
# Design Flow

Initially 7 inverters were designed for the reference voltages, ranging from 0.15 V to 1.05 V
![vtc](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/afd463a2-ed64-4573-a066-238270021183)
![comp_schematic](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/089332ee-eae5-45a4-b3b9-f08e621f21d9)


A multiplexer based 8:3 encoder was designed (active low) which can directly convert active low outputs of inverter chain to active high ADC-output bits.
![enc_sch](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/1eb04f03-5c72-408f-8fcc-c4ba5481a94f)

Both the designs were integrated and simulation was carried out.
![combine](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/f35b3f99-7266-4eed-a11c-7774d3738735)

The layout for both these blocks were made and RC extraction was done
![comp_layout](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/05d7e94d-c57e-4601-abab-f4a5d9675a07)
![enc_layout](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/19811d79-8561-48f3-989c-a3c0eeb7b047)

Post layout simulation was carried out.


# Results

Post layout results are as follows :
![output2](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/c6e706fc-b714-413f-8dc1-3104f281df1d)
![output_post](https://github.com/xchinmaydh/3-bit-Flash-ADC/assets/153248450/eeba7559-c394-4fa8-8ad3-205e4ad9ae31)






