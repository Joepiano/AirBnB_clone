README.md
![hbnb_logo](https://user-images.githubusercontent.com/99508912/189758710-90bf3d75-de52-4ec1-a712-276520e760d4.png)

Description 🏠
AirBnB Clone - The Console The console is the first segment of the AirBnB project at Holberton School that will collectively cover fundamental concepts of higher level programming. The goal of AirBnB project is to eventually deploy our server a simple copy of the AirBnB Website(HBnB). A command interpreter is created in this segment to manage objects for the AirBnB(HBnB) website.

The project currently only implements the back-end console.

Classes 🆑



Storage 🛄
The above classes are handled by the abstracted storage engine defined in the FileStorage class.

Every time the backend is initialized, HolbertonBnB instantiates an instance of FileStorage called storage. The storage object is loaded/re-loaded from any class instances stored in the JSON file file.json. As class instances are created, updated, or deleted, the storage object is used to register corresponding changes in the file.json.

Console 💻
The console is a command line interpreter that permits management of the backend of HolbertonBnB. It can be used to handle and manipulate all classes utilized by the application (achieved by calls on the storage object defined above).

Using the Console
The HolbertonBnB console can be run both interactively and non-interactively. To run the console in non-interactive mode, pipe any command(s) into an execution of the file console.py at the command line.

$ echo "help" | ./console.py
(hbnb) 
Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb) 
$
Alternatively, to use the HolbertonBnB console in interactive mode, run the file console.py by itself:

$ ./console.py
While running in interactive mode, the console displays a prompt for input:

$ ./console.py
(hbnb) 
To quit the console, enter the command quit, or input an EOF signal (ctrl-D).

$ ./console.py
(hbnb) quit
$
$ ./console.py
(hbnb) EOF
$





Functionalities of this command interpreter: Create a new object (ex: a new User or a new Place) Retrieve an object from a file, a database etc... Do operations on objects (count, compute stats, etc..t Table of Content Environment Installation File D.) Update attributes of an object Destroy an objecescriptions Usage Examples of use Bugs Authors License Environment This project is interpreted/tested on Ubuntu 14.04 LTS using python3 (version 3.4.3)

Installation Clone this repository: git clone "https://github.com/alexaorrico/AirBnB_clone.git" Access AirBnb directory: cd AirBnB_clone Run hbnb(interactively): ./console and enter command Run hbnb(non-interactively): echo "" | ./console.py File  entry point of the command interpreter. List of cDescriptions console.py - the console contains theommands this console current supports:

EOF - exits console quit - exits console - overwrites default emptyline method and does nothing create - Creates a new instance ofBaseModel, saves it (to the JSON file) and prints the id destroy - Deletes an instance based on the class name and id (save the change into the JSON file). show - Prints the string representation of an instance based on the class name and id. all - Prints all string representation of all instances based or not on the class name. update - Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file). models/ directory contains classes used for this project: base_model.py - The BaseModel class from which future classes will be derived

def init(self, *args, **kwargs) - Initialization of the base model def str(self) - String representation of the BaseModel class def save(self) - Updates the attribute updated_at with the current datetime def to_dict(self) - returns a dictionary containing all keys/values of the instance Classes inherited from Base Model:

amenity.on : file_storage.py - serializes instances to a JSON file & deserializes back to instances

def allpy city.py place.py review.py state.py user.py /models/engine directory contains File Storage class that handles JASON serialization and deserializati(self) - returns the dictionary __objects def new(self, obj) - sets in __objects the obj with key .id def save(self) - serializes __objects to the JSON file (path: __file_path) def reload(self) - deserializes the JSON file to __objects /tests directory contains all unit test cases for this project: /test_models/test_base_model.py - Contains the TestBaseModel and TestBaseModelDocs classes TestBaseModelDocs class:

def setUpClass(cls)- Set up for the doc tests def test_pep8_conformance_base_model(self) - Test that models/base_model.py conforms to PEP8 def test_pep8_conformance_test_base_model(self) - Test that tests/test_models/test_base_model.py conforms to PEP8 def test_bm_module_docstring(self) - Test for the base_model.py module docstring def test_bm_class_docstring(self) - Test for the BaseModel class docstring def test_bm_func_docstrings(self) - Test for the presence of docstrings in BaseModel methods TestBaseModel class:

