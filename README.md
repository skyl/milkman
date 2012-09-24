Milkman - Easy django model object generation
=============================================

Quick Examples
--------------

	from milkman.dairy import milkman
	from myapp.models import Video, Editor
	
	# I just want a random video in the db to test with
	v = milkman.deliver(Video)
	
	# I want a video with a particular editor
	e = milkman.deliver(Editor)
	v = milkman.deliver(Video, editor=e)

    # I want a video with a random editor from exists
	v = milkman.deliver(Video, editor=milkman.random)

    # Force optional field generation
    v = milkman.deliver(Video, description=milkman.random)
	
	
Development
-----------
Install virtualenv and virtualenvwrapper

http://www.virtualenv.org/en/latest/index.html

http://pypi.python.org/pypi/virtualenvwrapper

    mkvirtualenv milkman
    pip install -r requirements.txt


Running Tests
-------------

    python setup.py test
  

Known Issues
------------
Several of the basic django model fields have generators, although most do not.  Let us know if there is a particular field to be implemented thats really bugging you, or just send a patch :)
