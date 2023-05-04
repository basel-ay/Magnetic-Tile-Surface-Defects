# magnetic-tiles-defect

Surface defect detection is a core process of filtering unqualified products, however, the procedure can rarely be finished automatically. It is recorded that almost three-quarters of workers are employed to inspect product quality at the magnetic tile factories in Zhejiang Province, China, the largest magnetic tile production base in the world. To relieve human labor, many image processing techniques have been proposed to attempt such examination tasks. There have been several bottlenecks presented in the automatic damage detection for magnetic tiles, including the complexity of texture, the variety of defect shape, and the randomness of illumination conditions on magnetic tiles. The target defects such as blowhole, crack, break, fray are shown in Figure below:

![image](https://user-images.githubusercontent.com/64821137/236259068-8936244d-790c-4777-bc97-5d928308afb5.png)

### The dataset is described in detail here: 
https://www.researchgate.net/profile/Congying-Qiu/publication/327701995_Saliency_defect_detection_of_magnetic_tiles/links/5b9fd1bd45851574f7d25019/Saliency-defect-detection-of-magnetic-tiles.pdf

### The dataset itself is hosted in this repository:
[https://github.com/abin24/Magnetic-tile-defect-datasets.](https://github.com/abin24/Magnetic-tile-defect-datasets.)

### This project contains two components:
1. training of image segmentation model using pipelines
2. web API that calls the above model on a provided image and responds with a binary segmentation mask

Here's the pipeline:
```
                               +----------------+                         
                               | check_packages |                         
                          *****+----------------+*****                    
                     *****        *          **       ******              
               ******          ***             **           *****         
            ***               *                  **              ******   
+-----------+               **                     *                   ***
| data_load |             **                       *                     *
+-----------+           **                         *                     *
           ***        **                           *                     *
              *     **                             *                     *
               **  *                               *                     *
          +------------+                           *                     *
          | data_split |***                        *                     *
          +------------+   *****                   *                     *
                  *             *******            *                     *
                  *                    *****       *                     *
                  *                         ****   *                     *
                  **                          +-------+                ***
                    ****                      | train |          ******   
                        ****                  +-------+     *****         
                            ***              **       ******              
                               ****        **   ******                    
                                   **     *  ***                          
                                  +----------+                            
                                  | evaluate |                            
                                  +----------+
```             
