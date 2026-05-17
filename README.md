# SolSim3D
SolSim3D - Solar Cooking &amp; Thermal Co-Generation Simulator
<img width="1894" height="904" alt="image" src="https://github.com/user-attachments/assets/73f0b985-32c5-4442-8eb1-7ca980d73d8f" />


[Tiếng Việt bên dưới](#tiếng-việt)

SolSim3D is an interactive, technical 3D simulation platform designed for engineers, researchers, and green energy enthusiasts. It allows users to model, analyze, and stress-test a Closed-Loop Optical Feed Horn Solar Concentrator system integrated with a thermal co-generation water tank before moving into physical construction.

By utilizing high-fidelity numerical formulations for thermodynamics, optical reflection losses, and convective cooling, SolSim3D predicts terminal focal temperatures and multi-segment pipeline thermal distribution in real-time.

---

## English Introduction

### Key Features
* **Dynamic 3D CAD Parametrization:** Adjust parabolic dish scale ($D$, $H$, core hole diameter) and internal pipeline diameters in real-time.
* **Multi-Segment Hydraulic Bending:** Add custom pipeline configurations with varying orientations to simulate indoor deployment constraints.
* **Real-time Thermal Solver:** Simulates solar irradiance absorption ($850 W/m^2$), dynamic convection losses ($h=15 W/m^2\cdot K$), and reflection efficiency drops (95% per mirror angle).
* **Co-Generation Water Tank Module:** Includes an unconstrained cooling tank boundary simulation ($min = 0.1m$) to calculate waste heat absorption, water volume capacity, and continuous boiling times.
* **Raycasted Interactive Tooltip:** Hovering over individual components isolates localized surface temperatures and environmental factors.

### Technical Formulations Included
1. **Focal Length Calculation:** $$\text{f} = \frac{D^2}{16H}$$
2. **Effective Aperture Area:** $$A_{\text{eff}} = \frac{\pi}{4} (D^2 - d_{\text{hole}}^2)$$
3. **Thermal Equilibrium State:** $$T_{\text{cook}} = T_{\text{amb}} + \frac{P_{\text{out}}}{1.2 \cdot h \cdot A_{\text{pot}}}$$

### Technology Stack
* **Core Engine:** HTML5, Vanilla JavaScript (ES6+)
* **Graphics Rendering:** Three.js (r128) via WebGL
* **Camera & Controls:** OrbitControls.js
* **Styling:** CSS3 Matrix3D/Perspective Glassmorphism UI

---

## Tiếng Việt

SolSim3D là một nền tảng mô phỏng kỹ thuật 3D tương tác trực quan dành cho các kỹ sư, nhà nghiên cứu và những ai đam mê năng lượng xanh. Hệ thống cho phép mô hình hóa, phân tích cấu trúc toán học và kiểm tra ứng suất nhiệt của hệ thống Bếp Năng Lượng Mặt Trời trục ống dẫn quang (Closed-Loop Feed Horn) tích hợp bể nước đồng phát nhiệt lượng trước khi tiến hành thi công lắp đặt thực tế.

Thông qua việc áp dụng các công thức nhiệt động lực học chính xác về tổn hao bức xạ, đối lưu môi trường và hiệu suất phản xạ của gương, SolSim3D dự đoán chính xác nhiệt độ hội tụ tại đáy nồi và phân bổ nhiệt trên từng mét ống dẫn theo thời gian thực.

### Các Tính Năng Cốt Lõi
* **Tham số hóa Hình học 3D Linh hoạt:** Tự do thay đổi kích thước đĩa parabol (Đường kính $D$, chiều sâu $H$, lỗ lõi) và thiết diện đường ống dẫn quang.
* **Tùy biến Tuyến Ống Khúc Khuỷu:** Cho phép thêm/bớt các đoạn ống với các góc xoay hướng khác nhau nhằm tối ưu hóa đường đi trong không gian nhà xưởng thực tế.
* **Mô phỏng Nhiệt Động Học Thời Gian Thực:** Tính toán mức hấp thụ năng lượng mặt trời ($850 W/m^2$), tổn hao đối lưu tự nhiên ($h=15 W/m^2\cdot K$) và độ sụt giảm công suất qua từng khớp gương phản xạ (95%).
* **Tích hợp Bể Nước Giải Nhiệt Đồng Phát:** Mô phỏng hộp chứa nước bao quanh tuyến ống với kích thước tự do tùy chỉnh tuyệt đối (từ $0.1m$ trở lên) để tính toán thể tích chứa, công suất thu nhiệt dư và thời gian nước đạt độ sôi.
* **Khảo sát Điểm Bằng Raycaster:** Di chuột trực tiếp vào từng đoạn ống, gương chéo hoặc lòng đĩa để hiển thị thông số nhiệt độ bề mặt và trạng thái môi trường cô lập.

### Công Nghệ Sử Dụng
* **Ngôn ngữ cốt lõi:** HTML5, Vanilla JavaScript (ES6+)
* **Đồ họa 3D:** Thư viện Three.js (r128) chạy trên nền tảng WebGL hiệu năng cao.
* **Điều hướng không gian:** OrbitControls.js (Hỗ trợ xoay, phóng to thu nhỏ mượt mà).
* **Giao diện người dùng:** CSS3 Lập thể kết hợp bộ lọc kính mờ (Glassmorphism UI) góc nghiêng `rotateY(-20deg)` mang phong cách buồng điều khiển kỹ thuật số.

---

## Getting Started / Hướng dẫn Chạy Dự Án

1. Clone this repository to your local machine / Sao chép kho lưu trữ này về máy tính của bạn:
   ```bash
   git clone [https://github.com/doanthanhhungwork1-creator/SolSim3D.git](https://github.com/doanthanhhungwork1-creator/SolSim3D.git)
2. Open the index.html file directly in any modern web browser (Chrome, Edge, Firefox, Safari). No heavy node servers or build tools required.
(Mở trực tiếp file index.html bằng bất kỳ trình duyệt web hiện đại nào. Không cần cài đặt máy chủ Node hay công cụ đóng gói phức tạp).

3. Adjust the configurations on the right-hand panel to validate your physical hardware designs.
(Tùy chỉnh các tham số ở bảng điều khiển bên phải để kiểm nghiệm thiết kế phần cứng thực tế của bạn).
