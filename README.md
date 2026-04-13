# rtsp_checker.py-
import cv2

def check_rtsp(ip):
    url = f"rtsp://{ip}:554"

    print(f"Checking: {url}")

    cap = cv2.VideoCapture(url)

    if cap.isOpened():
        print("[+] Camera stream is accessible")
    else:
        print("[-] Cannot access camera")

    cap.release()
