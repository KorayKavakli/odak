# Visual Perception

:octicons-info-24: Informative

This section of `Computational Light course` introduces various components of human vision system, which plays a critical role in the design of camera, compute and display systems.

## Color Perception

:octicons-info-24: Informative

We can establish an understanding on color perception through studying its physical and perceptual meaning, so we can understand motivations behind display, computer graphic and camera technologies.
Color can be explained in a physical and perceptual capacity. In the physical sense, color is a quantity typically described using a wavelength of light. Humans can only percieve color within a certain range of the electromagnetic spectrum, from around 400 to 700 nanometers. For greater details on the electromagnetic spectrum and concept of wavelength, we recommend revisiting [Light, Computation, and Computational Light](computational_light.md) section of our course. Color is a perceptual phenomenon arising from the human visual system's interaction with light. Color is essentially a "side effect" created by our brain when specific wavelengths of light are emitted, reflected, or transmitted by objects.

The perception of color originates from the absorption of light by photoreceptors in the eye, converting the light into electrical signals to be interpreted by the brain. 

This note will only discuss the role of our eyes; for more information about how brain percieves light, please refer to [this paper](https://pubmed.ncbi.nlm.nih.gov/21841776/)

The photoreceptors where color perception originates are called [rods and cones](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4763127/). Rods, which are relatively more common in the periphery, help people see in low-light conditions, but can only interpret in a greyscale manner. Cones, which are more dense in the fovea, are pivotal in color perception in relatively normal environments. The cones are categorized into three types based on their sensitivity to specific wavelengths of light, corresponding to long (L), medium (M), and short (S) wavelengths. These [three types of cones](https://opg.optica.org/josaa/fulltext.cfm?uri=josaa-31-4-A195&id=279354) allow us to better understand the [trichromatic theory](https://www.jstor.org/stable/82365), which suggests that human color perception stems from combining stimulations of the LMS cones, which correspond to red, green, and blue light, respectively. For example, red is perceived when L cones are significantly stimulated more than the other types, and blue is perceived when S cone activation is more prominent. Scientists have tried to graphically represent how sensitive each type of cone is to different wavelengths of light, which is known as the spectral sensitivity function.

??? question end "Would you like to learn more about LMS?"
       Check out [this paper: B. P. Schmidt, M. Neitz, and J. Neitz, "Neurobiological hypothesis of color appearance and hue perception," J. Opt. Soc. Am. A 31(4), A195–207 (2014)](https://europepmc.org/article/pmc/4167798)! 


<figure markdown>
  ![Image title](media/lms_graph.png){ width="600" }
  <figcaption>Spectral Sensitivities of LMS cones</figcaption>
</figure>

However, the story of color perception deepens with the concept of [color opponency](https://pubmed.ncbi.nlm.nih.gov/1303712/). This theory reveals that our perception of color is not just a matter of additive combinations of primary colors but also involves a dynamic interplay of opposing colors: red versus green, blue versus yellow. This phenomenon is rooted in the neural pathways of the eye and brain, where certain cells are excited or inhibited by specific wavelengths, enhancing our ability to distinguish between subtle shades and contrasts.


### Display Realism (What does it mean to be realistic)

When considering the realism of displays, it is important to define what realism entails in the context of color perception. If we were to have a display, disregarding all cost and engineering challenges, just solely built to be "lifelike", what would we need to achieve? 

To answer this question, we would need to be able to apply the complex principles of human color perception and display technologies.

#### Accurate Reproduction of Colors (or at least perceptible): 
The most important characteristic of a realistic display is to accurately reproduce color. Current display technologies combine three color primaries (Red, Green, Blue) in different intensities attempting to recreate large ranges of color called a color space. It is possible to choose different primary colors, or even the number of primaries to represent one's color space, but its efficacy can be expressed by how vast the resulting color space is. The human color gamut is a collection of all visible human lights, and is currently impossible to represent with only three primaries. Because the gamut is continuous and infinite, you would need an infinite amount of primaries to represent all colors.

Fortunately, one promising solution is the use of *metamers*— applying different combinations of wavelengths that produce the same color perception in the human eye. This means two separate colors can elicit the same LMS cone response as each other. This allows displays to recreate a vast range of colors on a limited set of primaries.

[Code](https://gulpinhenry.github.io/PrismaFoveate/optimize_primaries.html) on how to optimize display primaries with a color space


#### Accounting for Photopic vs Scotopic vision
Human perception is extremely context dependent, where we need to adapt to various lighting conditions like low-light (scotopic) and lit (photopic) scenes. Displays must be able to figure out how to preserve the rod and cone functionality under all these different environments.


#### Chromaticity + Brightness
<!-- TODO: add some more stuff here -->



### Conclusion
As we dive deeper into light and color perception, it becomes evident that the task of replicating the natural spectrum of colors in technology is still an evolving journey. This exploration into the nature of color sets the stage for a deeper examination of how our biological systems perceive color and how technology strives to emulate that perception.


## Color Science
[Biomimetic Eye Modeling & Deep Neuromuscular Oculomotor Control](https://www.andrew.cmu.edu/user/aslakshm/pdfs/siggraph19_eye.pdf)

