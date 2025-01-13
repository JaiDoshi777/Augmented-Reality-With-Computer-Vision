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
