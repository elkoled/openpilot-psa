# ECU Firmware Query

## Summary

| ECU Name  | CAN Tx Addr | CAN Rx Addr | Bus | ECU Serial Number        | Manufacturing Date | Notes                  |
|-----------|-------------|-------------|-----|---------------------------|---------------------|----------------------|
| ARTIV     | 0x6B6       | 0x696       | 1   | 212053276                | 0x180521 (21.05.18) | Radar                 |
| DIRECTN   | 0x6B5       | 0x695       | 0   | 6077GC0817309            | 0x070615 (15.06.07) |              |
| CMM_E/HCU2| 0x6A6       | 0x686       | 0   | 210306062100             | 0x060321 (21.03.06) |              |
| MSB       | 0x6B4       | 0x694       | 0   | 521021900860             | 0x110121 (21.01.11) |              |
| VCU       | 0x6A2       | 0x682       | 0   | 9210126909               | 0x170521 (21.05.17) |              |
| ABRASR    | 0x6AD       | 0x68D       | 0   | 085095700857210527       | 0x270521 (21.05.27) | DTC error on query    |


## DEBUG prints fw_versions:

# fw_query_3:
```
Waiting for CAN messages...
starting python selfdrive.locationd.paramsd
Getting VIN & FW versions
Getting VIN & FW versions
starting python selfdrive.locationd.lagd
Setting OBD multiplexing to True
waiting for modem to come up
starting python selfdrive.controls.plannerd
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 0 success
system/camerad/cameras/spectra.cc: get session: 0 0xB60200
system/camerad/cameras/spectra.cc: -- Accessing sensor
starting python selfdrive.controls.radard
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
plannerd is waiting for CarParams
radard is waiting for CarParams
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 0
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xB60200 isp: 0xB40102 sensors: 0x2A0101 link: 0x760104
system/camerad/cameras/spectra.cc: link control: 0
updated is dead with 0
system/camerad/cameras/spectra.cc: start csiphy: 0
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 0
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 35) 0x23000d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 36) 0x24000e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 37) 0x25000f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 38) 0x260010 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 39) 0x270011 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 40) 0x280012 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 41) 0x290013 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 42) 0x2a0014 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 43) 0x2b0015 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 44) 0x2c0016 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 45) 0x2d0017 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 46) 0x2e0018 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 47) 0x2f0019 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 48) 0x30001a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 49) 0x31001b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 50) 0x32001c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 51) 0x33001d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 52) 0x34001e 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 0 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 1
system/camerad/cameras/spectra.cc: -- Probing sensor 1
OBD multiplexing set successfully
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0322f19000000000
CAN-TX: 0x7df - 0x0322f19000000000
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0322f19000000000
CAN-TX: 0x18db33f1 - 0x0322f19000000000
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL version: "OpenGL ES 3.2 "
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL vendor: "Qualcomm"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL renderer: "Adreno (TM) 630"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL language version: "OpenGL ES GLSL ES 3.20"
selfdrive/ui/qt/widgets/cameraview.cc: connecting to stream 0, was connected to 0
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 1 success
system/camerad/cameras/spectra.cc: get session: 0 0xF40205
system/camerad/cameras/spectra.cc: -- Accessing sensor
CAN-RX: 0x795 - 0x000000000090
CAN-RX: 0x795 - 0x000000000090
ISO-TP: RX - single frame - 0x795 idx=0 done=True
ISO-TP: RX - single frame - 0x795 idx=0 done=True
iso-tp query empty response: (1933, None)
iso-tp query empty response: (1933, None)
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0209020000000000
CAN-TX: 0x7df - 0x0209020000000000
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-RX: 0x7e8 - 0x1014490201565233
CAN-RX: 0x7e8 - 0x1014490201565233
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: TX - flow control continue - 0x7e0
ISO-TP: TX - flow control continue - 0x7e0
CAN-TX: 0x7e0 - 0x30000a0000000000
CAN-TX: 0x7e0 - 0x30000a0000000000
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
system/camerad/cameras/spectra.cc: acquire isp dev
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
system/camerad/cameras/spectra.cc: opened csiphy for 1
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xF40205 isp: 0x180107 sensors: 0x6C0106 link: 0xD0109
system/camerad/cameras/spectra.cc: link control: 0
system/loggerd/loggerd.cc: logging to /data/media/0/realdata/00000051--530555e1dd--0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 1
CAN-RX: 0x7e8 - 0x2254303634343339
CAN-RX: 0x7e8 - 0x2254303634343339
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 61) 0x3d0025 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 62) 0x3e0026 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 63) 0x3f0027 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 64) 0x400028 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 65) 0x410029 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 66) 0x42002a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 67) 0x43002b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 68) 0x44002c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 69) 0x45002d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 70) 0x46002e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 71) 0x47002f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 72) 0x480030 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 73) 0x490031 0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: map buf req: (fd: 74) 0x4a0032 0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: map buf req: (fd: 75) 0x4b0033 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 76) 0x4c0034 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 77) 0x4d0035 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 78) 0x4e0036 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 1 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 2
system/camerad/cameras/spectra.cc: -- Probing sensor 2
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
got vin with request=b'\t\x02'
got vin with request=b'\t\x02'
system/loggerd/loggerd.cc: large volume of 'logMessage' messages
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 2 success
system/camerad/cameras/spectra.cc: get session: 0 0x9C020A
system/camerad/cameras/spectra.cc: -- Accessing sensor
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/spectra.cc: acquire isp dev
micd stream started: stream.samplerate=44100.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/camerad/cameras/spectra.cc: acquire icp dev
system/camerad/cameras/spectra.cc: opened csiphy for 2
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x9C020A isp: 0x83010C sensors: 0xC2010B link: 0x28010F
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: start icp: 0
system/camerad/cameras/spectra.cc: camera init 2
soundd stream started: stream.samplerate=48000.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/camerad/cameras/camera_common.cc: allocated 18 CL buffers
Setting OBD multiplexing to False
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 88) 0x580043 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 106) 0x6a0044 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 89) 0x590045 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 107) 0x6b0046 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 90) 0x5a0047 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 108) 0x6c0048 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 91) 0x5b0049 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 109) 0x6d004a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 92) 0x5c004b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 110) 0x6e004c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 93) 0x5d004d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 111) 0x6f004e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 94) 0x5e004f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 112) 0x700050 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 95) 0x5f0051 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 113) 0x710052 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 96) 0x600053 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 114) 0x720054 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 97) 0x610055 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 115) 0x730056 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 98) 0x620057 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 116) 0x740058 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 99) 0x630059 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 117) 0x75005a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 100) 0x64005b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 118) 0x76005c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 101) 0x65005d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 119) 0x77005e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 102) 0x66005f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 120) 0x780060 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 103) 0x670061 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 121) 0x790062 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 104) 0x680063 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 122) 0x7a0064 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 105) 0x690065 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 123) 0x7b0066 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 2 from 1
system/camerad/cameras/spectra.cc: flushed bps: 0
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/camera_qcom2.cc: -- Starting devices
system/camerad/cameras/spectra.cc: starting sensor 0
Starting listener for: camerad
system/camerad/cameras/spectra.cc: starting sensor 1
system/camerad/cameras/spectra.cc: starting sensor 2
system/camerad/cameras/camera_qcom2.cc: -- Dequeueing Video events
system/loggerd/encoderd.cc: encoder road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 34
system/loggerd/encoderd.cc: encoder driver_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 4
system/loggerd/encoderd.cc: encoder wide_road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 5
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
OBD multiplexing set successfully
models loaded, modeld starting
vision stream set up, main_wide_camera: False, use_extra_client: True
connected main cam with buffer size: 4804608 (1928 x 1208)
connected extra cam with buffer size: 4804608 (1928 x 1208)
common/clutil.cc: platform[0] CL_PLATFORM_NAME: QUALCOMM Snapdragon(TM)
common/clutil.cc: vendor: QUALCOMM
common/clutil.cc: platform version: OpenCL 2.0 QUALCOMM build: commit #f437276 changeid # Date: 12/06/18 Thu Local Branch:  Remote Branch: 
common/clutil.cc: profile: FULL_PROFILE
common/clutil.cc: extensions:  
common/clutil.cc: name: QUALCOMM Adreno(TM)
common/clutil.cc: device version: OpenCL 2.0 Adreno(TM) 630
common/clutil.cc: max work group size: 1024
common/clutil.cc: type = 4, CL_DEVICE_TYPE_GPU
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 78
system/camerad/cameras/spectra.cc: camera 0 synced on frame_id_offset 5 timestamp 1509223012270
system/camerad/cameras/spectra.cc: camera 1 synced on frame_id_offset 5 timestamp 1509223022110
system/camerad/cameras/spectra.cc: camera 2 synced on frame_id_offset 5 timestamp 1509223031637
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 177408
VIN VR3UHZKXZMT064439
VIN VR3UHZKXZMT064439
system/loggerd/encoderd.cc: camera 1 encoder ready
system/loggerd/encoderd.cc: camera 2 encoder ready
system/loggerd/encoderd.cc: camera 0 encoder ready
selfdrive/ui/qt/widgets/cameraview.cc: Drawing same frame twice 0
system/loggerd/encoderd.cc: camera 1 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 2 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 0 waiting for frame 2, cur 1
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/loggerd/loggerd.cc: driverEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000051--530555e1dd--0/dcamera.hevc remuxing:0
system/loggerd/loggerd.cc: qRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000051--530555e1dd--0/qcamera.ts remuxing:1
system/loggerd/loggerd.cc: wideRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000051--530555e1dd--0/ecamera.hevc remuxing:0
system/loggerd/loggerd.cc: roadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000051--530555e1dd--0/fcamera.hevc remuxing:0
models loaded, dmonitoringmodeld starting
connecting to driver stream
connected with buffer size: 4804608
quectel setup done
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {773: 7, 770: 7, 840: 8, 1042: 8, 973: 8, 845: 8, 941: 8, 757: 7, 909: 8, 520: 8, 610: 1, 841: 8, 1298: 4, 1390: 6, 1128: 8, 1257: 4, 1394: 8, 1416: 8, 781: 8, 1037: 8, 1304: 4, 1122: 4, 1272: 5, 749: 7, 1101: 8, 850: 2, 1006: 4, 1074: 8, 1186: 2, 1161: 8, 1010: 8, 877: 4, 1086: 6, 1099: 8, 1118: 6, 1150: 8, 1522: 5, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1486: 3, 1173: 4, 1278: 3, 1038: 5, 1554: 8, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1515: 8, 1230: 8, 1458: 8, 1102: 3}, 1: {632: 8, 760: 7, 792: 5, 525: 8, 461: 3, 717: 1, 845: 8, 909: 8, 514: 5, 546: 5, 664: 6, 690: 1, 1069: 4, 1170: 6, 728: 7, 946: 2, 1294: 8, 1400: 6, 813: 8, 758: 8, 1032: 6, 694: 8, 962: 2, 1074: 8, 1160: 8, 1218: 4, 1378: 4, 1426: 8, 1106: 6, 914: 2, 1166: 7, 1330: 5, 1266: 8, 1070: 6, 1270: 5, 1554: 8, 1517: 3, 1393: 1, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4}, 2: {773: 7, 770: 7, 840: 8, 1042: 8, 973: 8, 845: 8, 941: 8, 757: 7, 909: 8, 520: 8, 610: 1, 841: 8, 1298: 4, 1390: 6, 1128: 8, 1257: 4, 1394: 8, 1416: 8, 781: 8, 1037: 8, 1304: 4, 1122: 4, 1272: 5, 749: 7, 1101: 8, 850: 2, 1006: 4, 1074: 8, 1186: 2, 1161: 8, 1010: 8, 877: 4, 1086: 6, 1099: 8, 1118: 6, 1150: 8, 1522: 5, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1486: 3, 1173: 4, 1278: 3, 1038: 5, 1554: 8, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1515: 8, 1230: 8, 1458: 8, 1102: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.0220647389999158}
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {773: 7, 770: 7, 840: 8, 1042: 8, 973: 8, 845: 8, 941: 8, 757: 7, 909: 8, 520: 8, 610: 1, 841: 8, 1298: 4, 1390: 6, 1128: 8, 1257: 4, 1394: 8, 1416: 8, 781: 8, 1037: 8, 1304: 4, 1122: 4, 1272: 5, 749: 7, 1101: 8, 850: 2, 1006: 4, 1074: 8, 1186: 2, 1161: 8, 1010: 8, 877: 4, 1086: 6, 1099: 8, 1118: 6, 1150: 8, 1522: 5, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1486: 3, 1173: 4, 1278: 3, 1038: 5, 1554: 8, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1515: 8, 1230: 8, 1458: 8, 1102: 3}, 1: {632: 8, 760: 7, 792: 5, 525: 8, 461: 3, 717: 1, 845: 8, 909: 8, 514: 5, 546: 5, 664: 6, 690: 1, 1069: 4, 1170: 6, 728: 7, 946: 2, 1294: 8, 1400: 6, 813: 8, 758: 8, 1032: 6, 694: 8, 962: 2, 1074: 8, 1160: 8, 1218: 4, 1378: 4, 1426: 8, 1106: 6, 914: 2, 1166: 7, 1330: 5, 1266: 8, 1070: 6, 1270: 5, 1554: 8, 1517: 3, 1393: 1, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4}, 2: {773: 7, 770: 7, 840: 8, 1042: 8, 973: 8, 845: 8, 941: 8, 757: 7, 909: 8, 520: 8, 610: 1, 841: 8, 1298: 4, 1390: 6, 1128: 8, 1257: 4, 1394: 8, 1416: 8, 781: 8, 1037: 8, 1304: 4, 1122: 4, 1272: 5, 749: 7, 1101: 8, 850: 2, 1006: 4, 1074: 8, 1186: 2, 1161: 8, 1010: 8, 877: 4, 1086: 6, 1099: 8, 1118: 6, 1150: 8, 1522: 5, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1486: 3, 1173: 4, 1278: 3, 1038: 5, 1554: 8, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1515: 8, 1230: 8, 1458: 8, 1102: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.0220647389999158}
selfdrived got CarParams
modeld got CarParams: psa
skipping model eval. Dropped 20 frames
selfdrive/pandad/panda_safety.cc: Finished FW query, Waiting for params to set safety model
plannerd got CarParams: psa
restored torque params from cache
```
# fw_query_2
```
Waiting for CAN messages...
starting python selfdrive.locationd.paramsd
starting python selfdrive.locationd.lagd
Getting VIN & FW versions
Getting VIN & FW versions
Setting OBD multiplexing to True
waiting for modem to come up
starting python selfdrive.controls.plannerd
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 0 success
system/camerad/cameras/spectra.cc: get session: 0 0x170200
system/camerad/cameras/spectra.cc: -- Accessing sensor
starting python selfdrive.controls.radard
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
plannerd is waiting for CarParams
radard is waiting for CarParams
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 0
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x170200 isp: 0x540102 sensors: 0x740101 link: 0x440104
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
updated is dead with 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 0
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 35) 0x23000d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 36) 0x24000e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 37) 0x25000f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 38) 0x260010 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 39) 0x270011 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 40) 0x280012 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 41) 0x290013 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 42) 0x2a0014 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 43) 0x2b0015 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 44) 0x2c0016 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 45) 0x2d0017 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 46) 0x2e0018 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 47) 0x2f0019 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 48) 0x30001a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 49) 0x31001b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 50) 0x32001c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 51) 0x33001d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 52) 0x34001e 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 0 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 1
system/camerad/cameras/spectra.cc: -- Probing sensor 1
OBD multiplexing set successfully
ISO-TP: REQUEST - 0x7df 0x22f190
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
ISO-TP: REQUEST - 0x7df 0x22f190
system/camerad/cameras/spectra.cc: probing the sensor: -1
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0322f19000000000
CAN-TX: 0x7df - 0x0322f19000000000
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0322f19000000000
CAN-TX: 0x18db33f1 - 0x0322f19000000000
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 1 success
system/camerad/cameras/spectra.cc: get session: 0 0x550205
system/camerad/cameras/spectra.cc: -- Accessing sensor
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL version: "OpenGL ES 3.2 "
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL vendor: "Qualcomm"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL renderer: "Adreno (TM) 630"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL language version: "OpenGL ES GLSL ES 3.20"
selfdrive/ui/qt/widgets/cameraview.cc: connecting to stream 0, was connected to 0
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0209020000000000
CAN-TX: 0x7df - 0x0209020000000000
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-RX: 0x7e8 - 0x1014490201565233
CAN-RX: 0x7e8 - 0x1014490201565233
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: TX - flow control continue - 0x7e0
ISO-TP: TX - flow control continue - 0x7e0
CAN-TX: 0x7e0 - 0x30000a0000000000
CAN-TX: 0x7e0 - 0x30000a0000000000
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
system/loggerd/loggerd.cc: logging to /data/media/0/realdata/00000052--94ddb36b0a--0
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 1
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x550205 isp: 0x20107 sensors: 0xEF0106 link: 0x150109
system/camerad/cameras/spectra.cc: link control: 0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 1
CAN-RX: 0x7e8 - 0x2254303634343339
CAN-RX: 0x7e8 - 0x2254303634343339
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 61) 0x3d0025 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 62) 0x3e0026 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 63) 0x3f0027 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 64) 0x400028 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 65) 0x410029 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 66) 0x42002a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 67) 0x43002b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 68) 0x44002c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 69) 0x45002d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 70) 0x46002e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 71) 0x47002f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 72) 0x480030 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 73) 0x490031 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 74) 0x4a0032 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 75) 0x4b0033 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 76) 0x4c0034 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 77) 0x4d0035 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 78) 0x4e0036 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 1 from 1
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 2
system/camerad/cameras/spectra.cc: -- Probing sensor 2
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
got vin with request=b'\t\x02'
got vin with request=b'\t\x02'
system/loggerd/loggerd.cc: large volume of 'logMessage' messages
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 2 success
system/camerad/cameras/spectra.cc: get session: 0 0xDF020A
system/camerad/cameras/spectra.cc: -- Accessing sensor
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: acquire icp dev
system/camerad/cameras/spectra.cc: opened csiphy for 2
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xDF020A isp: 0x2010C sensors: 0x6C010B link: 0x8010F
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: start icp: 0
system/camerad/cameras/spectra.cc: camera init 2
soundd stream started: stream.samplerate=48000.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/camerad/cameras/camera_common.cc: allocated 18 CL buffers
micd stream started: stream.samplerate=44100.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
Setting OBD multiplexing to False
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 88) 0x580043 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 106) 0x6a0044 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 89) 0x590045 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 107) 0x6b0046 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 90) 0x5a0047 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 108) 0x6c0048 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 91) 0x5b0049 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 109) 0x6d004a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 92) 0x5c004b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 110) 0x6e004c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 93) 0x5d004d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 111) 0x6f004e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 94) 0x5e004f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 112) 0x700050 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 95) 0x5f0051 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 113) 0x710052 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 96) 0x600053 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 114) 0x720054 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 97) 0x610055 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 115) 0x730056 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 98) 0x620057 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 116) 0x740058 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 99) 0x630059 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 117) 0x75005a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 100) 0x64005b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 118) 0x76005c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 101) 0x65005d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 119) 0x77005e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 102) 0x66005f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 120) 0x780060 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 103) 0x670061 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 121) 0x790062 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 104) 0x680063 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 122) 0x7a0064 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 105) 0x690065 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 123) 0x7b0066 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 2 from 1
system/camerad/cameras/spectra.cc: flushed bps: 0
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/camera_qcom2.cc: -- Starting devices
system/camerad/cameras/spectra.cc: starting sensor 0
Starting listener for: camerad
system/camerad/cameras/spectra.cc: starting sensor 1
system/camerad/cameras/spectra.cc: starting sensor 2
system/camerad/cameras/camera_qcom2.cc: -- Dequeueing Video events
system/loggerd/encoderd.cc: encoder road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 34
system/loggerd/encoderd.cc: encoder driver_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 4
system/loggerd/encoderd.cc: encoder wide_road_cam_encoder init 1928x1208
OBD multiplexing set successfully
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 5
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
models loaded, modeld starting
vision stream set up, main_wide_camera: False, use_extra_client: True
connected main cam with buffer size: 4804608 (1928 x 1208)
connected extra cam with buffer size: 4804608 (1928 x 1208)
common/clutil.cc: platform[0] CL_PLATFORM_NAME: QUALCOMM Snapdragon(TM)
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 84
common/clutil.cc: vendor: QUALCOMM
common/clutil.cc: platform version: OpenCL 2.0 QUALCOMM build: commit #f437276 changeid # Date: 12/06/18 Thu Local Branch:  Remote Branch: 
common/clutil.cc: profile: FULL_PROFILE
common/clutil.cc: extensions:  
common/clutil.cc: name: QUALCOMM Adreno(TM)
common/clutil.cc: device version: OpenCL 2.0 Adreno(TM) 630
common/clutil.cc: max work group size: 1024
common/clutil.cc: type = 4, CL_DEVICE_TYPE_GPU
system/camerad/cameras/spectra.cc: camera 0 synced on frame_id_offset 5 timestamp 1700989283276
system/camerad/cameras/spectra.cc: camera 1 synced on frame_id_offset 5 timestamp 1700989331644
system/camerad/cameras/spectra.cc: camera 2 synced on frame_id_offset 5 timestamp 1700989296917
VIN VR3UHZKXZMT064439
VIN VR3UHZKXZMT064439
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 177408
system/loggerd/encoderd.cc: camera 1 encoder ready
system/loggerd/encoderd.cc: camera 2 encoder ready
system/loggerd/encoderd.cc: camera 0 encoder ready
selfdrive/ui/qt/widgets/cameraview.cc: Drawing same frame twice 0
system/loggerd/encoderd.cc: camera 1 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 2 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 0 waiting for frame 2, cur 1
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/loggerd/loggerd.cc: driverEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000052--94ddb36b0a--0/dcamera.hevc remuxing:0
system/loggerd/loggerd.cc: qRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000052--94ddb36b0a--0/qcamera.ts remuxing:1
system/loggerd/loggerd.cc: wideRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000052--94ddb36b0a--0/ecamera.hevc remuxing:0
system/loggerd/loggerd.cc: roadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000052--94ddb36b0a--0/fcamera.hevc remuxing:0
quectel setup done
models loaded, dmonitoringmodeld starting
connecting to driver stream
connected with buffer size: 4804608
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1394: 8, 1037: 8, 1128: 8, 757: 7, 1257: 4, 1416: 8, 820: 8, 520: 8, 610: 1, 841: 8, 1304: 4, 773: 7, 973: 8, 845: 8, 941: 8, 749: 7, 770: 7, 840: 8, 1101: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 1186: 2, 781: 8, 1010: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1099: 8, 1458: 8, 1522: 5, 909: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1042: 8, 1515: 8, 1161: 8, 1430: 4, 1298: 4, 1278: 3, 1173: 4, 1102: 3, 1038: 5, 1554: 8, 166: 2, 1390: 6, 1134: 2, 1387: 4, 1486: 3, 936: 6, 1422: 8, 1326: 8, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8}, 1: {946: 2, 1294: 8, 1393: 1, 632: 8, 728: 7, 1400: 6, 694: 8, 514: 5, 546: 5, 1032: 6, 525: 8, 461: 3, 717: 1, 845: 8, 760: 7, 792: 5, 962: 2, 1074: 8, 664: 6, 690: 1, 1160: 8, 758: 8, 813: 8, 1426: 8, 1218: 4, 1378: 4, 1106: 6, 909: 8, 914: 2, 1069: 4, 1166: 7, 1330: 5, 1266: 8, 1270: 5, 1070: 6, 1554: 8, 1490: 4, 1170: 6, 1517: 3, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8}, 2: {1394: 8, 1037: 8, 1128: 8, 757: 7, 1257: 4, 1416: 8, 820: 8, 520: 8, 610: 1, 841: 8, 1304: 4, 773: 7, 973: 8, 845: 8, 941: 8, 749: 7, 770: 7, 840: 8, 1101: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 1186: 2, 781: 8, 1010: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1099: 8, 1458: 8, 1522: 5, 909: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1042: 8, 1515: 8, 1161: 8, 1430: 4, 1298: 4, 1278: 3, 1173: 4, 1102: 3, 1038: 5, 1554: 8, 166: 2, 1390: 6, 1134: 2, 1387: 4, 1486: 3, 936: 6, 1422: 8, 1326: 8, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.007032922999997}
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1394: 8, 1037: 8, 1128: 8, 757: 7, 1257: 4, 1416: 8, 820: 8, 520: 8, 610: 1, 841: 8, 1304: 4, 773: 7, 973: 8, 845: 8, 941: 8, 749: 7, 770: 7, 840: 8, 1101: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 1186: 2, 781: 8, 1010: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1099: 8, 1458: 8, 1522: 5, 909: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1042: 8, 1515: 8, 1161: 8, 1430: 4, 1298: 4, 1278: 3, 1173: 4, 1102: 3, 1038: 5, 1554: 8, 166: 2, 1390: 6, 1134: 2, 1387: 4, 1486: 3, 936: 6, 1422: 8, 1326: 8, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8}, 1: {946: 2, 1294: 8, 1393: 1, 632: 8, 728: 7, 1400: 6, 694: 8, 514: 5, 546: 5, 1032: 6, 525: 8, 461: 3, 717: 1, 845: 8, 760: 7, 792: 5, 962: 2, 1074: 8, 664: 6, 690: 1, 1160: 8, 758: 8, 813: 8, 1426: 8, 1218: 4, 1378: 4, 1106: 6, 909: 8, 914: 2, 1069: 4, 1166: 7, 1330: 5, 1266: 8, 1270: 5, 1070: 6, 1554: 8, 1490: 4, 1170: 6, 1517: 3, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8}, 2: {1394: 8, 1037: 8, 1128: 8, 757: 7, 1257: 4, 1416: 8, 820: 8, 520: 8, 610: 1, 841: 8, 1304: 4, 773: 7, 973: 8, 845: 8, 941: 8, 749: 7, 770: 7, 840: 8, 1101: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 1186: 2, 781: 8, 1010: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1099: 8, 1458: 8, 1522: 5, 909: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1042: 8, 1515: 8, 1161: 8, 1430: 4, 1298: 4, 1278: 3, 1173: 4, 1102: 3, 1038: 5, 1554: 8, 166: 2, 1390: 6, 1134: 2, 1387: 4, 1486: 3, 936: 6, 1422: 8, 1326: 8, 1454: 5, 1483: 8, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.007032922999997}
controlsd got CarParams
modeld got CarParams: psa
selfdrived got CarParams
skipping model eval. Dropped 19 frames
selfdrive/pandad/panda_safety.cc: Finished FW query, Waiting for params to set safety model
plannerd got CarParams: psa
restored torque params from cache
radard got CarParams
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
skipping model eval. Dropped 2 frames
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{"event": "selfdrived.initialized", "dt": 0.91, "timeout": false, "canValid": true, "invalid": ["alertDebug", "gpsLocation"], "not_alive": ["alertDebug", "gpsLocation"], "not_freq_ok": ["alertDebug", "gpsLocation"], "error": true}
selfdrive/pandad/panda_safety.cc: got 448 bytes CarParams
selfdrive/pandad/panda_safety.cc: Panda 0: setting safety model: 31, param: 0, alternative experience: 1
selfdrive/pandad/pandad.cc: psa_init
```

