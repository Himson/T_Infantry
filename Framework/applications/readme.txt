���������Ĳ�����
Ħ���ֵ�ת�٣�drivers_uartrc_low.h 36��FRICTION_WHEEL_MAX_DUTY  һ����1200��1600�ķ�Χ��ȫ�����õ�1350 
������̨�����λ�ã�tasks_motor.c �е�yaw_zero��pitch_zero����ͬ�ĳ���һ����
������̨��PID��tasks_motor.c �У�λ�û�PID��pitchPositionPID��yawPositionPID���ٶȻ�PID��pitchSpeedPID��yawSpeedPID
�����ٶ�PID��tasks_motor.c ��CM1SpeedPID��CMRotatePID������Ӧ��tasks_timed.h�е�CHASSIS_MOTOR_ROTATE_PID_DEFAULT��CHASSIS_MOTOR_SPEED_PID_DEFAULT
�������ţ���ͬ�ĳ�������һ������tasks_motor.h�е� #define INFANTRY_1
��̨λ�õ�Ŀ��ֵ��һ��ֻ��ң�����޸ģ������������ط��Ŀ������޸����ֵ��tasks_motor.c ��78��yawAngleTarget��82��pitchAngleTarget
                                                                    ���ǵò��Ǹ����ĳ�ʼֵ�����޸����������ͬʱע����������ʲô�ط��޸������������һ�㷶Χ��-10��10��
�����ٶȵ�Ŀ��ֵ��ע���ͬ�ϣ���drivers_uartrc.c����65�нṹ��ChassisSpeedRef��ǰ��ChassisSpeedRef.forward_back_ref������ChassisSpeedRef.left_right_ref��
                               ��תChassisSpeedRef.rotate_ref��һ�㷶Χ��������
ң�ص����ã�tasks_remotecontrol.c 213�е�RemoteControlProcess(Remote *rc) ��ͨ��ҡ��rc->ch0��rc->ch3����ֵΪ0��2047����ֵΪ1024��
                                       ҡ�˿���ǰ�����ҵ�������STICK_TO_CHASSIS_SPEED_REF_FACT��������̨�˶���������STICK_TO_PITCH_ANGLE_INC_FACT��STICK_TO_YAW_ANGLE_INC_FACT
�����̵����� 243�е� MouseKeyControlProcess(Mouse *mouse, Key *key) ��λ��key->v����λ�����£�
//Bit0-----W
//Bit1-----S
//Bit2-----A
//Bit3-----D
//Bit4-----Shift
//Bit5-----Ctrl
//Bit6-----Q
//Bit7-----E
//Bit8-----R
//Bit9-----F
//Bit10-----G
//Bit11-----Z
//Bit12-----X
//Bit13-----C
//Bit14-----V
//Bit15-----B
����������̨���Ƶ�������MOUSE_TO_PITCH_ANGLE_INC_FACT��MOUSE_TO_YAW_ANGLE_INC_FACT
          �����ƶ����ٶ�LOW_FORWARD_BACK_SPEED��MIDDLE_FORWARD_BACK_SPEED��NORMAL_FORWARD_BACK_SPEED
		                LOW_LEFT_RIGHT_SPEED��MIDDLE_LEFT_RIGHT_SPEED��NORMAL_LEFT_RIGHT_SPEED
ִ��һ�η��� ����һ��tasks_platemotor.c�е�ShootOneBullet()

Drivers/CMSIS,Application/MDK-ARM,Drivers/STM32F4xx_HAL_Driver:
��Щ��ST�ٷ��ṩ�Ĺ̼��⣬���԰�װоƬ�ײ������Ŀ⺯������ͬϵ�е�оƬ�⺯����һ����Cube����ʱ���Զ����ɡ�
��֪����Ӧ���ܵĿ⺯����ʲôʱ���԰ٶȣ����Բ�˵���飬Ҳ��������Ӧ����Ŀ⺯���ļ�������

Middlewares/FreeRTOS:
FreeRTOS����ϵͳ�ĳ����ļ���Cube����ʱ�Զ�����
���е�main����

Middlewares/USB_Device_Library:
USB�����ÿ⺯���ļ������ذ�����һ��miniUSB�ӿڣ����������ַ�ʽͨ�ţ�������Ŀǰû�п���

