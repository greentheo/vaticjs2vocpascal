import xml.etree.ElementTree as xmlET
import os

files = []
for file in os.listdir("data/vaticjs/project1/"):
    if file.endswith(".xml"):
        files.append(os.path.join("data/vaticjs/project1/", file))

for file in files:
    vjs = xmlET.parse(file)

    #get all the objects
    objs = [ child for child in vjs.getroot() if child.tag == 'object' ]

    frames = reduce(list.__add__, [list(child) for child in objs ])

    polygons = [frame for frame in  frames if frame.tag == 'polygon' ]

    #get all the frames for each object and get unique frames
    framenums = set([int(frame[0].text) for frame in polygons])


    #find the frames .jpg parsed files from the folder



    #create a new xml for each frame+objects


