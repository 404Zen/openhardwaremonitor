## OpenHardwareMonitor

forked from [openhardwaremonitor/openhardwaremonitor](https://github.com/openhardwaremonitor/openhardwaremonitor)



### What's the different

裁剪了json的长度，只保留了实时数据Value的值，以适用于嵌入式IoT获取数据。

可以通过 http://localhost:8085/puredata.json 获取;

同时保留原版 http://localhost:8085/data.json ;

在我的PC上，获取到的json数据长度由9480字节缩减至约1585字节，实际数据长度会由于每台设备的差异和实时状态而产生变化.



对比数据

puredata.json

```
{
    "PCName": {
        "Name": "DESKTOP-XXXXXX"
    },
    "Mainboard0": {
        "Name": "DANA_MB"
    },
    "CPU0": {
        "Name": "Intel Core i7-8750H",
        "Clocks": {
            "Bus Speed": "100.4 MHz",
            "CPU Core #1": "2208.0 MHz",
            "CPU Core #2": "2208.0 MHz",
            "CPU Core #3": "2208.0 MHz",
            "CPU Core #4": "2208.0 MHz",
            "CPU Core #5": "3412.4 MHz",
            "CPU Core #6": "2810.2 MHz"
        },
        "Temperatures": {
            "CPU Core #1": "53.0 °C",
            "CPU Core #2": "51.0 °C",
            "CPU Core #3": "51.0 °C",
            "CPU Core #4": "50.0 °C",
            "CPU Core #5": "51.0 °C",
            "CPU Core #6": "50.0 °C",
            "CPU Package": "53.0 °C"
        },
        "Load": {
            "CPU Total": "3.8 %",
            "CPU Core #1": "3.9 %",
            "CPU Core #2": "7.0 %",
            "CPU Core #3": "3.1 %",
            "CPU Core #4": "2.3 %",
            "CPU Core #5": "1.5 %",
            "CPU Core #6": "4.7 %"
        },
        "Powers": {
            "CPU Package": "7.5 W",
            "CPU Cores": "6.1 W",
            "CPU Graphics": "0.0 W",
            "CPU DRAM": "0.8 W"
        }
    },
    "RAM0": {
        "Name": "Generic Memory",
        "Load": {
            "Memory": "61.2 %"
        },
        "Data": {
            "Used Memory": "9.7 GB",
            "Available Memory": "6.2 GB"
        }
    },
    "GpuNvidia0": {
        "Name": "NVIDIA NVIDIA GeForce GTX 1060 with Max-Q Design",
        "Clocks": {
            "GPU Core": "227.5 MHz",
            "GPU Memory": "405.0 MHz",
            "GPU Shader": "455.0 MHz"
        },
        "Temperatures": {
            "GPU Core": "55.0 °C"
        },
        "Load": {
            "GPU Core": "3.0 %",
            "GPU Frame Buffer": "4.0 %",
            "GPU Video Engine": "0.0 %",
            "GPU Bus Interface": "0.0 %",
            "GPU Memory": "13.1 %"
        },
        "Powers": {
            "GPU Power": "5.6 W"
        },
        "Data": {
            "GPU Memory Free": "5337.0 MB",
            "GPU Memory Used": "807.0 MB",
            "GPU Memory Total": "6144.0 MB"
        },
        "Throughput": {
            "GPU PCIE Rx": "0.0 KB/s",
            "GPU PCIE Tx": "0.0 KB/s"
        }
    },
    "HDD0": {
        "Name": "ST1000LM048-2E7172",
        "Temperatures": {
            "Temperature": "38.0 °C"
        },
        "Load": {
            "Used Space": "60.5 %"
        }
    },
    "HDD1": {
        "Name": "Generic Hard Disk",
        "Load": {
            "Used Space": "69.1 %"
        }
    }
}
```



data.json

```
{
    "id": 0,
    "Text": "Sensor",
    "Children": [
        {
            "id": 1,
            "Text": "DESKTOP-XXXXXX",
            "Children": [
                {
                    "id": 2,
                    "Text": "DANA_MB",
                    "Children": [],
                    "Min": "",
                    "Value": "",
                    "Max": "",
                    "ImageURL": "images_icon/mainboard.png"
                },
                {
                    "id": 3,
                    "Text": "Intel Core i7-8750H",
                    "Children": [
                        {
                            "id": 4,
                            "Text": "Clocks",
                            "Children": [
                                {
                                    "id": 5,
                                    "Text": "Bus Speed",
                                    "Children": [],
                                    "Min": "100.4 MHz",
                                    "Value": "100.4 MHz",
                                    "Max": "100.4 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 6,
                                    "Text": "CPU Core #1",
                                    "Children": [],
                                    "Min": "2208.0 MHz",
                                    "Value": "3914.2 MHz",
                                    "Max": "4014.6 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 7,
                                    "Text": "CPU Core #2",
                                    "Children": [],
                                    "Min": "2208.0 MHz",
                                    "Value": "2208.0 MHz",
                                    "Max": "4014.6 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 8,
                                    "Text": "CPU Core #3",
                                    "Children": [],
                                    "Min": "2208.0 MHz",
                                    "Value": "2208.0 MHz",
                                    "Max": "4014.6 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 9,
                                    "Text": "CPU Core #4",
                                    "Children": [],
                                    "Min": "2208.0 MHz",
                                    "Value": "2208.0 MHz",
                                    "Max": "4014.6 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 10,
                                    "Text": "CPU Core #5",
                                    "Children": [],
                                    "Min": "2208.0 MHz",
                                    "Value": "3914.2 MHz",
                                    "Max": "4014.6 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 11,
                                    "Text": "CPU Core #6",
                                    "Children": [],
                                    "Min": "2208.0 MHz",
                                    "Value": "3914.2 MHz",
                                    "Max": "4014.6 MHz",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/clock.png"
                        },
                        {
                            "id": 12,
                            "Text": "Temperatures",
                            "Children": [
                                {
                                    "id": 13,
                                    "Text": "CPU Core #1",
                                    "Children": [],
                                    "Min": "45.0 °C",
                                    "Value": "51.0 °C",
                                    "Max": "73.0 °C",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 14,
                                    "Text": "CPU Core #2",
                                    "Children": [],
                                    "Min": "45.0 °C",
                                    "Value": "50.0 °C",
                                    "Max": "73.0 °C",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 15,
                                    "Text": "CPU Core #3",
                                    "Children": [],
                                    "Min": "44.0 °C",
                                    "Value": "50.0 °C",
                                    "Max": "71.0 °C",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 16,
                                    "Text": "CPU Core #4",
                                    "Children": [],
                                    "Min": "43.0 °C",
                                    "Value": "48.0 °C",
                                    "Max": "72.0 °C",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 17,
                                    "Text": "CPU Core #5",
                                    "Children": [],
                                    "Min": "44.0 °C",
                                    "Value": "49.0 °C",
                                    "Max": "71.0 °C",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 18,
                                    "Text": "CPU Core #6",
                                    "Children": [],
                                    "Min": "43.0 °C",
                                    "Value": "48.0 °C",
                                    "Max": "65.0 °C",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 19,
                                    "Text": "CPU Package",
                                    "Children": [],
                                    "Min": "45.0 °C",
                                    "Value": "51.0 °C",
                                    "Max": "76.0 °C",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/temperature.png"
                        },
                        {
                            "id": 20,
                            "Text": "Load",
                            "Children": [
                                {
                                    "id": 21,
                                    "Text": "CPU Total",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "16.7 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 22,
                                    "Text": "CPU Core #1",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "15.5 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 23,
                                    "Text": "CPU Core #2",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "21.1 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 24,
                                    "Text": "CPU Core #3",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "17.9 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 25,
                                    "Text": "CPU Core #4",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "14.1 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 26,
                                    "Text": "CPU Core #5",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "14.8 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 27,
                                    "Text": "CPU Core #6",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "17.1 %",
                                    "Max": "100.0 %",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/load.png"
                        },
                        {
                            "id": 28,
                            "Text": "Powers",
                            "Children": [
                                {
                                    "id": 29,
                                    "Text": "CPU Package",
                                    "Children": [],
                                    "Min": "1.9 W",
                                    "Value": "14.0 W",
                                    "Max": "44.4 W",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 30,
                                    "Text": "CPU Cores",
                                    "Children": [],
                                    "Min": "1.1 W",
                                    "Value": "12.7 W",
                                    "Max": "42.3 W",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 31,
                                    "Text": "CPU Graphics",
                                    "Children": [],
                                    "Min": "0.0 W",
                                    "Value": "0.0 W",
                                    "Max": "0.1 W",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 32,
                                    "Text": "CPU DRAM",
                                    "Children": [],
                                    "Min": "0.7 W",
                                    "Value": "1.2 W",
                                    "Max": "3.2 W",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/power.png"
                        }
                    ],
                    "Min": "",
                    "Value": "",
                    "Max": "",
                    "ImageURL": "images_icon/cpu.png"
                },
                {
                    "id": 33,
                    "Text": "Generic Memory",
                    "Children": [
                        {
                            "id": 34,
                            "Text": "Load",
                            "Children": [
                                {
                                    "id": 35,
                                    "Text": "Memory",
                                    "Children": [],
                                    "Min": "59.8 %",
                                    "Value": "62.2 %",
                                    "Max": "62.9 %",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/load.png"
                        },
                        {
                            "id": 36,
                            "Text": "Data",
                            "Children": [
                                {
                                    "id": 37,
                                    "Text": "Used Memory",
                                    "Children": [],
                                    "Min": "9.5 GB",
                                    "Value": "9.9 GB",
                                    "Max": "10.0 GB",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 38,
                                    "Text": "Available Memory",
                                    "Children": [],
                                    "Min": "5.9 GB",
                                    "Value": "6.0 GB",
                                    "Max": "6.4 GB",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/power.png"
                        }
                    ],
                    "Min": "",
                    "Value": "",
                    "Max": "",
                    "ImageURL": "images_icon/ram.png"
                },
                {
                    "id": 39,
                    "Text": "NVIDIA NVIDIA GeForce GTX 1060 with Max-Q Design",
                    "Children": [
                        {
                            "id": 40,
                            "Text": "Clocks",
                            "Children": [
                                {
                                    "id": 41,
                                    "Text": "GPU Core",
                                    "Children": [],
                                    "Min": "139.0 MHz",
                                    "Value": "784.5 MHz",
                                    "Max": "1265.5 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 42,
                                    "Text": "GPU Memory",
                                    "Children": [],
                                    "Min": "405.0 MHz",
                                    "Value": "810.0 MHz",
                                    "Max": "4006.8 MHz",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 43,
                                    "Text": "GPU Shader",
                                    "Children": [],
                                    "Min": "278.0 MHz",
                                    "Value": "1569.0 MHz",
                                    "Max": "2531.0 MHz",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/clock.png"
                        },
                        {
                            "id": 44,
                            "Text": "Temperatures",
                            "Children": [
                                {
                                    "id": 45,
                                    "Text": "GPU Core",
                                    "Children": [],
                                    "Min": "49.0 °C",
                                    "Value": "52.0 °C",
                                    "Max": "56.0 °C",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/temperature.png"
                        },
                        {
                            "id": 46,
                            "Text": "Load",
                            "Children": [
                                {
                                    "id": 47,
                                    "Text": "GPU Core",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "1.0 %",
                                    "Max": "52.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 48,
                                    "Text": "GPU Frame Buffer",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "2.0 %",
                                    "Max": "17.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 49,
                                    "Text": "GPU Video Engine",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "0.0 %",
                                    "Max": "0.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 50,
                                    "Text": "GPU Bus Interface",
                                    "Children": [],
                                    "Min": "0.0 %",
                                    "Value": "0.0 %",
                                    "Max": "4.0 %",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 51,
                                    "Text": "GPU Memory",
                                    "Children": [],
                                    "Min": "11.6 %",
                                    "Value": "14.2 %",
                                    "Max": "14.5 %",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/load.png"
                        },
                        {
                            "id": 52,
                            "Text": "Powers",
                            "Children": [
                                {
                                    "id": 53,
                                    "Text": "GPU Power",
                                    "Children": [],
                                    "Min": "4.7 W",
                                    "Value": "7.9 W",
                                    "Max": "25.9 W",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/power.png"
                        },
                        {
                            "id": 54,
                            "Text": "Data",
                            "Children": [
                                {
                                    "id": 55,
                                    "Text": "GPU Memory Free",
                                    "Children": [],
                                    "Min": "5254.4 MB",
                                    "Value": "5270.3 MB",
                                    "Max": "5431.5 MB",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 56,
                                    "Text": "GPU Memory Used",
                                    "Children": [],
                                    "Min": "712.5 MB",
                                    "Value": "873.7 MB",
                                    "Max": "889.6 MB",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 57,
                                    "Text": "GPU Memory Total",
                                    "Children": [],
                                    "Min": "6144.0 MB",
                                    "Value": "6144.0 MB",
                                    "Max": "6144.0 MB",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/power.png"
                        },
                        {
                            "id": 58,
                            "Text": "Throughput",
                            "Children": [
                                {
                                    "id": 59,
                                    "Text": "GPU PCIE Rx",
                                    "Children": [],
                                    "Min": "0.0 KB/s",
                                    "Value": "5.9 MB/s",
                                    "Max": "652.3 MB/s",
                                    "ImageURL": "images/transparent.png"
                                },
                                {
                                    "id": 60,
                                    "Text": "GPU PCIE Tx",
                                    "Children": [],
                                    "Min": "0.0 KB/s",
                                    "Value": "1000.0 KB/s",
                                    "Max": "198.2 MB/s",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/power.png"
                        }
                    ],
                    "Min": "",
                    "Value": "",
                    "Max": "",
                    "ImageURL": "images_icon/nvidia.png"
                },
                {
                    "id": 61,
                    "Text": "ST1000LM048-2E7172",
                    "Children": [
                        {
                            "id": 62,
                            "Text": "Temperatures",
                            "Children": [
                                {
                                    "id": 63,
                                    "Text": "Temperature",
                                    "Children": [],
                                    "Min": "38.0 °C",
                                    "Value": "38.0 °C",
                                    "Max": "38.0 °C",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/temperature.png"
                        },
                        {
                            "id": 64,
                            "Text": "Load",
                            "Children": [
                                {
                                    "id": 65,
                                    "Text": "Used Space",
                                    "Children": [],
                                    "Min": "60.5 %",
                                    "Value": "60.5 %",
                                    "Max": "60.5 %",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/load.png"
                        }
                    ],
                    "Min": "",
                    "Value": "",
                    "Max": "",
                    "ImageURL": "images_icon/hdd.png"
                },
                {
                    "id": 66,
                    "Text": "Generic Hard Disk",
                    "Children": [
                        {
                            "id": 67,
                            "Text": "Load",
                            "Children": [
                                {
                                    "id": 68,
                                    "Text": "Used Space",
                                    "Children": [],
                                    "Min": "69.1 %",
                                    "Value": "69.1 %",
                                    "Max": "69.1 %",
                                    "ImageURL": "images/transparent.png"
                                }
                            ],
                            "Min": "",
                            "Value": "",
                            "Max": "",
                            "ImageURL": "images_icon/load.png"
                        }
                    ],
                    "Min": "",
                    "Value": "",
                    "Max": "",
                    "ImageURL": "images_icon/hdd.png"
                }
            ],
            "Min": "",
            "Value": "",
            "Max": "",
            "ImageURL": "images_icon/computer.png"
        }
    ],
    "Min": "Min",
    "Value": "Value",
    "Max": "Max",
    "ImageURL": ""
}
```

