+++
title = "About me"
draft = false
image = ""
description = ""
+++
![Source(http://www.hdwallpaper.nu/monkey-wallpapers/)](https://th.bing.com/th/id/OIP.Ei5im9NyrIGBDptvYP5o3gHaEo?pid=ImgDet&rs=1)

```python
import pgzrun

WIDTH = 800
HEIGHT = 600

WHITE = (255, 255, 255)


class Vec:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, b):
        return Vec(self.x + b.x, self.y + b.y)

    def __sub__(self, b):
        return Vec(self.x - b.x, self.y - b.y)

    def __mul__(self, b):
        return Vec(self.x * b, self.y * b)

    def len(self):
        return (self.x ** 2 + self.y ** 2) ** (1/2)

    def __str__(self):
        return "(" + str(self.x) + ", " + str(self.y) + ")"


class Body:
    def __init__(self):
        self.p = Vec(0, 0)
        self.v = Vec(0, 0)
        self.a = Vec(0, 0)
        self.m = 1

    def add_acceleration(self, a):
        self.a = self.a + a

    def draw(self):
        radius = 10
        colour = (0, 0, 0)
        screen.draw.filled_circle((self.p.x, self.p.y), radius, colour)

    def update(self, dt):
        self.v = self.v + self.a * dt
        self.p = self.p + self.v * dt
        self.a = Vec(0, 0)

ball = Body()
ball.p = Vec(400, 10)

def draw():
    screen.fill(WHITE)
    ball.draw()

def update(dt):
    ball.add_acceleration(Vec(0, 10))
    ball.update(dt)
    
pgzrun.go()

```

## My Name

mail@example.org

Here should be some info about me...