# fw_query_1:
```
Waiting for CAN messages...
starting python selfdrive.locationd.paramsd
starting python selfdrive.locationd.lagd
starting python selfdrive.controls.plannerd
waiting for modem to come up
starting python selfdrive.controls.radard
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
plannerd is waiting for CarParams
radard is waiting for CarParams
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 0
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x2F0200 isp: 0xA50102 sensors: 0xAE0101 link: 0xF80104
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 0
Getting VIN & FW versions
Getting VIN & FW versions
Setting OBD multiplexing to True
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 35) 0x23000d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 36) 0x24000e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 37) 0x25000f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 38) 0x260010 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 39) 0x270011 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 40) 0x280012 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 41) 0x290013 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 42) 0x2a0014 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 43) 0x2b0015 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 44) 0x2c0016 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 45) 0x2d0017 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 46) 0x2e0018 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 47) 0x2f0019 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 48) 0x30001a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 49) 0x31001b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 50) 0x32001c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 51) 0x33001d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 52) 0x34001e 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 0 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 1
system/camerad/cameras/spectra.cc: -- Probing sensor 1
updated is dead with 0
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 1 success
system/camerad/cameras/spectra.cc: get session: 0 0x6D0205
system/camerad/cameras/spectra.cc: -- Accessing sensor
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL version: "OpenGL ES 3.2 "
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL vendor: "Qualcomm"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL renderer: "Adreno (TM) 630"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL language version: "OpenGL ES GLSL ES 3.20"
selfdrive/ui/qt/widgets/cameraview.cc: connecting to stream 0, was connected to 0
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
OBD multiplexing set successfully
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0322f19000000000
CAN-TX: 0x7df - 0x0322f19000000000
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0322f19000000000
CAN-TX: 0x18db33f1 - 0x0322f19000000000
CAN-RX: 0x795 - 0x000000000090
CAN-RX: 0x795 - 0x000000000090
ISO-TP: RX - single frame - 0x795 idx=0 done=True
ISO-TP: RX - single frame - 0x795 idx=0 done=True
iso-tp query empty response: (1933, None)
iso-tp query empty response: (1933, None)
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 1
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x6D0205 isp: 0xDB0107 sensors: 0x9C0106 link: 0x810109
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 1
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 61) 0x3d0025 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 62) 0x3e0026 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 63) 0x3f0027 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 64) 0x400028 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 65) 0x410029 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 66) 0x42002a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 67) 0x43002b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 68) 0x44002c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 69) 0x45002d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 70) 0x46002e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 71) 0x47002f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 72) 0x480030 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 73) 0x490031 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 74) 0x4a0032 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 75) 0x4b0033 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 76) 0x4c0034 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 77) 0x4d0035 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 78) 0x4e0036 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 1 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 2
system/camerad/cameras/spectra.cc: -- Probing sensor 2
system/loggerd/loggerd.cc: logging to /data/media/0/realdata/00000054--bf648d5fd3--0
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: REQUEST - 0x7df 0x0902
system/camerad/cameras/spectra.cc: probing the sensor: -1
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0209020000000000
CAN-TX: 0x7df - 0x0209020000000000
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-RX: 0x7e8 - 0x1014490201565233
CAN-RX: 0x7e8 - 0x1014490201565233
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: TX - flow control continue - 0x7e0
ISO-TP: TX - flow control continue - 0x7e0
CAN-TX: 0x7e0 - 0x30000a0000000000
CAN-TX: 0x7e0 - 0x30000a0000000000
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
system/loggerd/loggerd.cc: large volume of 'logMessage' messages
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
CAN-RX: 0x78d - 0xb800000000000000
CAN-RX: 0x78d - 0xb800000000000000
Error processing UDS response: (1925, None)
Traceback (most recent call last):
  File "/data/openpilot/opendbc/car/isotp_parallel_query.py", line 107, in get_data
    dat, rx_in_progress = msg.recv()
                          ^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 451, in recv
    frame_type = self._isotp_rx_next(msg)
                 ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 557, in _isotp_rx_next
    raise Exception(f"isotp - rx: invalid frame type: {rx_data[0] >> 4}")
Exception: isotp - rx: invalid frame type: 11
Error processing UDS response: (1925, None)
Traceback (most recent call last):
  File "/data/openpilot/opendbc/car/isotp_parallel_query.py", line 107, in get_data
    dat, rx_in_progress = msg.recv()
                          ^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 451, in recv
    frame_type = self._isotp_rx_next(msg)
                 ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 557, in _isotp_rx_next
    raise Exception(f"isotp - rx: invalid frame type: {rx_data[0] >> 4}")
Exception: isotp - rx: invalid frame type: 11
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
CAN-RX: 0x7e8 - 0x2254303634343339
CAN-RX: 0x7e8 - 0x2254303634343339
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 2 success
system/camerad/cameras/spectra.cc: get session: 0 0x34020A
system/camerad/cameras/spectra.cc: -- Accessing sensor
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
got vin with request=b'\t\x02'
got vin with request=b'\t\x02'
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
system/camerad/cameras/spectra.cc: acquire isp dev
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
micd stream started: stream.samplerate=44100.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/camerad/cameras/spectra.cc: acquire icp dev
system/camerad/cameras/spectra.cc: opened csiphy for 2
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x34020A isp: 0x3F010C sensors: 0xEA010B link: 0x8D010F
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: start icp: 0
system/camerad/cameras/spectra.cc: camera init 2
system/camerad/cameras/camera_common.cc: allocated 18 CL buffers
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 88) 0x580043 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 106) 0x6a0044 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 89) 0x590045 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 107) 0x6b0046 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 90) 0x5a0047 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 108) 0x6c0048 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 91) 0x5b0049 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 109) 0x6d004a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 92) 0x5c004b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 110) 0x6e004c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 93) 0x5d004d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 111) 0x6f004e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 94) 0x5e004f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 112) 0x700050 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 95) 0x5f0051 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 113) 0x710052 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 96) 0x600053 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 114) 0x720054 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 97) 0x610055 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 115) 0x730056 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 98) 0x620057 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 116) 0x740058 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 99) 0x630059 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 117) 0x75005a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 100) 0x64005b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 118) 0x76005c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 101) 0x65005d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 119) 0x77005e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 102) 0x66005f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 120) 0x780060 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 103) 0x670061 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 121) 0x790062 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 104) 0x680063 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 122) 0x7a0064 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 105) 0x690065 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 123) 0x7b0066 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 2 from 1
system/camerad/cameras/spectra.cc: flushed bps: 0
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/camera_qcom2.cc: -- Starting devices
system/camerad/cameras/spectra.cc: starting sensor 0
Starting listener for: camerad
system/camerad/cameras/spectra.cc: starting sensor 1
system/camerad/cameras/spectra.cc: starting sensor 2
system/camerad/cameras/camera_qcom2.cc: -- Dequeueing Video events
soundd stream started: stream.samplerate=48000.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/loggerd/encoderd.cc: encoder road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 34
system/loggerd/encoderd.cc: encoder driver_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 4
system/loggerd/encoderd.cc: encoder wide_road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 5
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
models loaded, modeld starting
vision stream set up, main_wide_camera: False, use_extra_client: True
connected main cam with buffer size: 4804608 (1928 x 1208)
connected extra cam with buffer size: 4804608 (1928 x 1208)
common/clutil.cc: platform[0] CL_PLATFORM_NAME: QUALCOMM Snapdragon(TM)
common/clutil.cc: vendor: QUALCOMM
common/clutil.cc: platform version: OpenCL 2.0 QUALCOMM build: commit #f437276 changeid # Date: 12/06/18 Thu Local Branch:  Remote Branch: 
common/clutil.cc: profile: FULL_PROFILE
common/clutil.cc: extensions:  
common/clutil.cc: name: QUALCOMM Adreno(TM)
common/clutil.cc: device version: OpenCL 2.0 Adreno(TM) 630
common/clutil.cc: max work group size: 1024
common/clutil.cc: type = 4, CL_DEVICE_TYPE_GPU
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 78
Setting OBD multiplexing to False
system/camerad/cameras/spectra.cc: camera 0 synced on frame_id_offset 5 timestamp 1834839412734
system/camerad/cameras/spectra.cc: camera 1 synced on frame_id_offset 5 timestamp 1834839423299
system/camerad/cameras/spectra.cc: camera 2 synced on frame_id_offset 5 timestamp 1834839432824
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 177408
system/loggerd/encoderd.cc: camera 1 encoder ready
system/loggerd/encoderd.cc: camera 2 encoder ready
system/loggerd/encoderd.cc: camera 0 encoder ready
selfdrive/ui/qt/widgets/cameraview.cc: Drawing same frame twice 0
OBD multiplexing set successfully
system/loggerd/encoderd.cc: camera 1 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 2 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 0 waiting for frame 2, cur 1
system/loggerd/loggerd.cc: driverEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000054--bf648d5fd3--0/dcamera.hevc remuxing:0
system/loggerd/loggerd.cc: qRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000054--bf648d5fd3--0/qcamera.ts remuxing:1
system/loggerd/loggerd.cc: wideRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000054--bf648d5fd3--0/ecamera.hevc remuxing:0
system/loggerd/loggerd.cc: roadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000054--bf648d5fd3--0/fcamera.hevc remuxing:0
VIN VR3UHZKXZMT064439
VIN VR3UHZKXZMT064439
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
models loaded, dmonitoringmodeld starting
connecting to driver stream
connected with buffer size: 4804608
quectel setup done
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {757: 7, 1257: 4, 1416: 8, 973: 8, 773: 7, 845: 8, 520: 8, 610: 1, 841: 8, 941: 8, 1304: 4, 909: 8, 770: 7, 840: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 781: 8, 1186: 2, 1037: 8, 1010: 8, 936: 6, 1128: 8, 1161: 8, 749: 7, 1101: 8, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1086: 6, 1118: 6, 1150: 8, 1042: 8, 877: 4, 1134: 2, 1298: 4, 1173: 4, 1422: 8, 1038: 5, 1554: 8, 1278: 3, 1326: 8, 1387: 4, 166: 2, 1390: 6, 1454: 5, 1394: 8, 1483: 8, 1522: 5, 1430: 4, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8, 1458: 8, 1102: 3, 1515: 8, 1486: 3}, 1: {632: 8, 728: 7, 1400: 6, 525: 8, 461: 3, 514: 5, 546: 5, 717: 1, 845: 8, 1393: 1, 909: 8, 760: 7, 758: 8, 792: 5, 962: 2, 1074: 8, 813: 8, 664: 6, 690: 1, 694: 8, 1160: 8, 946: 2, 1426: 8, 1218: 4, 1378: 4, 1032: 6, 1106: 6, 914: 2, 1069: 4, 1166: 7, 1330: 5, 1270: 5, 1266: 8, 1070: 6, 1518: 4, 1554: 8, 1517: 3, 1294: 8, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4, 1170: 6}, 2: {757: 7, 1257: 4, 1416: 8, 973: 8, 773: 7, 845: 8, 520: 8, 610: 1, 841: 8, 941: 8, 1304: 4, 909: 8, 770: 7, 840: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 781: 8, 1186: 2, 1037: 8, 1010: 8, 936: 6, 1128: 8, 1161: 8, 749: 7, 1101: 8, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1086: 6, 1118: 6, 1150: 8, 1042: 8, 877: 4, 1134: 2, 1298: 4, 1173: 4, 1422: 8, 1038: 5, 1554: 8, 1278: 3, 1326: 8, 1387: 4, 166: 2, 1390: 6, 1454: 5, 1394: 8, 1483: 8, 1522: 5, 1430: 4, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8, 1458: 8, 1102: 3, 1515: 8, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.0221305770000981}
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {757: 7, 1257: 4, 1416: 8, 973: 8, 773: 7, 845: 8, 520: 8, 610: 1, 841: 8, 941: 8, 1304: 4, 909: 8, 770: 7, 840: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 781: 8, 1186: 2, 1037: 8, 1010: 8, 936: 6, 1128: 8, 1161: 8, 749: 7, 1101: 8, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1086: 6, 1118: 6, 1150: 8, 1042: 8, 877: 4, 1134: 2, 1298: 4, 1173: 4, 1422: 8, 1038: 5, 1554: 8, 1278: 3, 1326: 8, 1387: 4, 166: 2, 1390: 6, 1454: 5, 1394: 8, 1483: 8, 1522: 5, 1430: 4, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8, 1458: 8, 1102: 3, 1515: 8, 1486: 3}, 1: {632: 8, 728: 7, 1400: 6, 525: 8, 461: 3, 514: 5, 546: 5, 717: 1, 845: 8, 1393: 1, 909: 8, 760: 7, 758: 8, 792: 5, 962: 2, 1074: 8, 813: 8, 664: 6, 690: 1, 694: 8, 1160: 8, 946: 2, 1426: 8, 1218: 4, 1378: 4, 1032: 6, 1106: 6, 914: 2, 1069: 4, 1166: 7, 1330: 5, 1270: 5, 1266: 8, 1070: 6, 1518: 4, 1554: 8, 1517: 3, 1294: 8, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4, 1170: 6}, 2: {757: 7, 1257: 4, 1416: 8, 973: 8, 773: 7, 845: 8, 520: 8, 610: 1, 841: 8, 941: 8, 1304: 4, 909: 8, 770: 7, 840: 8, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 781: 8, 1186: 2, 1037: 8, 1010: 8, 936: 6, 1128: 8, 1161: 8, 749: 7, 1101: 8, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 1293: 8, 1086: 6, 1118: 6, 1150: 8, 1042: 8, 877: 4, 1134: 2, 1298: 4, 1173: 4, 1422: 8, 1038: 5, 1554: 8, 1278: 3, 1326: 8, 1387: 4, 166: 2, 1390: 6, 1454: 5, 1394: 8, 1483: 8, 1522: 5, 1430: 4, 974: 8, 1941: 6, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1108: 8, 1172: 8, 1230: 8, 1458: 8, 1102: 3, 1515: 8, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.0221305770000981}
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
selfdrived got CarParams
selfdrive/pandad/panda_safety.cc: Finished FW query, Waiting for params to set safety model
restored torque params from cache
plannerd got CarParams: psa
controlsd got CarParams
radard got CarParams
modeld got CarParams: psa
skipping model eval. Dropped 24 frames
skipping model eval. Dropped 2 frames
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{"event": "selfdrived.initialized", "dt": 0.98, "timeout": false, "canValid": true, "invalid": ["alertDebug", "gpsLocation"], "not_alive": ["alertDebug", "gpsLocation"], "not_freq_ok": ["alertDebug", "gpsLocation"], "error": true}
selfdrive/pandad/panda_safety.cc: got 448 bytes CarParams
selfdrive/pandad/panda_safety.cc: Panda 0: setting safety model: 31, param: 0, alternative experience: 1
selfdrive/pandad/pandad.cc: psa_init
```

