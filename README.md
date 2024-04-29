This project was developed using the modern OpenGL API, supplemented by libraries such as GLFW, GLAD, and GLM, to render a scene. The final outcome of this scene consists of multiple simple and complex objects with elaborate textures that attempt to capture the natural look of these objects in the real world. These objects are a tabletop, a stack of three books, a cup filled with coffee, and a block of Swiss cheese. 
Admittedly, OpenGL is a very difficult subject. The process of setting up various buffer objects and programming shader programs to display the camera, models, projects, textures, and lights using complex mathematics is an arduous task. Especially since even calling a function in the wrong order can lead to undefined behavior. As such, lots of trial and error was utilized during the development of this project. The objects displayed were selected due to their relative simplicity given the pre-defined meshes. The most complex object is the coffee scene. Here, we simulate the coffee using the base of an inverted cone, where the remaining mesh is hidden by the body of the cup.  
Adding to the realism of this scene, we have assigned all these objects with lighting properties such as ambient, diffuse, and specular color, and shininess, to name a few, that describe how the object should look with light or in the absence of. Using various vector mathematical operations, the lighting properties of the objects and the sources of light, we are able to calculate the final color of the fragments to present a scene that obeys the Phong lighting model.
In addition, this OpenGL application also allows users to navigate around the scene using mouse and keyboard input. Specifically, users can press W, S, A, and D to move in the +Z, -Z, +X, and -X directions respectively. In addition, users may press E or Q to move up and down (+Y and -Z). The application also tracks the users’ mouse cursor to adjust the movement direction accordingly. The lighting on the objects will change based on movement around the scene.
Lastly, this project uses object-oriented programming to organize the code and add modularity to the project. Various functions are used to abstract low level details of, for example, setting values for uniform variables inside the shader programs. The ShaderManager class is responsible for such functions. Another class, SceneManager, stores all configuration values for models, projections, textures, lighting, etc. and makes the appropriate calls to an instance of the ShaderManager class to render the scene in this project. In addition, we use custom functions that automate processes for us. For example, we use a function loadTextureFromFile to take the name of a texture file and a tag to load the file into memory, create a mipmap and perform other texture tiling, before passing it to the vertex shader.
![image](https://github.com/Afshin-A/7-1_FinalProjectMilestones/assets/86595208/221e0a0b-49e6-4c14-b20b-ae4b1618e9b2)