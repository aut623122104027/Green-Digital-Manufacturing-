import psutil

def check_energy_usage():
    battery = psutil.sensors_battery()
    if battery:
        print(f"Battery percent: {battery.percent}%")
        print(f"Power plugged in: {battery.power_plugged}")
    else:
        print("No battery data available.")

check_energy_usage()