# extended debug print:
```
Waiting for CAN messages...
Getting VIN & FW versions
Getting VIN & FW versions
Setting OBD multiplexing to True
waiting for modem to come up
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
: "wl-shell" is a deprecated shell extension, prefer using "xdg-shell-v6" or "xdg-shell" if supported by the compositor by setting the environment variable QT_WAYLAND_SHELL_INTEGRATION
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
OBD multiplexing set successfully
Error processing UDS response: (1925, None)
Traceback (most recent call last):
  File "/data/openpilot/opendbc/car/isotp_parallel_query.py", line 107, in get_data
    dat, rx_in_progress = msg.recv()
                          ^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 451, in recv
    frame_type = self._isotp_rx_next(msg)
                 ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 557, in _isotp_rx_next
    raise Exception(f"isotp - rx: invalid frame type: {rx_data[0] >> 4}")
Exception: isotp - rx: invalid frame type: 11
Error processing UDS response: (1925, None)
Traceback (most recent call last):
  File "/data/openpilot/opendbc/car/isotp_parallel_query.py", line 107, in get_data
    dat, rx_in_progress = msg.recv()
                          ^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 451, in recv
    frame_type = self._isotp_rx_next(msg)
                 ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 557, in _isotp_rx_next
    raise Exception(f"isotp - rx: invalid frame type: {rx_data[0] >> 4}")
Exception: isotp - rx: invalid frame type: 11
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
iso-tp query empty response: (1930, None)
iso-tp query empty response: (1930, None)
Error processing UDS response: (1914, None)
Traceback (most recent call last):
  File "/data/openpilot/opendbc/car/isotp_parallel_query.py", line 107, in get_data
    dat, rx_in_progress = msg.recv()
                          ^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 451, in recv
    frame_type = self._isotp_rx_next(msg)
                 ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 524, in _isotp_rx_next
    assert not self.tx_done, "isotp - rx: flow control with no active frame"
           ^^^^^^^^^^^^^^^^
AssertionError: isotp - rx: flow control with no active frame
Error processing UDS response: (1914, None)
Traceback (most recent call last):
  File "/data/openpilot/opendbc/car/isotp_parallel_query.py", line 107, in get_data
    dat, rx_in_progress = msg.recv()
                          ^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 451, in recv
    frame_type = self._isotp_rx_next(msg)
                 ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/opendbc/car/uds.py", line 524, in _isotp_rx_next
    assert not self.tx_done, "isotp - rx: flow control with no active frame"
           ^^^^^^^^^^^^^^^^
AssertionError: isotp - rx: flow control with no active frame
system/camerad/cameras/spectra.cc: clearing and requeuing camera 0 from 1
system/loggerd/loggerd.cc: logging to /data/media/0/realdata/0000001a--d2a06e2a3b--0
got vin with request=b'\t\x02'
got vin with request=b'\t\x02'
ECU addr scan ‖ expected RX addrs: [(1218, None, 0), (1220, None, 0), (1223, None, 0), (1235, None, 0), (1242, None, 0), (1249, None, 0), (1380, None, 0), (1611, None, 0), (1666, None, 0), (1670, None, 0), (1677, None, 0), (1684, None, 0), (1685, None, 0), (1686, None, 0), (1686, None, 1), (1800, None, 0), (1801, None, 0), (1806, None, 0), (1806, None, 1), (1807, None, 0), (1807, None, 1), (1831, None, 0), (1831, None, 1), (1832, None, 0), (1833, None, 0), (1848, None, 0), (1848, None, 1), (1850, None, 0), (1850, None, 1), (1864, None, 0), (1864, None, 1), (1866, None, 0), (1866, None, 1), (1867, None, 0), (1867, None, 1), (1870, None, 0), (1870, None, 1), (1871, None, 0), (1880, 15, 0), (1880, 109, 0), (1888, None, 0), (1888, None, 1), (1890, None, 0), (1890, None, 1), (1891, None, 0), (1891, None, 1), (1896, None, 0), (1896, None, 1), (1900, None, 0), (1900, None, 1), (1907, None, 0), (1916, None, 0), (1916, None, 1), (1919, None, 0), (1919, None, 1), (1928, None, 0), (1935, None, 0), (1935, None, 1), (1945, None, 0), (1961, None, 0), (1962, None, 0), (1962, None, 1), (1963, None, 0), (1963, None, 1), (1976, None, 0), (1976, None, 1), (1977, None, 0), (1977, None, 1), (1979, None, 0), (1979, None, 1), (1983, None, 0), (1983, None, 1), (1984, None, 0), (1985, None, 0), (1985, None, 1), (1996, None, 0), (1996, None, 1), (1998, None, 0), (1998, None, 1), (2008, None, 0), (2008, None, 1), (2009, None, 0), (2009, None, 1), (2010, None, 0), (2012, None, 0), (2012, None, 1), (2024, None, 0), (2024, None, 1), (2025, None, 0), (2025, None, 1), (2026, None, 0), (2028, None, 0), (2048, None, 0), (2048, None, 1), (417001739, None, 0), (417001739, None, 1), (417001744, None, 0), (417001744, None, 1), (417001758, None, 0), (417001758, None, 1), (417001768, None, 0), (417001768, None, 1), (417001771, None, 0), (417001771, None, 1), (417001776, None, 0), (417001776, None, 1), (417001811, None, 0), (417001811, None, 1), (417001824, None, 0), (417001824, None, 1), (417001825, None, 0), (417001825, None, 1), (417001904, None, 0), (417001904, None, 1), (417001909, None, 0), (417001909, None, 1), (417001936, None, 0), (417001936, None, 1), (417001967, None, 0), (417001967, None, 1)]
NoneType: None
ECU addr scan ‖ expected RX addrs: [(1218, None, 0), (1220, None, 0), (1223, None, 0), (1235, None, 0), (1242, None, 0), (1249, None, 0), (1380, None, 0), (1611, None, 0), (1666, None, 0), (1670, None, 0), (1677, None, 0), (1684, None, 0), (1685, None, 0), (1686, None, 0), (1686, None, 1), (1800, None, 0), (1801, None, 0), (1806, None, 0), (1806, None, 1), (1807, None, 0), (1807, None, 1), (1831, None, 0), (1831, None, 1), (1832, None, 0), (1833, None, 0), (1848, None, 0), (1848, None, 1), (1850, None, 0), (1850, None, 1), (1864, None, 0), (1864, None, 1), (1866, None, 0), (1866, None, 1), (1867, None, 0), (1867, None, 1), (1870, None, 0), (1870, None, 1), (1871, None, 0), (1880, 15, 0), (1880, 109, 0), (1888, None, 0), (1888, None, 1), (1890, None, 0), (1890, None, 1), (1891, None, 0), (1891, None, 1), (1896, None, 0), (1896, None, 1), (1900, None, 0), (1900, None, 1), (1907, None, 0), (1916, None, 0), (1916, None, 1), (1919, None, 0), (1919, None, 1), (1928, None, 0), (1935, None, 0), (1935, None, 1), (1945, None, 0), (1961, None, 0), (1962, None, 0), (1962, None, 1), (1963, None, 0), (1963, None, 1), (1976, None, 0), (1976, None, 1), (1977, None, 0), (1977, None, 1), (1979, None, 0), (1979, None, 1), (1983, None, 0), (1983, None, 1), (1984, None, 0), (1985, None, 0), (1985, None, 1), (1996, None, 0), (1996, None, 1), (1998, None, 0), (1998, None, 1), (2008, None, 0), (2008, None, 1), (2009, None, 0), (2009, None, 1), (2010, None, 0), (2012, None, 0), (2012, None, 1), (2024, None, 0), (2024, None, 1), (2025, None, 0), (2025, None, 1), (2026, None, 0), (2028, None, 0), (2048, None, 0), (2048, None, 1), (417001739, None, 0), (417001739, None, 1), (417001744, None, 0), (417001744, None, 1), (417001758, None, 0), (417001758, None, 1), (417001768, None, 0), (417001768, None, 1), (417001771, None, 0), (417001771, None, 1), (417001776, None, 0), (417001776, None, 1), (417001811, None, 0), (417001811, None, 1), (417001824, None, 0), (417001824, None, 1), (417001825, None, 0), (417001825, None, 1), (417001904, None, 0), (417001904, None, 1), (417001909, None, 0), (417001909, None, 1), (417001936, None, 0), (417001936, None, 1), (417001967, None, 0), (417001967, None, 1)]
NoneType: None
ECU addr scan ‖ sending tester-present to: [(587, None, 0), (1792, None, 0), (1793, None, 0), (1798, None, 0), (1798, None, 1), (1799, None, 0), (1799, None, 1), (1810, None, 1), (1813, None, 1), (1824, None, 0), (1825, None, 0), (1840, None, 0), (1840, None, 1), (1842, None, 0), (1842, None, 1), (1843, None, 0), (1856, None, 0), (1856, None, 1), (1858, None, 0), (1858, None, 1), (1859, None, 0), (1859, None, 1), (1860, None, 0), (1862, None, 0), (1862, None, 1), (1863, None, 0), (1871, None, 1), (1875, None, 0), (1879, None, 1), (1882, None, 0), (1888, None, 0), (1888, None, 1), (1889, None, 0), (1892, None, 0), (1892, None, 1), (1920, None, 0), (1927, None, 0), (1927, None, 1), (1937, None, 0), (1953, None, 0), (1954, None, 0), (1954, None, 1), (1955, None, 0), (1955, None, 1), (1968, None, 0), (1968, None, 1), (1969, None, 0), (1969, None, 1), (1971, None, 0), (1971, None, 1), (1975, None, 0), (1975, None, 1), (1988, None, 0), (1988, None, 1), (1990, None, 0), (1990, None, 1), (2000, None, 0), (2000, None, 1), (2001, None, 0), (2001, None, 1), (2002, None, 0), (2004, None, 0), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (2018, None, 0), (2020, None, 0), (416943089, None, 0), (416943089, None, 1), (416944369, None, 0), (416944369, None, 1), (416947953, None, 0), (416947953, None, 1), (416950513, None, 0), (416950513, None, 1), (416951281, None, 0), (416951281, None, 1), (416952561, None, 0), (416952561, None, 1), (416961521, None, 0), (416961521, None, 1), (416964849, None, 0), (416964849, None, 1), (416965105, None, 0), (416965105, None, 1), (416985329, None, 0), (416985329, None, 1), (416986609, None, 0), (416986609, None, 1), (416993521, None, 0), (416993521, None, 1), (417001457, None, 0), (417001457, None, 1)] (obd_mux=True)
NoneType: None
ECU addr scan ‖ sending tester-present to: [(587, None, 0), (1792, None, 0), (1793, None, 0), (1798, None, 0), (1798, None, 1), (1799, None, 0), (1799, None, 1), (1810, None, 1), (1813, None, 1), (1824, None, 0), (1825, None, 0), (1840, None, 0), (1840, None, 1), (1842, None, 0), (1842, None, 1), (1843, None, 0), (1856, None, 0), (1856, None, 1), (1858, None, 0), (1858, None, 1), (1859, None, 0), (1859, None, 1), (1860, None, 0), (1862, None, 0), (1862, None, 1), (1863, None, 0), (1871, None, 1), (1875, None, 0), (1879, None, 1), (1882, None, 0), (1888, None, 0), (1888, None, 1), (1889, None, 0), (1892, None, 0), (1892, None, 1), (1920, None, 0), (1927, None, 0), (1927, None, 1), (1937, None, 0), (1953, None, 0), (1954, None, 0), (1954, None, 1), (1955, None, 0), (1955, None, 1), (1968, None, 0), (1968, None, 1), (1969, None, 0), (1969, None, 1), (1971, None, 0), (1971, None, 1), (1975, None, 0), (1975, None, 1), (1988, None, 0), (1988, None, 1), (1990, None, 0), (1990, None, 1), (2000, None, 0), (2000, None, 1), (2001, None, 0), (2001, None, 1), (2002, None, 0), (2004, None, 0), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (2018, None, 0), (2020, None, 0), (416943089, None, 0), (416943089, None, 1), (416944369, None, 0), (416944369, None, 1), (416947953, None, 0), (416947953, None, 1), (416950513, None, 0), (416950513, None, 1), (416951281, None, 0), (416951281, None, 1), (416952561, None, 0), (416952561, None, 1), (416961521, None, 0), (416961521, None, 1), (416964849, None, 0), (416964849, None, 1), (416965105, None, 0), (416965105, None, 1), (416985329, None, 0), (416985329, None, 1), (416986609, None, 0), (416986609, None, 1), (416993521, None, 0), (416993521, None, 1), (417001457, None, 0), (417001457, None, 1)] (obd_mux=True)
NoneType: None
ECU addr scan ‖ TX frames: ['0x7e4', '0x746', '0x760', '0x18dad0f1', '0x18daeff1', '0x700', '0x733', '0x18dab5f1', '0x7c6', '0x18dab0f1', '0x740', '0x18da30f1', '0x74f', '0x7b7', '0x742', '0x18da53f1', '0x7d1', '0x18da2bf1', '0x18da1ef1', '0x743', '0x706', '0x18da60f1', '0x7e0', '0x7a3', '0x7c4', '0x18da0bf1', '0x715', '0x7b0', '0x7d4', '0x7e1', '0x732', '0x7b3', '0x7d2', '0x730', '0x747', '0x18daeff1', '0x791', '0x787', '0x7b1', '0x18dab0f1', '0x7a2', '0x18da28f1', '0x18da61f1', '0x18dad0f1', '0x7d0', '0x18da10f1', '0x780', '0x764', '0x18da1ef1', '0x743', '0x7b7', '0x7c4', '0x746', '0x761', '0x706', '0x18da60f1', '0x753', '0x7a3', '0x707', '0x720', '0x7b3', '0x7d4', '0x744', '0x7e1', '0x732', '0x760', '0x7b1', '0x18da53f1', '0x18dab5f1', '0x7c6', '0x730', '0x740', '0x7a2', '0x18da28f1', '0x18da61f1', '0x18da30f1', '0x7e2', '0x787', '0x7e0', '0x75a', '0x7d0', '0x721', '0x742', '0x18da0bf1', '0x7a1', '0x7b0', '0x701', '0x7d1', '0x18da2bf1', '0x712', '0x18da10f1', '0x757', '0x764', '0x707', '0x24b']
NoneType: None
ECU addr scan ‖ TX frames: ['0x7e4', '0x746', '0x760', '0x18dad0f1', '0x18daeff1', '0x700', '0x733', '0x18dab5f1', '0x7c6', '0x18dab0f1', '0x740', '0x18da30f1', '0x74f', '0x7b7', '0x742', '0x18da53f1', '0x7d1', '0x18da2bf1', '0x18da1ef1', '0x743', '0x706', '0x18da60f1', '0x7e0', '0x7a3', '0x7c4', '0x18da0bf1', '0x715', '0x7b0', '0x7d4', '0x7e1', '0x732', '0x7b3', '0x7d2', '0x730', '0x747', '0x18daeff1', '0x791', '0x787', '0x7b1', '0x18dab0f1', '0x7a2', '0x18da28f1', '0x18da61f1', '0x18dad0f1', '0x7d0', '0x18da10f1', '0x780', '0x764', '0x18da1ef1', '0x743', '0x7b7', '0x7c4', '0x746', '0x761', '0x706', '0x18da60f1', '0x753', '0x7a3', '0x707', '0x720', '0x7b3', '0x7d4', '0x744', '0x7e1', '0x732', '0x760', '0x7b1', '0x18da53f1', '0x18dab5f1', '0x7c6', '0x730', '0x740', '0x7a2', '0x18da28f1', '0x18da61f1', '0x18da30f1', '0x7e2', '0x787', '0x7e0', '0x75a', '0x7d0', '0x721', '0x742', '0x18da0bf1', '0x7a1', '0x7b0', '0x701', '0x7d1', '0x18da2bf1', '0x712', '0x18da10f1', '0x757', '0x764', '0x707', '0x24b']
NoneType: None
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/spectra.cc: clearing and requeuing camera 1 from 1
ECU addr scan ‖ batch COMPLETE, still missing: [(587, None, 0), (1792, None, 0), (1793, None, 0), (1798, None, 0), (1798, None, 1), (1799, None, 0), (1799, None, 1), (1810, None, 1), (1813, None, 1), (1824, None, 0), (1825, None, 0), (1840, None, 0), (1840, None, 1), (1842, None, 0), (1842, None, 1), (1843, None, 0), (1856, None, 0), (1856, None, 1), (1858, None, 0), (1858, None, 1), (1859, None, 0), (1859, None, 1), (1860, None, 0), (1862, None, 0), (1862, None, 1), (1863, None, 0), (1871, None, 1), (1875, None, 0), (1879, None, 1), (1882, None, 0), (1888, None, 0), (1888, None, 1), (1889, None, 0), (1892, None, 0), (1892, None, 1), (1920, None, 0), (1927, None, 0), (1927, None, 1), (1937, None, 0), (1953, None, 0), (1954, None, 0), (1954, None, 1), (1955, None, 0), (1955, None, 1), (1968, None, 0), (1968, None, 1), (1969, None, 0), (1969, None, 1), (1971, None, 0), (1971, None, 1), (1975, None, 0), (1975, None, 1), (1988, None, 0), (1988, None, 1), (1990, None, 0), (1990, None, 1), (2000, None, 0), (2000, None, 1), (2001, None, 0), (2001, None, 1), (2002, None, 0), (2004, None, 0), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (2018, None, 0), (2020, None, 0), (416943089, None, 0), (416943089, None, 1), (416944369, None, 0), (416944369, None, 1), (416947953, None, 0), (416947953, None, 1), (416950513, None, 0), (416950513, None, 1), (416951281, None, 0), (416951281, None, 1), (416952561, None, 0), (416952561, None, 1), (416961521, None, 0), (416961521, None, 1), (416964849, None, 0), (416964849, None, 1), (416965105, None, 0), (416965105, None, 1), (416985329, None, 0), (416985329, None, 1), (416986609, None, 0), (416986609, None, 1), (416993521, None, 0), (416993521, None, 1), (417001457, None, 0), (417001457, None, 1)]
NoneType: None
ECU addr scan ‖ batch COMPLETE, still missing: [(587, None, 0), (1792, None, 0), (1793, None, 0), (1798, None, 0), (1798, None, 1), (1799, None, 0), (1799, None, 1), (1810, None, 1), (1813, None, 1), (1824, None, 0), (1825, None, 0), (1840, None, 0), (1840, None, 1), (1842, None, 0), (1842, None, 1), (1843, None, 0), (1856, None, 0), (1856, None, 1), (1858, None, 0), (1858, None, 1), (1859, None, 0), (1859, None, 1), (1860, None, 0), (1862, None, 0), (1862, None, 1), (1863, None, 0), (1871, None, 1), (1875, None, 0), (1879, None, 1), (1882, None, 0), (1888, None, 0), (1888, None, 1), (1889, None, 0), (1892, None, 0), (1892, None, 1), (1920, None, 0), (1927, None, 0), (1927, None, 1), (1937, None, 0), (1953, None, 0), (1954, None, 0), (1954, None, 1), (1955, None, 0), (1955, None, 1), (1968, None, 0), (1968, None, 1), (1969, None, 0), (1969, None, 1), (1971, None, 0), (1971, None, 1), (1975, None, 0), (1975, None, 1), (1988, None, 0), (1988, None, 1), (1990, None, 0), (1990, None, 1), (2000, None, 0), (2000, None, 1), (2001, None, 0), (2001, None, 1), (2002, None, 0), (2004, None, 0), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (2018, None, 0), (2020, None, 0), (416943089, None, 0), (416943089, None, 1), (416944369, None, 0), (416944369, None, 1), (416947953, None, 0), (416947953, None, 1), (416950513, None, 0), (416950513, None, 1), (416951281, None, 0), (416951281, None, 1), (416952561, None, 0), (416952561, None, 1), (416961521, None, 0), (416961521, None, 1), (416964849, None, 0), (416964849, None, 1), (416965105, None, 0), (416965105, None, 1), (416985329, None, 0), (416985329, None, 1), (416986609, None, 0), (416986609, None, 1), (416993521, None, 0), (416993521, None, 1), (417001457, None, 0), (417001457, None, 1)]
NoneType: None
ECU addr scan ‖ sending tester-present to: [(1872, 109, 0)] (obd_mux=True)
NoneType: None
ECU addr scan ‖ sending tester-present to: [(1872, 109, 0)] (obd_mux=True)
NoneType: None
ECU addr scan ‖ TX frames: ['0x750']
NoneType: None
ECU addr scan ‖ TX frames: ['0x750']
NoneType: None
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
models loaded, modeld starting
system/camerad/cameras/spectra.cc: clearing and requeuing camera 2 from 1
Starting listener for: camerad
ECU addr scan ‖ batch COMPLETE, still missing: [(1872, 109, 0)]
NoneType: None
ECU addr scan ‖ batch COMPLETE, still missing: [(1872, 109, 0)]
NoneType: None
ECU addr scan ‖ sending tester-present to: [(1872, 15, 0)] (obd_mux=True)
NoneType: None
ECU addr scan ‖ sending tester-present to: [(1872, 15, 0)] (obd_mux=True)
NoneType: None
ECU addr scan ‖ TX frames: ['0x750']
NoneType: None
ECU addr scan ‖ TX frames: ['0x750']
NoneType: None
vision stream set up, main_wide_camera: False, use_extra_client: True
connected main cam with buffer size: 4804608 (1928 x 1208)
connected extra cam with buffer size: 4804608 (1928 x 1208)
system/loggerd/encoderd.cc: encoder road_cam_encoder init 1928x1208
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/loggerd/encoderd.cc: encoder driver_cam_encoder init 1928x1208
system/loggerd/encoderd.cc: encoder wide_road_cam_encoder init 1928x1208
system/camerad/cameras/spectra.cc: camera 0 synced on frame_id_offset 6 timestamp 290223844407
system/camerad/cameras/spectra.cc: camera 1 synced on frame_id_offset 6 timestamp 290223855135
system/camerad/cameras/spectra.cc: camera 2 synced on frame_id_offset 5 timestamp 290223864613
ECU addr scan ‖ batch COMPLETE, still missing: [(1872, 15, 0)]
NoneType: None
ECU addr scan ‖ batch COMPLETE, still missing: [(1872, 15, 0)]
NoneType: None
Setting OBD multiplexing to False
models loaded, dmonitoringmodeld starting
connecting to driver stream
connected with buffer size: 4804608
OBD multiplexing set successfully
ECU addr scan ‖ sending tester-present to: [(1698, None, 0), (1702, None, 0), (1709, None, 0), (1716, None, 0), (1717, None, 0), (1718, None, 0), (1718, None, 1), (1810, None, 0), (1810, None, 1), (1813, None, 0), (1813, None, 1), (1840, None, 1), (1862, None, 1), (1871, None, 0), (1871, None, 1), (1879, None, 0), (1879, None, 1), (1927, None, 1), (1954, None, 1), (1955, None, 1), (1968, None, 1), (1969, None, 1), (1971, None, 1), (1975, None, 1), (1988, None, 1), (1990, None, 1), (2000, None, 1), (2001, None, 1), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (416943089, None, 1), (416944369, None, 1), (416947953, None, 1), (416950513, None, 1), (416951281, None, 1), (416952561, None, 1), (416961521, None, 1), (416964849, None, 1), (416965105, None, 1), (416985329, None, 1), (416986609, None, 1), (417001457, None, 1)] (obd_mux=False)
NoneType: None
ECU addr scan ‖ sending tester-present to: [(1698, None, 0), (1702, None, 0), (1709, None, 0), (1716, None, 0), (1717, None, 0), (1718, None, 0), (1718, None, 1), (1810, None, 0), (1810, None, 1), (1813, None, 0), (1813, None, 1), (1840, None, 1), (1862, None, 1), (1871, None, 0), (1871, None, 1), (1879, None, 0), (1879, None, 1), (1927, None, 1), (1954, None, 1), (1955, None, 1), (1968, None, 1), (1969, None, 1), (1971, None, 1), (1975, None, 1), (1988, None, 1), (1990, None, 1), (2000, None, 1), (2001, None, 1), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (416943089, None, 1), (416944369, None, 1), (416947953, None, 1), (416950513, None, 1), (416951281, None, 1), (416952561, None, 1), (416961521, None, 1), (416964849, None, 1), (416965105, None, 1), (416985329, None, 1), (416986609, None, 1), (417001457, None, 1)] (obd_mux=False)
NoneType: None
ECU addr scan ‖ TX frames: ['0x757', '0x7b0', '0x18dab5f1', '0x7c6', '0x730', '0x746', '0x7e1', '0x18da30f1', '0x7b7', '0x6b4', '0x6b5', '0x7e0', '0x787', '0x18daeff1', '0x715', '0x6b6', '0x6ad', '0x7b3', '0x18dab0f1', '0x7d1', '0x18da2bf1', '0x18da60f1', '0x74f', '0x712', '0x7a3', '0x18da10f1', '0x757', '0x18da53f1', '0x7b1', '0x7c4', '0x7d4', '0x7e1', '0x18da1ef1', '0x6a6', '0x7a2', '0x18da28f1', '0x18da61f1', '0x712', '0x74f', '0x7e0', '0x715', '0x7d0', '0x18da0bf1', '0x6b6', '0x6a2']
NoneType: None
ECU addr scan ‖ TX frames: ['0x757', '0x7b0', '0x18dab5f1', '0x7c6', '0x730', '0x746', '0x7e1', '0x18da30f1', '0x7b7', '0x6b4', '0x6b5', '0x7e0', '0x787', '0x18daeff1', '0x715', '0x6b6', '0x6ad', '0x7b3', '0x18dab0f1', '0x7d1', '0x18da2bf1', '0x18da60f1', '0x74f', '0x712', '0x7a3', '0x18da10f1', '0x757', '0x18da53f1', '0x7b1', '0x7c4', '0x7d4', '0x7e1', '0x18da1ef1', '0x6a6', '0x7a2', '0x18da28f1', '0x18da61f1', '0x712', '0x74f', '0x7e0', '0x715', '0x7d0', '0x18da0bf1', '0x6b6', '0x6a2']
NoneType: None
quectel setup done
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
ECU addr scan ‖ batch COMPLETE, still missing: [(1698, None, 0), (1702, None, 0), (1709, None, 0), (1716, None, 0), (1717, None, 0), (1718, None, 0), (1718, None, 1), (1810, None, 0), (1810, None, 1), (1813, None, 0), (1813, None, 1), (1840, None, 1), (1862, None, 1), (1871, None, 0), (1871, None, 1), (1879, None, 0), (1879, None, 1), (1927, None, 1), (1954, None, 1), (1955, None, 1), (1968, None, 1), (1969, None, 1), (1971, None, 1), (1975, None, 1), (1988, None, 1), (1990, None, 1), (2000, None, 1), (2001, None, 1), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (416943089, None, 1), (416944369, None, 1), (416947953, None, 1), (416950513, None, 1), (416951281, None, 1), (416952561, None, 1), (416961521, None, 1), (416964849, None, 1), (416965105, None, 1), (416985329, None, 1), (416986609, None, 1), (417001457, None, 1)]
NoneType: None
ECU addr scan ‖ batch COMPLETE, still missing: [(1698, None, 0), (1702, None, 0), (1709, None, 0), (1716, None, 0), (1717, None, 0), (1718, None, 0), (1718, None, 1), (1810, None, 0), (1810, None, 1), (1813, None, 0), (1813, None, 1), (1840, None, 1), (1862, None, 1), (1871, None, 0), (1871, None, 1), (1879, None, 0), (1879, None, 1), (1927, None, 1), (1954, None, 1), (1955, None, 1), (1968, None, 1), (1969, None, 1), (1971, None, 1), (1975, None, 1), (1988, None, 1), (1990, None, 1), (2000, None, 1), (2001, None, 1), (2004, None, 1), (2016, None, 0), (2016, None, 1), (2017, None, 0), (2017, None, 1), (416943089, None, 1), (416944369, None, 1), (416947953, None, 1), (416950513, None, 1), (416951281, None, 1), (416952561, None, 1), (416961521, None, 1), (416964849, None, 1), (416965105, None, 1), (416985329, None, 1), (416986609, None, 1), (417001457, None, 1)]
NoneType: None
ECU addr scan ‖ NO RESPONSE from: [(1218, None, 0), (1220, None, 0), (1223, None, 0), (1235, None, 0), (1242, None, 0), (1249, None, 0), (1380, None, 0), (1611, None, 0), (1666, None, 0), (1670, None, 0), (1677, None, 0), (1684, None, 0), (1685, None, 0), (1686, None, 0), (1686, None, 1), (1800, None, 0), (1801, None, 0), (1806, None, 0), (1806, None, 1), (1807, None, 0), (1807, None, 1), (1831, None, 0), (1831, None, 1), (1832, None, 0), (1833, None, 0), (1848, None, 0), (1848, None, 1), (1850, None, 0), (1850, None, 1), (1864, None, 0), (1864, None, 1), (1866, None, 0), (1866, None, 1), (1867, None, 0), (1867, None, 1), (1870, None, 0), (1870, None, 1), (1871, None, 0), (1880, 15, 0), (1880, 109, 0), (1888, None, 0), (1888, None, 1), (1890, None, 0), (1890, None, 1), (1891, None, 0), (1891, None, 1), (1896, None, 0), (1896, None, 1), (1900, None, 0), (1900, None, 1), (1907, None, 0), (1916, None, 0), (1916, None, 1), (1919, None, 0), (1919, None, 1), (1928, None, 0), (1935, None, 0), (1935, None, 1), (1945, None, 0), (1961, None, 0), (1962, None, 0), (1962, None, 1), (1963, None, 0), (1963, None, 1), (1976, None, 0), (1976, None, 1), (1977, None, 0), (1977, None, 1), (1979, None, 0), (1979, None, 1), (1983, None, 0), (1983, None, 1), (1984, None, 0), (1985, None, 0), (1985, None, 1), (1996, None, 0), (1996, None, 1), (1998, None, 0), (1998, None, 1), (2008, None, 0), (2008, None, 1), (2009, None, 0), (2009, None, 1), (2010, None, 0), (2012, None, 0), (2012, None, 1), (2024, None, 0), (2024, None, 1), (2025, None, 0), (2025, None, 1), (2026, None, 0), (2028, None, 0), (2048, None, 0), (2048, None, 1), (417001739, None, 0), (417001739, None, 1), (417001744, None, 0), (417001744, None, 1), (417001758, None, 0), (417001758, None, 1), (417001768, None, 0), (417001768, None, 1), (417001771, None, 0), (417001771, None, 1), (417001776, None, 0), (417001776, None, 1), (417001811, None, 0), (417001811, None, 1), (417001824, None, 0), (417001824, None, 1), (417001825, None, 0), (417001825, None, 1), (417001904, None, 0), (417001904, None, 1), (417001909, None, 0), (417001909, None, 1), (417001936, None, 0), (417001936, None, 1), (417001967, None, 0), (417001967, None, 1)]
NoneType: None
ECU addr scan ‖ NO RESPONSE from: [(1218, None, 0), (1220, None, 0), (1223, None, 0), (1235, None, 0), (1242, None, 0), (1249, None, 0), (1380, None, 0), (1611, None, 0), (1666, None, 0), (1670, None, 0), (1677, None, 0), (1684, None, 0), (1685, None, 0), (1686, None, 0), (1686, None, 1), (1800, None, 0), (1801, None, 0), (1806, None, 0), (1806, None, 1), (1807, None, 0), (1807, None, 1), (1831, None, 0), (1831, None, 1), (1832, None, 0), (1833, None, 0), (1848, None, 0), (1848, None, 1), (1850, None, 0), (1850, None, 1), (1864, None, 0), (1864, None, 1), (1866, None, 0), (1866, None, 1), (1867, None, 0), (1867, None, 1), (1870, None, 0), (1870, None, 1), (1871, None, 0), (1880, 15, 0), (1880, 109, 0), (1888, None, 0), (1888, None, 1), (1890, None, 0), (1890, None, 1), (1891, None, 0), (1891, None, 1), (1896, None, 0), (1896, None, 1), (1900, None, 0), (1900, None, 1), (1907, None, 0), (1916, None, 0), (1916, None, 1), (1919, None, 0), (1919, None, 1), (1928, None, 0), (1935, None, 0), (1935, None, 1), (1945, None, 0), (1961, None, 0), (1962, None, 0), (1962, None, 1), (1963, None, 0), (1963, None, 1), (1976, None, 0), (1976, None, 1), (1977, None, 0), (1977, None, 1), (1979, None, 0), (1979, None, 1), (1983, None, 0), (1983, None, 1), (1984, None, 0), (1985, None, 0), (1985, None, 1), (1996, None, 0), (1996, None, 1), (1998, None, 0), (1998, None, 1), (2008, None, 0), (2008, None, 1), (2009, None, 0), (2009, None, 1), (2010, None, 0), (2012, None, 0), (2012, None, 1), (2024, None, 0), (2024, None, 1), (2025, None, 0), (2025, None, 1), (2026, None, 0), (2028, None, 0), (2048, None, 0), (2048, None, 1), (417001739, None, 0), (417001739, None, 1), (417001744, None, 0), (417001744, None, 1), (417001758, None, 0), (417001758, None, 1), (417001768, None, 0), (417001768, None, 1), (417001771, None, 0), (417001771, None, 1), (417001776, None, 0), (417001776, None, 1), (417001811, None, 0), (417001811, None, 1), (417001824, None, 0), (417001824, None, 1), (417001825, None, 0), (417001825, None, 1), (417001904, None, 0), (417001904, None, 1), (417001909, None, 0), (417001909, None, 1), (417001936, None, 0), (417001936, None, 1), (417001967, None, 0), (417001967, None, 1)]
NoneType: None
VIN VR3UHZKXZMT064439
VIN VR3UHZKXZMT064439
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1278: 3, 757: 7, 1010: 8, 1038: 5, 1554: 8, 1128: 8, 1161: 8, 973: 8, 781: 8, 1037: 8, 773: 7, 877: 4, 520: 8, 610: 1, 841: 8, 1099: 8, 770: 7, 840: 8, 845: 8, 1035: 4, 1054: 8, 1067: 8, 941: 8, 909: 8, 1042: 8, 1298: 4, 1257: 4, 1416: 8, 1390: 6, 1173: 4, 1086: 6, 1118: 6, 1150: 8, 1304: 4, 1394: 8, 1122: 4, 1272: 5, 749: 7, 1186: 2, 1101: 8, 936: 6, 850: 2, 1006: 4, 1074: 8, 166: 2, 1134: 2, 1293: 8, 1422: 8, 1326: 8, 1387: 4, 1522: 5, 1430: 4, 1454: 5, 1941: 6, 974: 8, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1108: 8, 1172: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1515: 8, 1230: 8, 1483: 8, 1458: 8, 1102: 3, 1486: 3}, 1: {1554: 8, 632: 8, 728: 7, 525: 8, 813: 8, 758: 8, 514: 5, 546: 5, 1032: 6, 946: 2, 1106: 6, 694: 8, 760: 7, 792: 5, 461: 3, 914: 2, 717: 1, 1393: 1, 845: 8, 664: 6, 690: 1, 909: 8, 1517: 3, 1400: 6, 1294: 8, 962: 2, 1069: 4, 1160: 8, 1218: 4, 1378: 4, 1074: 8, 1426: 8, 1270: 5, 1166: 7, 1330: 5, 1266: 8, 1070: 6, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1410: 4, 1464: 8, 1489: 8, 1490: 4, 1942: 8, 1170: 6}, 2: {1278: 3, 757: 7, 1010: 8, 1038: 5, 1554: 8, 1128: 8, 1161: 8, 973: 8, 781: 8, 1037: 8, 773: 7, 877: 4, 520: 8, 610: 1, 841: 8, 1099: 8, 770: 7, 840: 8, 845: 8, 1035: 4, 1054: 8, 1067: 8, 941: 8, 909: 8, 1042: 8, 1298: 4, 1257: 4, 1416: 8, 1390: 6, 1173: 4, 1086: 6, 1118: 6, 1150: 8, 1304: 4, 1394: 8, 1122: 4, 1272: 5, 749: 7, 1186: 2, 1101: 8, 936: 6, 850: 2, 1006: 4, 1074: 8, 166: 2, 1134: 2, 1293: 8, 1422: 8, 1326: 8, 1387: 4, 1522: 5, 1430: 4, 1454: 5, 1941: 6, 974: 8, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1108: 8, 1172: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1515: 8, 1230: 8, 1483: 8, 1458: 8, 1102: 3, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.7888091359999976}
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1278: 3, 757: 7, 1010: 8, 1038: 5, 1554: 8, 1128: 8, 1161: 8, 973: 8, 781: 8, 1037: 8, 773: 7, 877: 4, 520: 8, 610: 1, 841: 8, 1099: 8, 770: 7, 840: 8, 845: 8, 1035: 4, 1054: 8, 1067: 8, 941: 8, 909: 8, 1042: 8, 1298: 4, 1257: 4, 1416: 8, 1390: 6, 1173: 4, 1086: 6, 1118: 6, 1150: 8, 1304: 4, 1394: 8, 1122: 4, 1272: 5, 749: 7, 1186: 2, 1101: 8, 936: 6, 850: 2, 1006: 4, 1074: 8, 166: 2, 1134: 2, 1293: 8, 1422: 8, 1326: 8, 1387: 4, 1522: 5, 1430: 4, 1454: 5, 1941: 6, 974: 8, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1108: 8, 1172: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1515: 8, 1230: 8, 1483: 8, 1458: 8, 1102: 3, 1486: 3}, 1: {1554: 8, 632: 8, 728: 7, 525: 8, 813: 8, 758: 8, 514: 5, 546: 5, 1032: 6, 946: 2, 1106: 6, 694: 8, 760: 7, 792: 5, 461: 3, 914: 2, 717: 1, 1393: 1, 845: 8, 664: 6, 690: 1, 909: 8, 1517: 3, 1400: 6, 1294: 8, 962: 2, 1069: 4, 1160: 8, 1218: 4, 1378: 4, 1074: 8, 1426: 8, 1270: 5, 1166: 7, 1330: 5, 1266: 8, 1070: 6, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1410: 4, 1464: 8, 1489: 8, 1490: 4, 1942: 8, 1170: 6}, 2: {1278: 3, 757: 7, 1010: 8, 1038: 5, 1554: 8, 1128: 8, 1161: 8, 973: 8, 781: 8, 1037: 8, 773: 7, 877: 4, 520: 8, 610: 1, 841: 8, 1099: 8, 770: 7, 840: 8, 845: 8, 1035: 4, 1054: 8, 1067: 8, 941: 8, 909: 8, 1042: 8, 1298: 4, 1257: 4, 1416: 8, 1390: 6, 1173: 4, 1086: 6, 1118: 6, 1150: 8, 1304: 4, 1394: 8, 1122: 4, 1272: 5, 749: 7, 1186: 2, 1101: 8, 936: 6, 850: 2, 1006: 4, 1074: 8, 166: 2, 1134: 2, 1293: 8, 1422: 8, 1326: 8, 1387: 4, 1522: 5, 1430: 4, 1454: 5, 1941: 6, 974: 8, 1379: 7, 1362: 8, 1012: 8, 820: 8, 1485: 4, 1933: 8, 1358: 8, 1108: 8, 1172: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1515: 8, 1230: 8, 1483: 8, 1458: 8, 1102: 3, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 1.7888091359999976}
skipping model eval. Dropped 30 frames
selfdrive/pandad/panda_safety.cc: Finished FW query, Waiting for params to set safety model
```

