{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Alpha Beta Filter\n",
    "\n",
    "\n",
    "This post goes over an implementation of an Alpha Beta Filter in Python."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "import numpy as np\n",
    "import matplotlib.pyplot as plt\n",
    "import pdb\n",
    "\n",
    "dt = 0.5\n",
    "xk_1 = 0\n",
    "vk_1 = 0\n",
    "ak_1 = 0\n",
    "\n",
    "a = 0.1\n",
    "b = 0.1\n",
    "g = 0.001\n",
    "\n",
    "iteration = 0\n",
    "\n",
    "fig = plt.figure()\n",
    "fig.show()\n",
    "fig.canvas.show\n",
    "plt.axis([0, 200, 0, 1.5])\n",
    "\n",
    "while True:\n",
    "    xm = np.random.rand(1)\n",
    "\n",
    "    xk = xk_1 + (vk_1 * dt)\n",
    "    vk = vk_1 + (ak_1 * dt)\n",
    "    ak = (vk - vk_1) /dt\n",
    "\n",
    "    rk = xm - xk\n",
    "\n",
    "    xk += a*rk\n",
    "    vk += (b*rk)/dt\n",
    "    ak += (2*g*rk)/np.power(dt,2)\n",
    "\n",
    "    xk_1 = xk\n",
    "    vk_1 = vk\n",
    "    ak_1 = ak\n",
    "\n",
    "    print(\"xk = \" ,xk, \"vk = \" ,vk, \"ak = \",ak)\n",
    "    iteration += 1\n",
    "    #plt.axis([0, 20+iteration, 0, 1.5])\n",
    "    plt.plot(iteration,xm,'k+')\n",
    "    plt.plot(iteration,xk,'b*')\n",
    "    plt.pause(0.05)\n",
    "    plt.draw()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
