# 3D-Rotation-and-Projections_

3D Rotation and Projection 
1. Project Overview 
This project presents the visualization of randomly generated 3D point cloud data on a 2D display. 
The application generates points within a three-dimensional coordinate system, applies rotation 
transformations including Yaw, Pitch, and Roll, and projects the transformed points onto a two
dimensional canvas using either Orthographic Projection or Perspective Projection. 
The project provides practical knowledge of computer graphics concepts such as coordinate 
transformations, rotational mathematics, and projection techniques used in 3D visualization. 
2. Workflow of the Project 
1. Generate random 3D points. 
2. Store the generated points in a JSON file. 
3. Load the point data into the visualization application. 
4. Apply Yaw, Pitch, and Roll rotations. 
5. Convert degree values into radians. 
6. Apply Orthographic or Perspective Projection. 
7. Draw the projected points on the HTML canvas. 
8. Continuously update the display to create smooth animation. 
3. Random 3D Point Generation 
The application generates random x, y, and z coordinate values within a predefined range using 
JavaScript. 
Formula 
x = Math.random() * 200 - 100; 
y = Math.random() * 200 - 100; 
z = Math.random() * 200 - 100; 
Example Point: 
(45.2, -23.6, 80.1) 
These coordinates represent the position of each point in the three-dimensional space. 
4. Rotation Techniques Used 
The visualization uses three basic rotation transformations. 
Yaw Rotation (Rotation about Y-axis) 
Rotates the object left or right. 
Formula 
x' = x cos(θ) + z sin(θ) 
z' = -x sin(θ) + z cos(θ) 
Where 
• θ = Yaw angle 
• x', z' = New coordinates 
Pitch Rotation (Rotation about X-axis) 
Rotates the object upward or downward. 
Formula 
y' = y cos(θ) − z sin(θ) 
z' = y sin(θ) + z cos(θ) 
Where 
• θ = Pitch angle 
Roll Rotation (Rotation about Z-axis) 
Rotates the object clockwise or counterclockwise. 
Formula 
x' = x cos(θ) − y sin(θ) 
y' = x sin(θ) + y cos(θ) 
Where 
• θ = Roll angle 
5. Degree-to-Radian Conversion 
JavaScript trigonometric functions require angles in radians. 
Formula 
Radians = Degrees × π / 180 
Example 
90° × π /180 
= π/2 
= 1.5708 radians 
JavaScript Code 
const radians = degrees * Math.PI / 180; 
6. Projection Methods 
Orthographic Projection 
Orthographic projection displays the object without considering depth. 
Formula 
xscreen = x 
yscreen = y 
After Centering 
xscreen = x + canvasWidth / 2 
yscreen = y + canvasHeight / 2 
Characteristics 
• No depth effect 
• Constant object size 
• Suitable for CAD and Engineering drawings 
Perspective Projection 
Perspective projection creates a realistic 3D effect by considering depth. 
Formula 
Scale = D / (D + z) 
Where 
• D = Viewing Distance 
• z = Depth Coordinate 
Projected Coordinates 
xscreen = x × Scale 
yscreen = y × Scale 
Example 
Scale = 400 / (400 + z) 
xscreen = x × Scale 
yscreen = y × Scale 
Characteristics 
• Realistic depth perception 
• Distant objects appear smaller 
• Used in games and computer graphics 
7. Overall Implementation 
The application loads the generated 3D points from the JSON file, applies rotation transformations, 
converts rotation angles into radians, and projects the transformed coordinates onto a 2D canvas. 
The animation loop continuously updates the visualization, allowing users to observe the rotating 
point cloud from different viewing angles. 
8. Result 
The final output displays an interactive 3D Point Cloud Visualization on an HTML canvas. Users can 
rotate the object using Yaw, Pitch, and Roll controls and switch between Orthographic and 
Perspective projection modes. 
9. Output 
The output screen contains: 
• Interactive 3D Point Cloud 
• Yaw Slider 
• Pitch Slider 
• Roll Slider 
• Orthographic Projection 
• Perspective Projection 
• Auto Rotation 
• HTML Canvas Visualization 
10. Conclusion 
This project successfully demonstrates the visualization of three-dimensional point cloud data using This project successfully demonstrates the visualization of three-dimensional point cloud data using rotation transformations and projection techniques. It provides practical knowledge of computer 
graphics concepts and illustrates how mathematical transformations can be used to display 3D 
objects on a 2D screen.
OUTPUT:
<img width="1920" height="1080" alt="Screenshot 2026-07-05 212658" src="https://github.com/user-attachments/assets/5fd0a75d-0b28-4a61-bfee-65cc89fb06ee" />

rotation transformations and projection techniques. It provides practical knowledge of computer 
graphics concepts and illustrates how mathematical transformations can be used to display 3D 
objects on a 2D screen. 
