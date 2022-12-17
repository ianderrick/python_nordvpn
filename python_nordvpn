import tkinter as tk
import subprocess

class NordVPNClient:
    def __init__(self, master):
        self.master = master
        master.title("NordVPN Client")

        self.connect_button = tk.Button(master, text="Connect", command=self.connect)
        self.connect_button.pack()

        self.disconnect_button = tk.Button(master, text="Disconnect", command=self.disconnect)
        self.disconnect_button.pack()

        self.p2p_button = tk.Button(master, text="Enable P2P", command=self.enable_p2p)
        self.p2p_button.pack()

        self.meshnet_button = tk.Button(master, text="Enable Meshnet", command=self.enable_meshnet)
        self.meshnet_button.pack()

    def connect(self):
        subprocess.run(["nordvpn", "connect"])

    def disconnect(self):
        subprocess.run(["nordvpn", "disconnect"])

    def enable_p2p(self):
        subprocess.run(["nordvpn", "set", "p2p"])

    def enable_meshnet(self):
        subprocess.run(["nordvpn", "set", "meshnet"])

root = tk.Tk()
my_gui = NordVPNClient(root)
root.mainloop()