Application/User��
��������ã�Cube����

Framework/RTOS:
rtos_init.c:ϵͳ�ĳ�ʼ���������԰����ϵ�����ģ����г�ʼ����Ҫ����оƬ�ϵ������ʼ�����Ǹ������֮ǰ����Cube���ɵġ�
���Ҫ�Լ�д���Ժ����ʲô��Ӳ����Ҫ��ʼ���Ļ���������ӡ�
rtos_semaphore.c:ϵͳ�����ź����ĳ�ʼ��������ź������������ʽ���
rtos_task.c:ϵͳ���̳�ʼ�������������������ʽ���

Framework/Peripheral:
peripheral_define.h: ��ʱ�������ڣ�CAN������������߿ɶ���
peripheral_gpio.c���ⲿ�ж϶�ȡMPU6050����
peripheral_laser.h��������׼���Ŀ��غ���

Framework/Utilities:
utilities_debug.c���ض���C��׼�⺯��printf������DEBUG_UART,����ֱ����printf�����Ϣ�����ڣ��������
utilities_iopool.c��IOPOOL�Ķ��壬һ�������ȫ�ֱ��������̼߳䰲ȫͨ�ŵķ�ʽ������ʹ�ÿ�C�ļ�ע��
utilities_minmax.h���������Сֵ�ĺ����ͽǶȹ淶���ĺ���
utilities_tim.c��ʹ��1ms��ʱ������ϵ��ms��λ��ʱ��
peripheral_tim.c��Ħ���֡����PWM���趨ʱ����ʼ������

Framework/Drives:
drivers_led.c����ƺ��̵ƵĿ��غ������Լ��������Ƶ�����
drivers_imu.c��IMU���������ݵĶ�ȡ�������Լ�IMU���ݵ�ˢ������
drivers_buzzer.c����������ִ�к�����������������
drivers_canmotor.c��CAN�ĵײ�������CAN�Ľ�����ͨ���жϵķ�ʽ�����Խ��շ����ı�����λ�á��ٶ���Ϣ���Լ����������ǵ����ݡ�
                    CAN�ķ�����������������Լ����õ��������ǣ���Ҫ����
drivers_uart.c�����д��ڵ��жϺ���������ң�������ڣ����㴮�ڣ�����ϵͳ����
drivers_uartrc.c��ң�������ڽ��պ�������Ҫ�������˵�ģʽ���ã��Լ�����Ħ���ֵ������߼�
drivers_upper.c�������ͨ�ź�����ԭ��ֻ�ش�һ��������Ļ�������
drivers_flash.c��flashд��Ͷ�ȡ�ĺ��������ڵ��籣�棬������Ŀǰû�õ�
drivers_sonar.c�������������������������ã�����û���õ�
drivers_ramp.h��б�º���
pid_regulator.c��PID������ʵ�֣��������PID���������߼����㷨Ҫ������
pwm_server_motor����ͬPWM���Ʋ����Ķ���Ƕȣ�ԭ���������Ƶ��ֿ��صģ�����û���õ�
drivers_uartjudge.c������ϵͳ���ڵ��жϺ�����������ϵͳ������֡��������Ϣ
drivers_platemotor.c�����̵���ٶ�/λ�ÿ���
drivers_cmpower.c������������ʣ������̬����

Framework/Applications���������������ߣ��Ƚ���Ҫ
tasks_motor.c�����̺���̨�Ŀ���������ҪҪ���ĵ���PID����̨PID�������
application_motorcontrol.c��ִ�е��CAN�źſ��Ƶĺ���
tasks_upper.c������ͨ������
application_quaternion��������Ԫ���ĺ�����������Ŀǰû���õ�
tasks_remotecontrol.c��ң�������Ƶ����������Ƚ���Ҫ��ң�������ˡ�ҡ�ˣ�������������ʽ������߸�
tasks_timed.c 2ms���ڵ�����״̬���л�
application_waveform.c ��λ���۲����źŲ��Σ�֮ǰû���õ�
tasks_platemotor.c ���̵���������������Ʒ��䣬����һ��ShootOneBullet()ִ��һ�η���