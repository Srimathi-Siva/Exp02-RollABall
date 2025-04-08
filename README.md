### Exp02-RollABall
### AIM :
To develop a 3D application for RollABall in unity.
### ALGORITHM :
~~~
STEP 1 :
Create a new project.
STEP 2 :
Click Heirarchy -> 3D object -> Select the plane -> 3DObject -> Sphere.
STEP 3 :
Define the physics properties of the surface (Rigidbody).
STEP 4 :
Assets -> Create -> # Script
STEP 5 :
Create a folder name Coding and create a C# file to add the coding in it.
STEP 6 :
To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.
STEP 7 :
Run the game and you can move the ball by using the respective keys
~~~
### PROGRAM :
Developed by : Mourya G
Reg No :  212224230170
~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class RollAball : MonoBehaviour
{
    // Start is called before the first frame update
    public float xforce = 5.0f, yforce = 200.0f, zforce = 5.0f;
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.A))
        {
            x = x - xforce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + xforce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z + zforce;
        }
        if (Input.GetKey(KeyCode.S))
        {
            z = z - zforce;
        }
        if (Input.GetKeyDown(KeyCode.Space))
        {
            y = yforce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);

    }
}
~~~
### OUTPUT :
![427544846-8516a654-5266-435a-8693-cca132472156](https://github.com/user-attachments/assets/0b64b5be-3b02-4345-9fdd-b4c5934daabf)
### RESULT :
Thus a 3D application for RollABall objects in unity is developed successfully.