## fw_versions fix:

```
def get_fw_versions_ordered(can_recv: CanRecvCallable, can_send: CanSendCallable, set_obd_multiplexing: ObdCallback, vin: str,
                            ecu_rx_addrs: set[EcuAddrBusType], timeout: float = 0.1, num_pandas: int = 1, progress: bool = False) -> list[CarParams.CarFw]:
  """Queries for FW versions ordering brands by likelihood, breaks when exact match is found"""

  all_car_fw = []
  brand_matches = get_brand_ecu_matches(ecu_rx_addrs)

  # Sort brands by number of matching ECUs first, then percentage of matching ECUs in the database
  # This allows brands with only one ECU to be queried first (e.g. Tesla)
  for brand in sorted(brand_matches, key=lambda b: (brand_matches[b].count(True), brand_matches[b].count(True) / len(brand_matches[b])), reverse=True):
    # Skip this brand if there are no matching present ECUs
    ############## FIX ##############
    # if True not in brand_matches[brand]:
    #   continue
    ############## FIX ##############

    car_fw = get_fw_versions(can_recv, can_send, set_obd_multiplexing, query_brand=brand, timeout=timeout, num_pandas=num_pandas, progress=progress)
    all_car_fw.extend(car_fw)

    # If there is a match using this brand's FW alone, finish querying early
    _, matches = match_fw_to_car(car_fw, vin, log=False)
    if len(matches) == 1:
      break

  return all_car_fw
```
## fw_versions
```
python selfdrive/debug/car/fw_versions.py

Found FW versions
{
  Brand: psa, bus: 1, OBD: False - (Ecu.fwdRadar, 0x6b6, None): [b'212053276']
  Brand: psa, bus: 1, OBD: False - (Ecu.fwdRadar, 0x6b6, None): [b'\xff\xff\x00\x00\x0f\xe8\x18\x05!@Y\xa4\x03\xff\xff\xff\x00\x02\x00\x00\x01\x94\x80\x97']
  Brand: psa, bus: 0, OBD: False - (Ecu.adas, 0x6a6, None): [b'210306062100']
  Brand: psa, bus: 0, OBD: False - (Ecu.transmission, 0x6ad, None): [b'085095700857210527']
  Brand: psa, bus: 0, OBD: False - (Ecu.abs, 0x6b4, None): [b'521021900860']
  Brand: psa, bus: 0, OBD: False - (Ecu.eps, 0x6a2, None): [b'9210126909']
  Brand: psa, bus: 0, OBD: False - (Ecu.engine, 0x6b5, None): [b'6077GC0817309']
  Brand: psa, bus: 0, OBD: False - (Ecu.transmission, 0x6ad, None): [b"\x00\x00\x00\x00\x03\x93!\x08 \x01\xc2\x12\x12\xff\xff\xff\x00\x02\x00\x00\x01\x94w'"]
  Brand: psa, bus: 0, OBD: False - (Ecu.abs, 0x6b4, None): [b'\xff\xff\x00\x00t\x01\x11\x01!\x01\x040\x15\xff\xff\xff\x00\x02\x00\x00\xfe\x95\x08w']
  Brand: psa, bus: 0, OBD: False - (Ecu.adas, 0x6a6, None): [b'\xff\xff\x00\x00\r\n\x06\x03!\x03\x01\x12\x01\xff\xff\xff\x00\x02\x00\x00\x02\x94\x86b']
  Brand: psa, bus: 0, OBD: False - (Ecu.eps, 0x6a2, None): [b'\xf2i\x00\x00\r\x99\x11\x05\x15\x01!\xb2\x01!\x07#\xfd\xd4S\xe2\x02\x96E ']
  Brand: psa, bus: 0, OBD: False - (Ecu.engine, 0x6b5, None): [b'\xbfP\x00\x00\x13j\x07\x06\x15\xb5@\xf5\x03\xff\xff\xff\x00\x02\x00\x00\x01\x944g']
}

Possible matches: set()
Getting fw took 22.027 s
```

