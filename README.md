# 21.5" iMac to Monitor Conversion
Converting a 21.5" iMac that doesn't work anymore into an external monitor while keeping the
aesthetics and functionality intact.

[TODO! image & caption for finished project]

**Read the guide before attempting anything**

## Teardown of the iMac
You can follow the instructions of iFixit's teardowns such as the [iMac Intel 21.5" EMC 2428 Mid
2011](https://www.ifixit.com/Teardown/iMac+Intel+21.5-Inch+EMC+2428+Teardown/5485) to learn how to
prepare the monitor, this teardown is the closest to the model that is used in this project which
is a 21.5" iMac 1311 which was released late 2009, mid 2010 and mid 2011.

![Completed teardown of iMac showing OEM parts the project will re-use](img/teardown.png)
*After the teardown of the project was completed, OEM parts were decided to be kept based on
wanting to reuse as much as possible and keeping the aesthetic of the iMac's look. This includes
the power delivery cables, speakers, LCD panel, glass panel, chassis and possibly reusing the disc
drive and SD card slots.*

### **Read this!**
The teardown is needed to find what type of panel is being used in the iMac so the approaiate HDMI
controller can be purchased. The sticker on the back of the panel will show this:

![Label on the back of the panel from the project highlighted in yellow](img/panel_label.png)
*The label on the back of the panel has been highlighted in yellow, the image shows that the panel
regarding this project is an LG LM215WF3-SDC2. The information can be used to find a HDMI
controller board that will translate HDMI signal to the display panel.*

## Equipment, hardware & materials
### Equipment
- [Precision screwdriver kit](https://www.ifixit.com/en-au/products/mako-driver-kit-64-precision-bits)
- [Suction cups](https://www.ifixit.com/products/heavy-duty-suction-cups-pair)
- [Opening and prying kit](https://www.ifixit.com/en-au/products/prying-and-opening-tool-assortment)
- [Wire cutters](https://www.amazon.com.au/dp/B003EICAUS/?coliid=I1RJDNN308335&colid=14X3I2WPO7TMI&ref_=list_c_wl_lv_ov_lig_dp_it&th=1)
- [Wire strippers](https://www.amazon.com.au/dp/B09V1ZG2QB/?coliid=I3BA364UGTTKVA&colid=14X3I2WPO7TMI&psc=1&ref_=list_c_wl_lv_ov_lig_dp_it)

### Hardware
- [21.5" iMac 1311 LM215WF3-SDC2 HDMI Controller](https://www.aliexpress.com/item/1005005231652690.html?spm=a2g0o.order_list.order_list_main.53.7eea1802QVjeaj)
- [Speaker crossover for iMac 1311](https://www.aliexpress.com/item/1005012003234698.html?spm=a2g0o.order_list.order_list_main.47.7eea1802QVjeaj)
- [Meanwell LRS-100-12 Switching Power Supply](https://www.aliexpress.com/item/1005007287646072.html?spm=a2g0o.order_list.order_list_main.17.7eea1802QVjeaj)
- [Fan tempature controller DC 12V](https://www.aliexpress.com/item/1005007561332409.html?spm=a2g0o.order_list.order_list_main.5.7eea1802QVjeaj) 

### Materials
- Kapton tape
- Double sided tape
- [Insulated copper wire 4mm<sup>2</sup>](https://www.bunnings.com.au/deta-5m-1-5mm-earth-single-insulated-cable_p0760616?store=8199&gclsrc=aw.ds&gad_source=1&gad_campaignid=23536369919&gbraid=0AAAAADtbEB8QEOTxCLM00H_oIlhemE8ay&gclid=Cj0KCQjwlqTRBhCBARIsANrkrxjGDfaCJAvMGN44jW4C7daOmCjXGYtUSTPutc6Yl6-hUiGVq3aaDiAaAuKEEALw_wcB) 
- Electrical tape
- End terminal rated at minimum 10A

## Salvaging OEM parts
### OEM power cabling
Keeping the OEM power cabling was important as other projects will remove sections of the chassis
to help with cabling, this project is based on the aesthetic of the iMac so salvaging the OEM power
delivery cables was the reason for this decision.

The solution is to use a switching power supply that will convert the power coming from mains into
the needed voltage (V) and current (A) to drive the HDMI controller board as well as any of boards 
that will reuse the OEM parts that are to be salvaged in the project.

![Location of OEM power cables highlighted in yellow](img/power_cable_highlighted.png)
*The location of the OEM power cables is highlighted in yellow, it shows that the 3 wire mains has
been split into a connector that uses live and neutral wiring and a ground wire with a terminal end
that has been secured to an earthing lug within the iMac's chassis.*

The switching power supply chosen was the Meanwell LRS-100-12, it was chosen because the HDMI
controller board requires 12V DC input for power as well as the fan controller also needs the same
12V DC.

![Label of the Meanwell LRS-100-12 with specs highlighted](img/switching_power_supply_label.png)
*Label of the Meanwell LRS-100-12 with the speciciations highlighted in yellow which says that the
switching power supply can take an input range of 100-240V at a frequency of 50/60 Hz from the
grid and will output 12V DC with 8.5A current.*

**When performing this next task make sure the correct wires are attached to the correct terminal,
handling the power supply is dangerous, TAKE NOTICE, the live (L) and neutral (N) wire connector
needs to be snipped, stripped and attached to the switching power supply correctly. Wrap kapton
tape around the live wire before snipping.**

The iMac's power supply has the connector for the iMac's power cable that needs to be salvaged:
![Power supply and switching power supply showing the power cable delivery connector](img/power_supply_and_switching_power_supply.png)
*The power cable connector from the iMac's power supply are snipped from the PCB and stripped
enough for the bare wire to be wrapped around the terminal screw*

![Switching power supply taped up](img/switching_power_supply_taped.png)
*Kapton tape was used to cover the metal to reduce contact with iMac chassis and doubled-sided tape
will be used to attach it*

An electrical earth needs to be added and attached to the metal case as grounding which will be
secured with terminal end that can handle the temperature of mains ampere while also being attached 
to the ground terminal of the switching power supply.

![Project showing the final placement and attachments of the power delivery using the switching
power supply](img/switching_power_supply_installed.png)
*Earth wire was stripped on both ends with bare wire being screwed into the ground terminal
location on the switching power supply and a terminal end (you can crimp using wire stripper tip) 
was attached to the other side to be screwed into the grounding lug of the chassis*

![Earth wire wrapped in electrical wire on terminal end](img/earth_wire_wrapped.png)
*Earth wire on the terminal end is wrapped with electrical tape, you could use heatshrink wrap
instead*

### iMac speakers
Keeping the 

### iMac panel

### Future considerations
