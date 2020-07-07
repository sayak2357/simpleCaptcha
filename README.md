# simpleCaptcha
This is a simple captcha function along with a driver code which can be executed using jupyter notebook.

Steps to run the project(in Linux):

1) install pip3 in ubuntu using the commands:

    sudo apt-get update
    sudo apt-get -y install python3-pip
2) execute python3 in commandline or open jupyter notebook

3) in jupyter notebook or inside python3 shell, execute:
  import random
  from captcha.image import ImageCaptcha
  import IPython.display as display
  from PIL import Image

4) declare the following function:


  
  
        def simpleCaptcha():
    
    
            randInt = random.randint(1000,9999)
            n=str(randInt)


            image = ImageCaptcha()
            data = image.generate(n)
            image.write(n,'out.png')
    
   

            image_path = 'out.png'
            display.display(Image.open(image_path))
    
            ip=int(input('enter the number:'))
            if ip==randInt:
                print('correct')
                return True
            else:
                simpleCaptcha()
  
4) execute driver code by running simpleCaptcha() in commandline or in jupyter notebook

5) This project has a simpleCaptcha.ipynb file which contains the entire code of the project written using jupyter notebook