## Cloudlog, with fingerprint
```
Waiting for CAN messages...
selfdrived is waiting for CarParams
Getting VIN & FW versions
Getting VIN & FW versions
Setting OBD multiplexing to True
starting python system.qcomgpsd.qcomgpsd
starting python selfdrive.locationd.paramsd
starting python selfdrive.locationd.lagd
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 0 success
system/camerad/cameras/spectra.cc: get session: 0 0xFC0200
system/camerad/cameras/spectra.cc: -- Accessing sensor
starting python selfdrive.controls.plannerd
waiting for modem to come up
starting python selfdrive.controls.radard
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
plannerd is waiting for CarParams
radard is waiting for CarParams
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
updated is dead with 0
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 0
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xFC0200 isp: 0xED0102 sensors: 0x430101 link: 0x910104
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 0
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL version: "OpenGL ES 3.2 "
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL vendor: "Qualcomm"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL renderer: "Adreno (TM) 630"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL language version: "OpenGL ES GLSL ES 3.20"
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 36) 0x24000d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 37) 0x25000e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 38) 0x26000f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 39) 0x270010 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 40) 0x280011 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 41) 0x290012 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 42) 0x2a0013 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 43) 0x2b0014 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 44) 0x2c0015 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 45) 0x2d0016 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 46) 0x2e0017 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 47) 0x2f0018 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 48) 0x300019 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 49) 0x31001a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 50) 0x32001b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 51) 0x33001c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 52) 0x34001d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 53) 0x35001e 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 0 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 1
system/camerad/cameras/spectra.cc: -- Probing sensor 1
selfdrive/ui/qt/widgets/cameraview.cc: connecting to stream 0, was connected to 0
OBD multiplexing set successfully
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0322f19000000000
CAN-TX: 0x7df - 0x0322f19000000000
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0322f19000000000
CAN-TX: 0x18db33f1 - 0x0322f19000000000
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 1 success
system/camerad/cameras/spectra.cc: get session: 0 0x520205
system/camerad/cameras/spectra.cc: -- Accessing sensor
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0209020000000000
CAN-TX: 0x7df - 0x0209020000000000
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-RX: 0x7e8 - 0x1014490201565233
CAN-RX: 0x7e8 - 0x1014490201565233
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: TX - flow control continue - 0x7e0
ISO-TP: TX - flow control continue - 0x7e0
CAN-TX: 0x7e0 - 0x30000a0000000000
CAN-TX: 0x7e0 - 0x30000a0000000000
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
system/loggerd/loggerd.cc: logging to /data/media/0/realdata/00000092--efd340dee4--0
CAN-RX: 0x7e8 - 0x2254303634343339
CAN-RX: 0x7e8 - 0x2254303634343339
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 1
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0x520205 isp: 0xCB0107 sensors: 0x90106 link: 0x420109
system/camerad/cameras/spectra.cc: link control: 0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 1
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 62) 0x3e0025 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 63) 0x3f0026 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 64) 0x400027 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 65) 0x410028 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 66) 0x420029 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 67) 0x43002a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 68) 0x44002b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 69) 0x45002c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 70) 0x46002d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 71) 0x47002e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 72) 0x48002f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 73) 0x490030 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 74) 0x4a0031 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 75) 0x4b0032 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 76) 0x4c0033 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 77) 0x4d0034 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 78) 0x4e0035 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 79) 0x4f0036 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 1 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 2
system/camerad/cameras/spectra.cc: -- Probing sensor 2
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
got vin with request=b'\t\x02'
got vin with request=b'\t\x02'
system/loggerd/loggerd.cc: large volume of 'logMessage' messages
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 2 success
system/camerad/cameras/spectra.cc: get session: 0 0xE020A
system/camerad/cameras/spectra.cc: -- Accessing sensor
micd stream started: stream.samplerate=44100.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
soundd stream started: stream.samplerate=48000.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: acquire icp dev
system/camerad/cameras/spectra.cc: opened csiphy for 2
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xE020A isp: 0x9C010C sensors: 0x11010B link: 0xE8010F
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: start icp: 0
system/camerad/cameras/spectra.cc: camera init 2
system/camerad/cameras/camera_common.cc: allocated 18 CL buffers
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 89) 0x590043 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 107) 0x6b0044 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 90) 0x5a0045 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 108) 0x6c0046 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 91) 0x5b0047 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 109) 0x6d0048 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 92) 0x5c0049 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 110) 0x6e004a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 93) 0x5d004b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 111) 0x6f004c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 94) 0x5e004d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 112) 0x70004e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 95) 0x5f004f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 113) 0x710050 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 96) 0x600051 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 114) 0x720052 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 97) 0x610053 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 115) 0x730054 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 98) 0x620055 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 116) 0x740056 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 99) 0x630057 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 117) 0x750058 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 100) 0x640059 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 118) 0x76005a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 101) 0x65005b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 119) 0x77005c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 102) 0x66005d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 120) 0x78005e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 103) 0x67005f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 121) 0x790060 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 104) 0x680061 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 122) 0x7a0062 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 105) 0x690063 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 123) 0x7b0064 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 106) 0x6a0065 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 124) 0x7c0066 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 2 from 1
system/camerad/cameras/spectra.cc: flushed bps: 0
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/camera_qcom2.cc: -- Starting devices
system/camerad/cameras/spectra.cc: starting sensor 0
Starting listener for: camerad
system/camerad/cameras/spectra.cc: starting sensor 1
system/camerad/cameras/spectra.cc: starting sensor 2
system/camerad/cameras/camera_qcom2.cc: -- Dequeueing Video events
models loaded, modeld starting
vision stream set up, main_wide_camera: False, use_extra_client: True
connected main cam with buffer size: 4804608 (1928 x 1208)
connected extra cam with buffer size: 4804608 (1928 x 1208)
common/clutil.cc: platform[0] CL_PLATFORM_NAME: QUALCOMM Snapdragon(TM)
common/clutil.cc: vendor: QUALCOMM
common/clutil.cc: platform version: OpenCL 2.0 QUALCOMM build: commit #f437276 changeid # Date: 12/06/18 Thu Local Branch:  Remote Branch: 
common/clutil.cc: profile: FULL_PROFILE
common/clutil.cc: extensions:  
common/clutil.cc: name: QUALCOMM Adreno(TM)
common/clutil.cc: device version: OpenCL 2.0 Adreno(TM) 630
common/clutil.cc: max work group size: 1024
common/clutil.cc: type = 4, CL_DEVICE_TYPE_GPU
system/loggerd/encoderd.cc: encoder road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 35
system/loggerd/encoderd.cc: encoder driver_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 4
system/loggerd/encoderd.cc: encoder wide_road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 5
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/camerad/cameras/spectra.cc: camera 0 synced on frame_id_offset 5 timestamp 2719074499254
system/camerad/cameras/spectra.cc: camera 1 synced on frame_id_offset 5 timestamp 2719074457589
system/camerad/cameras/spectra.cc: camera 2 synced on frame_id_offset 5 timestamp 2719074469203
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 79
selfdrive/ui/qt/widgets/cameraview.cc: Drawing same frame twice 0
system/loggerd/encoderd.cc: camera 1 encoder ready
system/loggerd/encoderd.cc: camera 2 encoder ready
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 177408
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/loggerd/encoderd.cc: camera 0 encoder ready
system/loggerd/encoderd.cc: camera 0 waiting for frame 3, cur 1
system/loggerd/encoderd.cc: camera 1 waiting for frame 3, cur 2
system/loggerd/encoderd.cc: camera 2 waiting for frame 3, cur 2
system/loggerd/encoderd.cc: camera 0 waiting for frame 3, cur 2
system/loggerd/loggerd.cc: driverEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000092--efd340dee4--0/dcamera.hevc remuxing:0
system/loggerd/loggerd.cc: qRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000092--efd340dee4--0/qcamera.ts remuxing:1
system/loggerd/loggerd.cc: wideRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000092--efd340dee4--0/ecamera.hevc remuxing:0
system/loggerd/loggerd.cc: roadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000092--efd340dee4--0/fcamera.hevc remuxing:0
Setting OBD multiplexing to False
OBD multiplexing set successfully
models loaded, dmonitoringmodeld starting
connecting to driver stream
connected with buffer size: 4804608
quectel setup done
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
VIN VR3UHZKXZMT064439
VIN VR3UHZKXZMT064439
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1067: 8, 757: 7, 1128: 8, 973: 8, 845: 8, 941: 8, 820: 8, 909: 8, 773: 7, 520: 8, 610: 1, 841: 8, 1042: 8, 1298: 4, 770: 7, 840: 8, 781: 8, 1037: 8, 1390: 6, 1394: 8, 1257: 4, 1416: 8, 749: 7, 1101: 8, 1173: 4, 1304: 4, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1186: 2, 1010: 8, 166: 2, 1012: 8, 1161: 8, 1099: 8, 1522: 5, 1035: 4, 1054: 8, 1430: 4, 1278: 3, 1134: 2, 1108: 8, 1172: 8, 1038: 5, 1554: 8, 1293: 8, 1230: 8, 1387: 4, 1485: 4, 1933: 8, 1458: 8, 1102: 3, 1486: 3, 936: 6, 1941: 6, 1422: 8, 1326: 8, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1515: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8}, 1: {946: 2, 1106: 6, 632: 8, 728: 7, 525: 8, 461: 3, 717: 1, 914: 2, 845: 8, 909: 8, 514: 5, 546: 5, 1032: 6, 758: 8, 760: 7, 792: 5, 694: 8, 813: 8, 664: 6, 690: 1, 1294: 8, 1400: 6, 1270: 5, 962: 2, 1074: 8, 1160: 8, 1426: 8, 1218: 4, 1378: 4, 1069: 4, 1166: 7, 1330: 5, 1266: 8, 1070: 6, 1554: 8, 1393: 1, 1517: 3, 1490: 4, 1170: 6, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8}, 2: {1067: 8, 757: 7, 1128: 8, 973: 8, 845: 8, 941: 8, 820: 8, 909: 8, 773: 7, 520: 8, 610: 1, 841: 8, 1042: 8, 1298: 4, 770: 7, 840: 8, 781: 8, 1037: 8, 1390: 6, 1394: 8, 1257: 4, 1416: 8, 749: 7, 1101: 8, 1173: 4, 1304: 4, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1186: 2, 1010: 8, 166: 2, 1012: 8, 1161: 8, 1099: 8, 1522: 5, 1035: 4, 1054: 8, 1430: 4, 1278: 3, 1134: 2, 1108: 8, 1172: 8, 1038: 5, 1554: 8, 1293: 8, 1230: 8, 1387: 4, 1485: 4, 1933: 8, 1458: 8, 1102: 3, 1486: 3, 936: 6, 1941: 6, 1422: 8, 1326: 8, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1515: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 2.0508603389998825}
{'event': 'fingerprinted', 'car_fingerprint': 'PSA_OPEL_CORSA_F', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1067: 8, 757: 7, 1128: 8, 973: 8, 845: 8, 941: 8, 820: 8, 909: 8, 773: 7, 520: 8, 610: 1, 841: 8, 1042: 8, 1298: 4, 770: 7, 840: 8, 781: 8, 1037: 8, 1390: 6, 1394: 8, 1257: 4, 1416: 8, 749: 7, 1101: 8, 1173: 4, 1304: 4, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1186: 2, 1010: 8, 166: 2, 1012: 8, 1161: 8, 1099: 8, 1522: 5, 1035: 4, 1054: 8, 1430: 4, 1278: 3, 1134: 2, 1108: 8, 1172: 8, 1038: 5, 1554: 8, 1293: 8, 1230: 8, 1387: 4, 1485: 4, 1933: 8, 1458: 8, 1102: 3, 1486: 3, 936: 6, 1941: 6, 1422: 8, 1326: 8, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1515: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8}, 1: {946: 2, 1106: 6, 632: 8, 728: 7, 525: 8, 461: 3, 717: 1, 914: 2, 845: 8, 909: 8, 514: 5, 546: 5, 1032: 6, 758: 8, 760: 7, 792: 5, 694: 8, 813: 8, 664: 6, 690: 1, 1294: 8, 1400: 6, 1270: 5, 962: 2, 1074: 8, 1160: 8, 1426: 8, 1218: 4, 1378: 4, 1069: 4, 1166: 7, 1330: 5, 1266: 8, 1070: 6, 1554: 8, 1393: 1, 1517: 3, 1490: 4, 1170: 6, 1518: 4, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8}, 2: {1067: 8, 757: 7, 1128: 8, 973: 8, 845: 8, 941: 8, 820: 8, 909: 8, 773: 7, 520: 8, 610: 1, 841: 8, 1042: 8, 1298: 4, 770: 7, 840: 8, 781: 8, 1037: 8, 1390: 6, 1394: 8, 1257: 4, 1416: 8, 749: 7, 1101: 8, 1173: 4, 1304: 4, 1122: 4, 1272: 5, 850: 2, 1006: 4, 1074: 8, 877: 4, 1086: 6, 1118: 6, 1150: 8, 1186: 2, 1010: 8, 166: 2, 1012: 8, 1161: 8, 1099: 8, 1522: 5, 1035: 4, 1054: 8, 1430: 4, 1278: 3, 1134: 2, 1108: 8, 1172: 8, 1038: 5, 1554: 8, 1293: 8, 1230: 8, 1387: 4, 1485: 4, 1933: 8, 1458: 8, 1102: 3, 1486: 3, 936: 6, 1941: 6, 1422: 8, 1326: 8, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1515: 8, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 2.0508603389998825}
modeld got CarParams: psa
selfdrive/pandad/panda_safety.cc: Finished FW query, Waiting for params to set safety model
```

