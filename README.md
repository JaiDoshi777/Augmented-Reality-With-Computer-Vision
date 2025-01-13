# Augmented-Reality-With-Computer-Vision
The primary objective was to implement a seamless overlay of a 2D image (poster) onto various wall images using ArUco markers.

The project "Augmented Reality with Computer Vision" focuses on overlaying a 2D poster onto images of walls, aligning with their 3D perspective and placement using advanced computer vision techniques.

These markers, detectable via OpenCV's CV2 library, help compute precise 3D placements and transformations for the poster. By leveraging the geometric properties of the markers and a perspective transform matrix, the team achieved accurate alignment between the wall’s perspective and the overlaid poster.

**Methodology**
The process began with importing the base images (wall images and poster) and calculating their corner coordinates. The poster was further divided into smaller segments for detailed alignment and stored for subsequent transformation. ArUco markers were detected using OpenCV functions, which provided their corner coordinates and associated marker IDs. These coordinates facilitated generating a perspective transformation matrix to align the poster's angle with that of the wall.

The alignment process involved transforming the poster's coordinates using the perspective matrix and projecting it onto the wall image. Binary masking and bitwise operations were employed to blend the transformed poster into the wall image seamlessly. This ensured that the poster adopted the wall’s perspective and appeared as a natural extension of the scene.

**Geometric Calculations**
Critical geometric operations included scaling the poster, identifying the center points, and precisely aligning the transformed poster with the ArUco marker. These calculations played a pivotal role in ensuring realistic overlays. The team utilized various OpenCV functions like cv.warpPerspective for transformation and cv2.fillPoly for masking.

**Results and Evaluation**
The results showcased varying degrees of alignment accuracy across different images. While the algorithm performed well in several cases, aligning both vertically and horizontally with wall lines and reference bars, some instances revealed minor inaccuracies due to issues such as marker detection errors or scaling variations. These discrepancies highlighted areas for potential refinement in the algorithm.

**Conclusion**
The project successfully demonstrated the integration of augmented reality with computer vision, particularly in achieving perspective-aligned overlays. The team gained valuable insights into OpenCV's capabilities and the challenges associated with precise marker-based transformations. Future improvements could focus on enhancing marker detection accuracy and refining scaling operations to achieve consistently precise results across diverse scenarios.


![image](https://github.com/user-attachments/assets/957242ed-b869-4be4-877b-237383dae4c1)
![image](https://github.com/user-attachments/assets/21222817-7603-404c-a5ce-65a3a7552011)
![image](https://github.com/user-attachments/assets/08cf1998-ac40-400e-8add-d2134f230f0c)
![image](https://github.com/user-attachments/assets/2149d525-4d80-4212-825d-04b405c0ec51)
![image](https://github.com/user-attachments/assets/1936d2b3-8518-44e6-a502-bf1bb50a9738)
![image](https://github.com/user-attachments/assets/4d5d323c-92dc-44f9-81e6-b210088ca959)
![image](https://github.com/user-attachments/assets/e7665aec-8160-448c-8f77-0390cd249719)
![image](https://github.com/user-attachments/assets/6abaa031-64a9-46ee-aca0-5b8c8e522f83)
![image](https://github.com/user-attachments/assets/d54a06d8-d8c8-4402-a8ba-294c7464e2dc)
![image](https://github.com/user-attachments/assets/3e77cee7-338f-4c97-b0d5-3d76b705a0ed)

