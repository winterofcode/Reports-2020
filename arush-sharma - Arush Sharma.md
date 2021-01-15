# Developer - Winter of Code 2020
# Arush Sharma
## Dynopii : pyvirtualaudiocable

The project was to develop a python based virtual audio cable. The project had no initial codebase and was built from scratch. I worked on developing the virtual audio cable for a linux operating system environment, and by the end of this WoC, was able to develop a python script that accomplished the goals we set out with.

I am Arush Sharma, an ECE second year undergraduate at [IIT Roorkee](https://iitr.ac.in), and this winter I worked at Dynopii as a WoC student.

The project was mentored by [Anubhav Singh](https://github.com/xprilion) and [Aniket Kumar](https://github.com/ani4aniket), along with [Abhishek Nandy](https://github.com/abhilegend), [Kazi Haque](https://github.com/kazi92), and [Snehangshu Bhattacharya](https://github.com/forkbomb-666)  
# Contributions
[10 commits](https://github.com/dynopii/pyvirtualaudiocable/commits?author=arushsharma24) <span style="color:green; font-size:0.7em">&nbsp;494++&nbsp;&nbsp;</span><span style="color:red; font-size:0.7em">434--</span>

This project was to be built from scratch, and I was free to proceed in any direction to choose how to accomplish our task. I had to research several of the possibilities such as pacmd/pactl, ALSA, JACK and to choose the best fit. 

I also had a great experience learning python, especially learning the [subprocess](https://docs.python.org/3/library/subprocess.html) module while also understanding piping between commands in the linux terminal and it's execution from python.

My work was submitted in the PR : [#2](https://github.com/dynopii/pyvirtualaudiocable/pull/2) "Virtual device creation and routing microphone audio via a python script", with a few notable commits being :
- 619e3dd : Python script pipes audio from arecord to aplay, and the modules are loaded and unloaded by running shell scripts
-  598ddad : Included the shell scripts into the python code, so that it is completely python based and consists of a single file.
  
# Future Scope
I beleive that the development of this virtual audio cable has only begun, and we have a long way to go ahead in it. This solution works and can be used, but we still face some issues in certain cases which I would like to see resolved in the future :
- Development for Windows operating systems
- Resolving the issue of echoing of the voice of other participants in a callz
- Device detected as an Output device instead on an input device in Discord
- Device not detected in Zoom

# Overall Experience
I had a lot of fun participating and contributing to Dynopii for this Winter of Code. It was certainly a very personally enjoyable experience being one of the initial developers in this project. While on the technical front, I learned a lot about audio management in linux, management of virtual devices, as well as python, the experience I had was also enriching in many other ways, as I communicated with my mentors and team members, had the experience of working in an organized project, learning a lot in the whole process. I would like to specially thank [Anubhav Singh](https://github.com/xprilion) and [Aniket Kumar](https://github.com/ani4aniket) for the excellent mentorship, for reviewing my work and for the inspiring guidance and support. This experience will definitely be remembered as a great start of what I hope to be a long and fun journey in the open source world.