def test_is_base_model(self) - Test that the instatiation of a BaseModel works def test_created_at_instantiation(self) - Test created_at is a pub. instance attribute of type datetime def test_updated_at_instantiation(self) - Test updated_at is a pub. instance attribute of type datetime def test_diff_datetime_objs(self) - Test that two BaseModel instances have different datetime objects /test_models/test_amenity.py - Contains the TestAmenityDocs class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_amenity(self) - Test that models/amenity.py conforms to PEP8 def test_pep8_conformance_test_amenity(self) - Test that tests/test_models/test_amenity.py conforms to PEP8 def test_amenity_module_docstring(self) - Test for the amenity.py module docstring def test_amenity_class_docstring(self) - Test for the Amenity class docstring /test_models/test_city.py - Contains the TestCityDocs class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_city(self) - Test that models/city.py conforms to PEP8 def test_pep8_conformance_test_city(self) - Test that tests/test_models/test_city.py conforms to PEP8 def test_city_module_docstring(self) - Test for the city.py module docstring def test_city_class_docstring(self) - Test for the City class docstring /test_models/test_file_storage.py - Contains the TestFileStorageDocs class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_file_storage(self) - Test that models/file_storage.py conforms to PEP8 def test_pep8_conformance_test_file_storage(self) - Test that tests/test_models/test_file_storage.py conforms to PEP8 def test_file_storage_module_docstring(self) - Test for the file_storage.py module docstring def test_file_storage_class_docstring(self) - Test for the FileStorage class docstring /test_models/test_place.py - Contains the TestPlaceDoc class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_place(self) - Test that models/place.py conforms to PEP8. def test_pep8_conformance_test_place(self) - Test that tests/test_models/test_place.py conforms to PEP8. def test_place_module_docstring(self) - Test for the place.py module docstring def test_place_class_docstring(self) - Test for the Place class docstring /test_models/test_review.py - Contains the TestReviewDocs class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_review(self) - Test that models/review.py conforms to PEP8 def test_pep8_conformance_test_review(self) - Test that tests/test_models/test_review.py conforms to PEP8 def test_review_module_docstring(self) - Test for the review.py module docstring def test_review_class_docstring(self) - Test for the Review class docstring /test_models/state.py - Contains the TestStateDocs class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_state(self) - Test that models/state.py conforms to PEP8 def test_pep8_conformance_test_state(self) - Test that tests/test_models/test_state.py conforms to PEP8 def test_state_module_docstring(self) - Test for the state.py module docstring def test_state_class_docstring(self) - Test for the State class docstring /test_models/user.py - Contains the TestUserDocs class:

def setUpClass(cls) - Set up for the doc tests def test_pep8_conformance_user(self) - Test that models/user.py conforms to PEP8 def test_pep8_conformance_test_user(self) - Test that tests/test_models/test_user.py conforms to PEP8 def test_user_module_docstring(self) - Test for the user.py module docstring def test_user_class_docstring(self) - Test for the User class docstring Examples of use vagrantAirBnB_clone$./console.py (hbnb) help

Documented commands (type help ):
EOF all create destroy help quit show update

(hbnb) all MyModel ** class doesn't exist ** (hbnb) create BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050 (hbnb) all BaseModel [[BaseModel] (7da56403-cc45-4f1c-ad32-bfafeb2bb050) {'updated_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772167), 'id': '7da56403-cc45-4f1c-ad32-bfafeb2bb050', 'created_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772123)}] (hbnb) show BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050 [BaseModel] (7da56403-cc45-4f1c-ad32-bfafeb2bb050) {'updated_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772167), 'id': '7da56403-cc45-4f1c-ad32-bfafeb2bb050', 'created_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772123)} (hbnb) destroy BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050 (hbnb) show BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050 ** no instance found ** (hbnb) quit Bugs No known bugs at this time.

Authors Joshua Ezunya - Github / Twitter.

License Public Domain. No copy write protection.