## Cloudlog, without fingerprint
```
Waiting for CAN messages...
starting python system.qcomgpsd.qcomgpsd
starting python selfdrive.locationd.paramsd
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 0 success
system/camerad/cameras/spectra.cc: get session: 0 0xB80200
system/camerad/cameras/spectra.cc: -- Accessing sensor
starting python selfdrive.locationd.lagd
waiting for modem to come up
starting python selfdrive.controls.plannerd
Getting VIN & FW versions
Getting VIN & FW versions
Setting OBD multiplexing to True
starting python selfdrive.controls.radard
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned updated uploader statsd
plannerd is waiting for CarParams
updated is dead with 0
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
radard is waiting for CarParams
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL version: "OpenGL ES 3.2 "
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL vendor: "Qualcomm"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL renderer: "Adreno (TM) 630"
selfdrive/ui/qt/onroad/annotated_camera.cc: OpenGL language version: "OpenGL ES GLSL ES 3.20"
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: opened csiphy for 0
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xB80200 isp: 0xE90102 sensors: 0x720101 link: 0xED0104
system/camerad/cameras/spectra.cc: link control: 0
selfdrive/ui/qt/widgets/cameraview.cc: connecting to stream 0, was connected to 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 0
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 36) 0x24000d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 37) 0x25000e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 38) 0x26000f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 39) 0x270010 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 40) 0x280011 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 41) 0x290012 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 42) 0x2a0013 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 43) 0x2b0014 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 44) 0x2c0015 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 45) 0x2d0016 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 46) 0x2e0017 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 47) 0x2f0018 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 48) 0x300019 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 49) 0x31001a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 50) 0x32001b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 51) 0x33001c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 52) 0x34001d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 53) 0x35001e 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 0 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 1
system/camerad/cameras/spectra.cc: -- Probing sensor 1
OBD multiplexing set successfully
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: REQUEST - 0x7df 0x22f190
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0322f19000000000
CAN-TX: 0x7df - 0x0322f19000000000
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: REQUEST - 0x18db33f1 0x22f190
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0322f19000000000
CAN-TX: 0x18db33f1 - 0x0322f19000000000
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 1 success
system/camerad/cameras/spectra.cc: get session: 0 0xF30205
system/camerad/cameras/spectra.cc: -- Accessing sensor
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: REQUEST - 0x7df 0x0902
ISO-TP: TX - single frame - 0x7df
ISO-TP: TX - single frame - 0x7df
CAN-TX: 0x7df - 0x0209020000000000
CAN-TX: 0x7df - 0x0209020000000000
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: REQUEST - 0x18db33f1 0x0902
ISO-TP: TX - single frame - 0x18db33f1
ISO-TP: TX - single frame - 0x18db33f1
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-TX: 0x18db33f1 - 0x0209020000000000
CAN-RX: 0x7e8 - 0x1014490201565233
CAN-RX: 0x7e8 - 0x1014490201565233
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: RX - first frame - 0x7e8 idx=0 done=False
ISO-TP: TX - flow control continue - 0x7e0
ISO-TP: TX - flow control continue - 0x7e0
CAN-TX: 0x7e0 - 0x30000a0000000000
CAN-TX: 0x7e0 - 0x30000a0000000000
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
ISO-TP: RESPONSE - 0x7e8 0x490201565233
ISO-TP: RESPONSE - 0x7e8 0x490201565233
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
CAN-RX: 0x7e8 - 0x2155485a4b585a4d
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x7e8 idx=1 done=False
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d
CAN-RX: 0x7e8 - 0x2254303634343339
CAN-RX: 0x7e8 - 0x2254303634343339
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RX - consecutive frame - 0x7e8 idx=2 done=True
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: acquire isp dev
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: opened csiphy for 1
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xF30205 isp: 0x740107 sensors: 0x9A0106 link: 0xA40109
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: camera init 1
system/loggerd/loggerd.cc: logging to /data/media/0/realdata/00000095--9d6f77344d--0
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
ISO-TP: RESPONSE - 0x7e8 0x49020156523355485a4b585a4d54303634343339
got vin with request=b'\t\x02'
got vin with request=b'\t\x02'
system/loggerd/loggerd.cc: large volume of 'logMessage' messages
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
micd stream started: stream.samplerate=44100.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
soundd stream started: stream.samplerate=48000.0 stream.channels=1 stream.dtype='float32' stream.device=31, stream.blocksize=4096
common/clutil.cc: platform[0] CL_PLATFORM_NAME: QUALCOMM Snapdragon(TM)
common/clutil.cc: vendor: QUALCOMM
common/clutil.cc: platform version: OpenCL 2.0 QUALCOMM build: commit #f437276 changeid # Date: 12/06/18 Thu Local Branch:  Remote Branch: 
common/clutil.cc: profile: FULL_PROFILE
common/clutil.cc: extensions:  
common/clutil.cc: name: QUALCOMM Adreno(TM)
common/clutil.cc: device version: OpenCL 2.0 Adreno(TM) 630
common/clutil.cc: max work group size: 1024
common/clutil.cc: type = 4, CL_DEVICE_TYPE_GPU
models loaded, modeld starting
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 62) 0x3e0025 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 63) 0x3f0026 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 64) 0x400027 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 65) 0x410028 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 66) 0x420029 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 67) 0x43002a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 68) 0x44002b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 69) 0x45002c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 70) 0x46002d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 71) 0x47002e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 72) 0x48002f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 73) 0x490030 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 74) 0x4a0031 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 75) 0x4b0032 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 76) 0x4c0033 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 77) 0x4d0034 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 78) 0x4e0035 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 79) 0x4f0036 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 1 from 1
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/spectra.cc: opened sensor for 2
system/camerad/cameras/spectra.cc: -- Probing sensor 2
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system.micd lagging by 297.35 ms
system.micd lagging by 197.56 ms
system.micd lagging by 97.62 ms
system/camerad/cameras/spectra.cc: VIDIOC_CAM_CONTROL error: op_code 266 - errno 19
system/camerad/cameras/spectra.cc: probing the sensor: -1
system/camerad/cameras/spectra.cc: probing the sensor: 0
system/camerad/cameras/spectra.cc: -- Probing sensor 2 success
system/camerad/cameras/spectra.cc: get session: 0 0xBB020A
system/camerad/cameras/spectra.cc: -- Accessing sensor
system/camerad/cameras/spectra.cc: acquire sensor dev
system/camerad/cameras/spectra.cc: -- Configuring sensor
Setting OBD multiplexing to False
system/camerad/cameras/spectra.cc: acquire isp dev
system/camerad/cameras/spectra.cc: acquire icp dev
system/camerad/cameras/spectra.cc: opened csiphy for 2
system/camerad/cameras/spectra.cc: acquire csiphy dev
system/camerad/cameras/spectra.cc: -- Config CSI PHY
system/camerad/cameras/spectra.cc: -- Link devices
system/camerad/cameras/spectra.cc: link: 0 session: 0xBB020A isp: 0xCC010C sensors: 0x8C010B link: 0x78010F
system/camerad/cameras/spectra.cc: link control: 0
system/camerad/cameras/spectra.cc: start csiphy: 0
system/camerad/cameras/spectra.cc: start isp: 0
system/camerad/cameras/spectra.cc: start icp: 0
system/camerad/cameras/spectra.cc: camera init 2
system/camerad/cameras/camera_common.cc: allocated 18 CL buffers
system/camerad/cameras/camera_common.cc: created 18 YUV vipc buffers with size 2048x1216
system/camerad/cameras/spectra.cc: map buf req: (fd: 89) 0x590043 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 107) 0x6b0044 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 90) 0x5a0045 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 108) 0x6c0046 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 91) 0x5b0047 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 109) 0x6d0048 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 92) 0x5c0049 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 110) 0x6e004a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 93) 0x5d004b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 111) 0x6f004c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 94) 0x5e004d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 112) 0x70004e 0
models loaded, dmonitoringmodeld starting
system/camerad/cameras/spectra.cc: map buf req: (fd: 95) 0x5f004f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 113) 0x710050 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 96) 0x600051 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 114) 0x720052 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 97) 0x610053 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 115) 0x730054 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 98) 0x620055 0
connecting to driver stream
system/camerad/cameras/spectra.cc: map buf req: (fd: 116) 0x740056 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 99) 0x630057 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 117) 0x750058 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 100) 0x640059 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 118) 0x76005a 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 101) 0x65005b 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 119) 0x77005c 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 102) 0x66005d 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 120) 0x78005e 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 103) 0x67005f 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 121) 0x790060 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 104) 0x680061 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 122) 0x7a0062 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 105) 0x690063 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 123) 0x7b0064 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 106) 0x6a0065 0
system/camerad/cameras/spectra.cc: map buf req: (fd: 124) 0x7c0066 0
system/camerad/cameras/spectra.cc: clearing and requeuing camera 2 from 1
system/camerad/cameras/spectra.cc: flushed bps: 0
system/camerad/cameras/spectra.cc: flushed all req: 100
system/camerad/cameras/camera_qcom2.cc: -- Starting devices
system/camerad/cameras/spectra.cc: starting sensor 0
Starting listener for: camerad
system/camerad/cameras/spectra.cc: starting sensor 1
system/camerad/cameras/spectra.cc: starting sensor 2
system/camerad/cameras/camera_qcom2.cc: -- Dequeueing Video events
vision stream set up, main_wide_camera: False, use_extra_client: True
connected main cam with buffer size: 4804608 (1928 x 1208)
connected extra cam with buffer size: 4804608 (1928 x 1208)
selfdrive/pandad/spi.cc: SPI: got NACK, waiting for 0x85
selfdrive/pandad/spi.cc:   652 / 0x0 / 7 / 64 / tx: 13131300004000
OBD multiplexing set successfully
selfdrive/pandad/spi.cc: SPI: got NACK, waiting for 0x79
selfdrive/pandad/spi.cc:   653 / 0x0 / 7 / 64 / tx: 110007004000b6
system/loggerd/encoderd.cc: encoder road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 35
system/loggerd/encoderd.cc: encoder driver_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 4
system/loggerd/encoderd.cc: encoder wide_road_cam_encoder init 1928x1208
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 5
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 2373632
connected with buffer size: 4804608
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
system/loggerd/encoder/v4l_encoder.cc: opened encoder device msm_vidc_driver msm_vidc_venc = 79
system/camerad/cameras/spectra.cc: camera 0 synced on frame_id_offset 5 timestamp 3117981184959
system/camerad/cameras/spectra.cc: camera 1 synced on frame_id_offset 5 timestamp 3117981228758
system/camerad/cameras/spectra.cc: camera 2 synced on frame_id_offset 5 timestamp 3117981198395
setup_quectel failed, trying again
Traceback (most recent call last):
  File "/data/openpilot/openpilot/common/retry.py", line 13, in wrapper
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/system/qcomgpsd/qcomgpsd.py", line 191, in setup_quectel
    send_recv(diag, DIAG_SUBSYS_CMD_F, pack('<BHBBIIII',
  File "/data/openpilot/openpilot/system/qcomgpsd/modemdiag.py", line 65, in send_recv
    opcode, payload = diag.recv()
                      ^^^^^^^^^^^
  File "/data/openpilot/openpilot/system/qcomgpsd/modemdiag.py", line 48, in recv
    unframed_message = self.hdlc_decapsulate(raw_payload)
                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/data/openpilot/openpilot/system/qcomgpsd/modemdiag.py", line 35, in hdlc_decapsulate
    assert payload[-2:] == pack('<H', ModemDiag.ccitt_crc16(payload[:-2]))
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AssertionError
system/loggerd/encoderd.cc: camera 2 encoder ready
selfdrive/ui/qt/widgets/cameraview.cc: Drawing same frame twice 0
system/loggerd/encoderd.cc: camera 1 encoder ready
system/loggerd/encoder/v4l_encoder.cc: in buffer size 4804608, out buffer size 177408
system/loggerd/encoderd.cc: camera 0 encoder ready
system/loggerd/encoderd.cc: camera 1 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 2 waiting for frame 2, cur 1
system/loggerd/encoderd.cc: camera 0 waiting for frame 2, cur 1
system/loggerd/loggerd.cc: driverEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000095--9d6f77344d--0/dcamera.hevc remuxing:0
system/loggerd/loggerd.cc: qRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000095--9d6f77344d--0/qcamera.ts remuxing:1
system/loggerd/loggerd.cc: roadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000095--9d6f77344d--0/fcamera.hevc remuxing:0
system/loggerd/loggerd.cc: wideRoadEncodeData: has encoderd offset 0
system/loggerd/video_writer.cc: encoder_open /data/media/0/realdata/00000095--9d6f77344d--0/ecamera.hevc remuxing:0
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
VIN VR3UHZKXZMT064439
VIN VR3UHZKXZMT064439
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
loggerd encoderd logmessaged camerad logcatd proclogd micd timed modeld dmonitoringmodeld sensord ui soundd locationd calibrationd torqued controlsd selfdrived card deleter dmonitoringd qcomgpsd pandad paramsd lagd plannerd radard hardwared tombstoned uploader statsd
{'event': 'fingerprinted', 'car_fingerprint': 'None', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 1: {632: 8, 728: 7, 525: 8, 813: 8, 1266: 8, 514: 5, 546: 5, 1032: 6, 1070: 6, 760: 7, 792: 5, 461: 3, 717: 1, 758: 8, 845: 8, 664: 6, 690: 1, 1074: 8, 694: 8, 962: 2, 1069: 4, 1554: 8, 1218: 4, 946: 2, 1106: 6, 909: 8, 914: 2, 1270: 5, 1393: 1, 1294: 8, 1400: 6, 1426: 8, 1160: 8, 1378: 4, 1166: 7, 1330: 5, 1518: 4, 1517: 3, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4, 1170: 6}, 2: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 2.0968555660001584}
{'event': 'fingerprinted', 'car_fingerprint': 'None', 'source': 0, 'fuzzy': False, 'cached': False, 'fw_count': 0, 'ecu_responses': [], 'vin_rx_addr': 2024, 'vin_rx_bus': 0, 'fingerprints': '{0: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 1: {632: 8, 728: 7, 525: 8, 813: 8, 1266: 8, 514: 5, 546: 5, 1032: 6, 1070: 6, 760: 7, 792: 5, 461: 3, 717: 1, 758: 8, 845: 8, 664: 6, 690: 1, 1074: 8, 694: 8, 962: 2, 1069: 4, 1554: 8, 1218: 4, 946: 2, 1106: 6, 909: 8, 914: 2, 1270: 5, 1393: 1, 1294: 8, 1400: 6, 1426: 8, 1160: 8, 1378: 4, 1166: 7, 1330: 5, 1518: 4, 1517: 3, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4, 1170: 6}, 2: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}', 'fw_query_time': 2.0968555660001584}
{'event': "car doesn't match any fingerprints", 'fingerprints': '{0: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 1: {632: 8, 728: 7, 525: 8, 813: 8, 1266: 8, 514: 5, 546: 5, 1032: 6, 1070: 6, 760: 7, 792: 5, 461: 3, 717: 1, 758: 8, 845: 8, 664: 6, 690: 1, 1074: 8, 694: 8, 962: 2, 1069: 4, 1554: 8, 1218: 4, 946: 2, 1106: 6, 909: 8, 914: 2, 1270: 5, 1393: 1, 1294: 8, 1400: 6, 1426: 8, 1160: 8, 1378: 4, 1166: 7, 1330: 5, 1518: 4, 1517: 3, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4, 1170: 6}, 2: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}'}
{'event': "car doesn't match any fingerprints", 'fingerprints': '{0: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 1: {632: 8, 728: 7, 525: 8, 813: 8, 1266: 8, 514: 5, 546: 5, 1032: 6, 1070: 6, 760: 7, 792: 5, 461: 3, 717: 1, 758: 8, 845: 8, 664: 6, 690: 1, 1074: 8, 694: 8, 962: 2, 1069: 4, 1554: 8, 1218: 4, 946: 2, 1106: 6, 909: 8, 914: 2, 1270: 5, 1393: 1, 1294: 8, 1400: 6, 1426: 8, 1160: 8, 1378: 4, 1166: 7, 1330: 5, 1518: 4, 1517: 3, 1234: 3, 1362: 8, 1202: 8, 1489: 8, 1942: 8, 1410: 4, 1464: 8, 1490: 4, 1170: 6}, 2: {1128: 8, 973: 8, 781: 8, 1037: 8, 520: 8, 610: 1, 841: 8, 773: 7, 757: 7, 770: 7, 840: 8, 845: 8, 941: 8, 749: 7, 1101: 8, 1006: 4, 1074: 8, 1086: 6, 1118: 6, 1150: 8, 1161: 8, 1293: 8, 1010: 8, 1038: 5, 1554: 8, 877: 4, 1099: 8, 1035: 4, 1054: 8, 1067: 8, 909: 8, 1042: 8, 1298: 4, 1390: 6, 1394: 8, 1173: 4, 1257: 4, 1416: 8, 1304: 4, 850: 2, 1122: 4, 1272: 5, 1278: 3, 1186: 2, 1522: 5, 166: 2, 936: 6, 1430: 4, 1134: 2, 1422: 8, 1326: 8, 1387: 4, 1454: 5, 974: 8, 1379: 7, 1483: 8, 1362: 8, 1012: 8, 820: 8, 1941: 6, 1358: 8, 1938: 8, 1347: 4, 1411: 7, 1443: 8, 1314: 8, 1506: 8, 1442: 7, 1473: 8, 1475: 8, 1432: 4, 1922: 8, 1485: 4, 1108: 8, 1172: 8, 1230: 8, 1933: 8, 1515: 8, 1458: 8, 1102: 3, 1486: 3}, 3: {}, 4: {}, 5: {}, 6: {}, 7: {}}'}
restored torque params from cache
plannerd got CarParams: mock
selfdrive/pandad/panda_safety.cc: Finished FW query, Waiting for params to set safety model
```


