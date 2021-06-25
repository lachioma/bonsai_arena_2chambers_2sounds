# bonsai_arena_2chambers_2sounds
Arena with two distinct chambers, each associated to a distinct background sound. Play the background sound when the mouse is inside either chamber.

The two chambers are defined as separate ROIs using the **CropPolygon** node.
When the mouse enters the ROI, the average brightness of the ROI decreases. When the average brightness drops below a threshold (manually set in the **LessThan** node), the sound playback is triggered. The playback is repeated in loop until the brightness goes back above the threshold (== mouse exits the ROI).

**DistinctUntilChanged** node makes propagate the signal only when there is a change, so either a rising edge (0->1) or falling edge (1->0). The distinction between the two edges is then done by the **isTrue** and **isFalse** conditions.


![image](https://user-images.githubusercontent.com/29898879/123437607-daa8a800-d59d-11eb-9f2d-a38dad9322ac.png)


