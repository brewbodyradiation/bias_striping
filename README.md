# bias_striping
The Wide Field Channel of the Advanced Camera for Surveys (ACS/WFC) on the Hubble Space Telescope (HST) exhibits instrumental noise 
in the form of a striped pattern on 0- second exposure “bias” images. This noise was noticed after Servicing Mission 4 (SM4), where 
the CCD Electronics Box Replacement was installed (CEB-R). The CEB-R contains an Application- Specific Integrated Circuit (ASIC) which 
imparts a low frequency noise which appears to have direct correlation with the striping pattern. This pattern was characterized for 
mitigation in science exposures shortly after its discovery (Grogin et al. 2011, STScI Instrument Science Report ACS-2011-05).

This "hst_proj.py" pipeline is designed to download the raw bias images from the ACS/WFC from the HST archive, subtract the "superbias" 
from the collection of raw biases, approximate the intensity of the striping in each row and clip the intensity outliers, then subtract 
the median of the stripe intensities to convert the unit of bias striping noise to intensitiy. 
