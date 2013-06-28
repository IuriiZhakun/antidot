antidot
=======

1) Recognize AHERO
   1) Use SURF (becuase it's scale/rotation invariant) 
      http://achuwilson.wordpress.com/2011/08/05/object-detection-using-surf-in-opencv-part-1/
      If it's slow, use CUDA version http://www.d2.mpi-inf.mpg.de/surf
      
2.1) Implement strategy for jungler.
     1) Use Prophet, because he can teleport easily.
        1) Implement 'select' AHERO
     2) Store forest creep locations (relative cooredinates from 'mini' map)
     3) Define a sequence of visits
     4) Implement upgrades
     5) Define upgrades strategy
     6) Do 'shopping' manually
     7) Go and 'visit' forest creeps until stopped
        1) Forest fight (go if enough mp (tp + raise tree) and enough hp > 50%)
           0) detect mp
           1) raise trees
              1) select 1 mag
              2) select tree
              3) apply
           2) select trees
              1) recognize trees
           3) attack forest creep using trees
              1) recognize forest creep
           4) select AHERO
           5) attack the same forest creep
           6) if hp is low < 30%, then escape
              1) if mp enough, tp base, else walk base
              
2) Make large map image:
   1) Use stitching http://ramsrigoutham.com/2012/11/22/panorama-image-stitching-in-opencv/   
   
3) Track AHERO
   1) Map AHERO movement in the image map(1). 
   2) Store using relative coordinates from micro ('mini') map.
4) Make 'road'(aka pathes) map
   1) Merge AHERO movements using some threshold
5) Match location
   1) From current screen image, find corresponding image in the map
   2) Find a position in the 'road' map
   3) 'Log' (print accesable regions) from current screen image

   
antidot