# Panda Requests
## ARTIV (6B6)
```
python panda/examples/query_fw_versions.py --addr 6b6 --bus 1 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6b6, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6b6 0x3e00
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x023e000000000000
CAN-RX: 0x696 - 0x027e00
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7e00
ISO-TP: REQUEST - 0x6b6 0x1001
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0210010000000000
CAN-RX: 0x696 - 0x06500100c80014
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x500100c80014
ISO-TP: REQUEST - 0x6b6 0x1003
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0210030000000000
CAN-RX: 0x696 - 0x06500300c80014
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x500300c80014
ISO-TP: REQUEST - 0x6b6 0x22f180
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18000000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f181
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18100000000
ISO-TP: REQUEST - 0x6b6 0x22f182
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18200000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f183
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18300000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f184
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18400000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f185
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18500000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f186
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18600000000
ISO-TP: REQUEST - 0x6b6 0x22f187
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18700000000
ISO-TP: REQUEST - 0x6b6 0x22f188
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18800000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f189
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18900000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f18a
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18a00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f18b
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18b00000000
CAN-RX: 0x696 - 0x0662f18b180521
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x62f18b180521
ISO-TP: REQUEST - 0x6b6 0x22f18c
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18c00000000
CAN-RX: 0x696 - 0x100c62f18c323132
ISO-TP: RX - first frame - 0x696 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b6
CAN-TX: 0x6b6 - 0x3000000000000000
CAN-RX: 0x696 - 0x21303533323736
ISO-TP: RX - consecutive frame - 0x696 idx=1 done=True
ISO-TP: RESPONSE - 0x696 0x62f18c323132303533323736
ISO-TP: REQUEST - 0x6b6 0x22f18d
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18d00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f18e
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18e00000000
ISO-TP: REQUEST - 0x6b6 0x22f190
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19000000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f191
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19100000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f192
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19200000000
ISO-TP: REQUEST - 0x6b6 0x22f193
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19300000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f194
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19400000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f195
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19500000000
ISO-TP: REQUEST - 0x6b6 0x22f196
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19600000000
ISO-TP: REQUEST - 0x6b6 0x22f197
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19700000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f198
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19800000000
ISO-TP: REQUEST - 0x6b6 0x22f199
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19900000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19a
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19a00000000
ISO-TP: REQUEST - 0x6b6 0x22f19b
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19b00000000
ISO-TP: REQUEST - 0x6b6 0x22f19c
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19c00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19d
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19d00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19e
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19e00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19f
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19f00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
0x6b6, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:02<00:00,  2.84s/it]


*** Results for address 0x6B6 ***


0xF18B ECU_MANUFACTURING_DATE: b'\x18\x05!'
0xF18C ECU_SERIAL_NUMBER: b'212053276'
```

## DIRECTN (6B5)
```
python panda/examples/query_fw_versions.py --addr 6b5 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6b5, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6b5 0x3e00
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x023e000000000000
CAN-RX: 0x695 - 0x027e00
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7e00
ISO-TP: REQUEST - 0x6b5 0x1001
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0210010000000000
CAN-RX: 0x695 - 0x06500100c80014
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x500100c80014
ISO-TP: REQUEST - 0x6b5 0x1003
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0210030000000000
CAN-RX: 0x695 - 0x06500300c80014
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x500300c80014
ISO-TP: REQUEST - 0x6b5 0x22f180
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18000000000
CAN-RX: 0x695 - 0x101062f180010906
ISO-TP: RX - first frame - 0x695 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b5
CAN-TX: 0x6b5 - 0x3000000000000000
CAN-RX: 0x695 - 0x210f0f0f0f0f0f08
ISO-TP: RX - consecutive frame - 0x695 idx=1 done=False
CAN-RX: 0x695 - 0x22000201
ISO-TP: RX - consecutive frame - 0x695 idx=2 done=True
ISO-TP: RESPONSE - 0x695 0x62f1800109060f0f0f0f0f0f08000201
ISO-TP: REQUEST - 0x6b5 0x22f181
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18100000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f182
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18200000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f183
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18300000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f184
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18400000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f185
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18500000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f186
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18600000000
CAN-RX: 0x695 - 0x0462f18603
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x62f18603
ISO-TP: REQUEST - 0x6b5 0x22f187
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18700000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f188
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18800000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f189
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18900000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f18a
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18a00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f18b
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18b00000000
CAN-RX: 0x695 - 0x0662f18b070615
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x62f18b070615
ISO-TP: REQUEST - 0x6b5 0x22f18c
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18c00000000
CAN-RX: 0x695 - 0x101062f18c363037
ISO-TP: RX - first frame - 0x695 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b5
CAN-TX: 0x6b5 - 0x3000000000000000
CAN-RX: 0x695 - 0x2137474330383137
ISO-TP: RX - consecutive frame - 0x695 idx=1 done=False
CAN-RX: 0x695 - 0x22333039
ISO-TP: RX - consecutive frame - 0x695 idx=2 done=True
ISO-TP: RESPONSE - 0x695 0x62f18c36303737474330383137333039
ISO-TP: REQUEST - 0x6b5 0x22f18d
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18d00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f18e
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18e00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f190
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19000000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f191
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19100000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f192
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19200000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f193
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19300000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f194
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19400000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f195
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19500000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f196
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19600000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f197
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19700000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f198
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19800000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f199
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19900000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19a
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19a00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19b
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19b00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19c
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19c00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19d
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19d00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19e
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19e00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19f
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19f00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
0x6b5, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.44s/it]


*** Results for address 0x6B5 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'\x01\t\x06\x0f\x0f\x0f\x0f\x0f\x0f\x08\x00\x02\x01'
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x07\x06\x15'
0xF18C ECU_SERIAL_NUMBER: b'6077GC0817309'
```

## CMM_E/HCU2 (6A6)
```
python panda/examples/query_fw_versions.py --addr 6a6 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6a6, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6a6 0x3e00
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x023e000000000000
CAN-RX: 0x686 - 0x027e00
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7e00
ISO-TP: REQUEST - 0x6a6 0x1001
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0210010000000000
CAN-RX: 0x686 - 0x06500100c80014
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x500100c80014
ISO-TP: REQUEST - 0x6a6 0x1003
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0210030000000000
CAN-RX: 0x686 - 0x06500300c80014
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x500300c80014
ISO-TP: REQUEST - 0x6a6 0x22f180
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18000000000
CAN-RX: 0x686 - 0x100d62f180000000
ISO-TP: RX - first frame - 0x686 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a6
CAN-TX: 0x6a6 - 0x3000000000000000
CAN-RX: 0x686 - 0x2100000000000000
ISO-TP: RX - consecutive frame - 0x686 idx=1 done=True
ISO-TP: RESPONSE - 0x686 0x62f18000000000000000000000
ISO-TP: REQUEST - 0x6a6 0x22f181
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18100000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f182
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18200000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f183
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18300000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f184
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18400000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f185
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18500000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f186
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18600000000
CAN-RX: 0x686 - 0x0462f18603
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x62f18603
ISO-TP: REQUEST - 0x6a6 0x22f187
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18700000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f188
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18800000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f189
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18900000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f18a
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18a00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f18b
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18b00000000
CAN-RX: 0x686 - 0x0662f18b060321
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x62f18b060321
ISO-TP: REQUEST - 0x6a6 0x22f18c
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18c00000000
CAN-RX: 0x686 - 0x100f62f18c323130
ISO-TP: RX - first frame - 0x686 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a6
CAN-TX: 0x6a6 - 0x3000000000000000
CAN-RX: 0x686 - 0x2133303630363231
CAN-RX: 0x686 - 0x223030
ISO-TP: RX - consecutive frame - 0x686 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x686 idx=2 done=True
ISO-TP: RESPONSE - 0x686 0x62f18c323130333036303632313030
ISO-TP: REQUEST - 0x6a6 0x22f18d
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18d00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f18e
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18e00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f190
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19000000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f191
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19100000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f192
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19200000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f193
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19300000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f194
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19400000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f195
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19500000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f196
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19600000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f197
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19700000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f198
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19800000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f199
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19900000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19a
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19a00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19b
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19b00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19c
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19c00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19d
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19d00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19e
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19e00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19f
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19f00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
0x6a6, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.34s/it]


*** Results for address 0x6A6 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x06\x03!'
0xF18C ECU_SERIAL_NUMBER: b'210306062100'
```

## MSB (6B4)
```
python panda/examples/query_fw_versions.py --addr 6b4 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6b4, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6b4 0x3e00
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x023e000000000000
CAN-RX: 0x694 - 0x027e00
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7e00
ISO-TP: REQUEST - 0x6b4 0x1001
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0210010000000000
CAN-RX: 0x694 - 0x06500100c80014
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x500100c80014
ISO-TP: REQUEST - 0x6b4 0x1003
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0210030000000000
CAN-RX: 0x694 - 0x06500300c80014
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x500300c80014
ISO-TP: REQUEST - 0x6b4 0x22f180
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18000000000
CAN-RX: 0x694 - 0x101062f180533930
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x2143303539323031
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
CAN-RX: 0x694 - 0x22303236
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f18053393043303539323031303236
ISO-TP: REQUEST - 0x6b4 0x22f181
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18100000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f182
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18200000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f183
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18300000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f184
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18400000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f185
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18500000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f186
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18600000000
CAN-RX: 0x694 - 0x0462f18603
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x62f18603
ISO-TP: REQUEST - 0x6b4 0x22f187
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18700000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f188
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18800000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f189
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18900000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f18a
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18a00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f18b
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18b00000000
CAN-RX: 0x694 - 0x0662f18b110121
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x62f18b110121
ISO-TP: REQUEST - 0x6b4 0x22f18c
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18c00000000
CAN-RX: 0x694 - 0x100f62f18c353231
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x2130323139303038
CAN-RX: 0x694 - 0x223630
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f18c353231303231393030383630
ISO-TP: REQUEST - 0x6b4 0x22f18d
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18d00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f18e
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18e00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f190
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19000000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f191
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19100000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f192
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19200000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f193
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19300000000
CAN-RX: 0x694 - 0x101462f193383130
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x213232312d303030
CAN-RX: 0x694 - 0x22383056312e3120
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f1933831303232312d303030383056312e3120
ISO-TP: REQUEST - 0x6b4 0x22f194
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19400000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f195
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19500000000
CAN-RX: 0x694 - 0x101462f195413042
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x214d55433035394b
CAN-RX: 0x694 - 0x2233364356323000
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f1954130424d55433035394b33364356323000
ISO-TP: REQUEST - 0x6b4 0x22f196
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19600000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f197
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19700000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f198
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19800000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f199
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19900000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19a
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19a00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19b
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19b00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19c
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19c00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19d
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19d00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19e
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19e00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19f
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19f00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
0x6b4, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.58s/it]


*** Results for address 0x6B4 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'S90C059201026'
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x11\x01!'
0xF18C ECU_SERIAL_NUMBER: b'521021900860'
0xF193 SYSTEM_SUPPLIER_ECU_HARDWARE_VERSION_NUMBER: b'810221-00080V1.1 '
0xF195 SYSTEM_SUPPLIER_ECU_SOFTWARE_VERSION_NUMBER: b'A0BMUC059K36CV20\x00'
```

## VCU (6A2)
```
python panda/examples/query_fw_versions.py --addr 6a2 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6a2, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6a2 0x3e00
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x023e000000000000
CAN-RX: 0x682 - 0x027e00
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7e00
ISO-TP: REQUEST - 0x6a2 0x1001
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0210010000000000
CAN-RX: 0x682 - 0x06500100c80014
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x500100c80014
ISO-TP: REQUEST - 0x6a2 0x1003
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0210030000000000
CAN-RX: 0x682 - 0x06500300c80014
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x500300c80014
ISO-TP: REQUEST - 0x6a2 0x22f180
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18000000000
CAN-RX: 0x682 - 0x102762f180564538
ISO-TP: RX - first frame - 0x682 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a2
CAN-TX: 0x6a2 - 0x3000000000000000
CAN-RX: 0x682 - 0x21305f4c5f32375f
ISO-TP: RX - consecutive frame - 0x682 idx=1 done=False
CAN-RX: 0x682 - 0x2230392d344d2020
ISO-TP: RX - consecutive frame - 0x682 idx=2 done=False
CAN-RX: 0x682 - 0x2320202056453830
ISO-TP: RX - consecutive frame - 0x682 idx=3 done=False
CAN-RX: 0x682 - 0x242d534552202020
ISO-TP: RX - consecutive frame - 0x682 idx=4 done=False
CAN-RX: 0x682 - 0x252020202020
ISO-TP: RX - consecutive frame - 0x682 idx=5 done=True
ISO-TP: RESPONSE - 0x682 0x62f180564538305f4c5f32375f30392d344d2020202020564538302d5345522020202020202020
ISO-TP: REQUEST - 0x6a2 0x22f181
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18100000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f182
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18200000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f183
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18300000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f184
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18400000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f185
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18500000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f186
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18600000000
CAN-RX: 0x682 - 0x0462f18603
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x62f18603
ISO-TP: REQUEST - 0x6a2 0x22f187
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18700000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f188
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18800000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f189
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18900000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f18a
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18a00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f18b
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18b00000000
CAN-RX: 0x682 - 0x0662f18b170521
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x62f18b170521
ISO-TP: REQUEST - 0x6a2 0x22f18c
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18c00000000
CAN-RX: 0x682 - 0x100d62f18c393231
ISO-TP: RX - first frame - 0x682 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a2
CAN-TX: 0x6a2 - 0x3000000000000000
CAN-RX: 0x682 - 0x2130313236393039
ISO-TP: RX - consecutive frame - 0x682 idx=1 done=True
ISO-TP: RESPONSE - 0x682 0x62f18c39323130313236393039
ISO-TP: REQUEST - 0x6a2 0x22f18d
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18d00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f18e
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18e00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f190
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19000000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f191
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19100000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f192
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19200000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f193
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19300000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f194
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19400000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f195
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19500000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f196
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19600000000
CAN-RX: 0x682 - 0x101362f196484f4d
ISO-TP: RX - first frame - 0x682 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a2
CAN-TX: 0x6a2 - 0x3000000000000000
CAN-RX: 0x682 - 0x212d303030343532
ISO-TP: RX - consecutive frame - 0x682 idx=1 done=False
CAN-RX: 0x682 - 0x22000000000000
ISO-TP: RX - consecutive frame - 0x682 idx=2 done=True
ISO-TP: RESPONSE - 0x682 0x62f196484f4d2d303030343532000000000000
ISO-TP: REQUEST - 0x6a2 0x22f197
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19700000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f198
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19800000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f199
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19900000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19a
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19a00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19b
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19b00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19c
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19c00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19d
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19d00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19e
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19e00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19f
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19f00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
0x6a2, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.32s/it]


*** Results for address 0x6A2 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'VE80_L_27_09-4M     VE80-SER        '
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x17\x05!'
0xF18C ECU_SERIAL_NUMBER: b'9210126909'
0xF196 EXHAUST_REGULATION_OR_TYPE_APPROVAL_NUMBER: b'HOM-000452\x00\x00\x00\x00\x00\x00'
```

## ABRASR (6AD)
```
python panda/examples/query_fw_versions.py --addr 6ad --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6ad, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6ad 0x3e00
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x023e000000000000
CAN-RX: 0x68d - 0x027e00
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7e00
ISO-TP: REQUEST - 0x6ad 0x1001
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0210010000000000
CAN-RX: 0x68d - 0x06500100c80014
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x500100c80014
ISO-TP: REQUEST - 0x6ad 0x1003
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0210030000000000
CAN-RX: 0x68d - 0x037f1078
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f1078
UDS-RX: response pending
CAN-RX: 0x68d - 0x06500300c80014
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x500300c80014
ISO-TP: REQUEST - 0x6ad 0x22f180
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18000000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f181
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18100000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f182
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18200000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f183
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18300000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f184
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18400000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f185
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18500000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f186
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18600000000
CAN-RX: 0x68d - 0x0462f18603
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x62f18603
ISO-TP: REQUEST - 0x6ad 0x22f187
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18700000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f188
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18800000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f189
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18900000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f18a
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18a00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f18b
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18b00000000
CAN-RX: 0x68d - 0x0662f18b270521
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x62f18b270521
ISO-TP: REQUEST - 0x6ad 0x22f18c
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18c00000000
CAN-RX: 0x68d - 0x101562f18c303835
ISO-TP: RX - first frame - 0x68d idx=0 done=False
ISO-TP: TX - flow control continue - 0x6ad
CAN-TX: 0x6ad - 0x3000000000000000
CAN-RX: 0x68d - 0x2130393537303038
CAN-RX: 0x68d - 0x2235373231303532
ISO-TP: RX - consecutive frame - 0x68d idx=1 done=False
ISO-TP: RX - consecutive frame - 0x68d idx=2 done=False
CAN-RX: 0x68d - 0x2337
ISO-TP: RX - consecutive frame - 0x68d idx=3 done=True
ISO-TP: RESPONSE - 0x68d 0x62f18c303835303935373030383537323130353237
ISO-TP: REQUEST - 0x6ad 0x22f18d
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18d00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f18e
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18e00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f190
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19000000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f191
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19100000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f192
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19200000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f193
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19300000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f194
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19400000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f195
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19500000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f196
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19600000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f197
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19700000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f198
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19800000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f199
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19900000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19a
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19a00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19b
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19b00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19c
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19c00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19d
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19d00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19e
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19e00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19f
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19f00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
0x6ad, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.46s/it]


*** Results for address 0x6AD ***


0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b"'\x05!"
0xF18C ECU_SERIAL_NUMBER: b'085095700857210527'
```
