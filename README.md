# SoccerNet - Action Spotting

## Notice

This repository provides documentation and an overview of the SoccerNet Action Spotting project. Due to GitHub's storage limitations, the full set of files—including models, source code, datasets, training outputs, and visualizations—are not hosted here.

To access the complete project, please visit the following link:

**Google Drive Access:**  
[Download Full Project Files](https://drive.google.com/file/d/1S-tYcSvdcfSM79XOodPtoaZrg0iUYVMZ/view?usp=sharing)

---

## Project Overview

This project builds on the SoccerNet Development Kit for the Action Spotting and Ball Action Spotting challenges. It includes data preparation, model integration, event detection logic, and real-time video analysis features.

The SoccerNet-v2 dataset introduces new benchmarks and tasks in sports video understanding, including:
- Action Spotting (17 class labels)
- Ball Action Spotting (12 dense action classes)
- Camera Boundary Detection
- Replay Grounding

The project also integrates detection models (e.g., YOLOv11x-seg and DeepLabv3) and provides annotated outputs, AR overlays, and event logs.

---

## Dataset Access

You can learn more about the official dataset and evaluation challenge here:

- [SoccerNet Website](https://www.soccer-net.org/)
- [2024 Challenge – Evaluation Server](https://eval.ai/web/challenges/challenge-page/2200/overview)
- [Baseline GitHub Repository](https://github.com/recokick/ball-action-spotting)

---

## Full Package Contents (Available in Google Drive)

The Google Drive package includes:
- Complete project source code
- YOLOv11x-seg + DeepLabv3 integration
- Custom event detection logic for real-time inference
- Live stream analysis setup (WebSocket)
- Output video annotation with AR overlays
- Clip-based SoccerNet spotting module
- Installation scripts and configuration files
- Sample 360° and broadcast match videos

---

## Getting Started

To use the full project from Google Drive:

1. Download and unzip the project folder.
2. Review `setup_instructions.md` for detailed setup.
3. Create a virtual environment and install dependencies from `requirements.txt`.
4. Run the pipeline using:

```bash
python run_pipeline.py --config config.yaml
```

This will start the unified video processing pipeline, detecting players, analyzing zones, and identifying football events in real-time.

---

## Technical Stack

- Python 3.9+
- PyTorch
- OpenCV
- DeepLabv3
- YOLOv11x-seg
- WebSocket (for real-time communication)
- panolens.js (optional for 360° VR view)

---

## License and Usage

Please refer to the license terms of the SoccerNet dataset and any third-party components used in this project. This repository is shared for educational and non-commercial research purposes.

---

## Citation

If you use this project or the SoccerNet dataset in your research or development work, please cite the following:

```bibtex
@InProceedings{Deliège2020SoccerNetv2,
      title={SoccerNet-v2 : A Dataset and Benchmarks for Holistic Understanding of Broadcast Soccer Videos}, 
      author={Adrien Deliège and others},
      year={2021},
      booktitle = {The IEEE Conference on Computer Vision and Pattern Recognition (CVPR) Workshops}
}
```

For additional details, see the full paper:  
[SoccerNet-v2 Paper (CVPR 2021)](https://openaccess.thecvf.com/content/CVPR2021W/CVSports/papers/Deliege_SoccerNet-v2_A_Dataset_and_Benchmarks_for_Holistic_Understanding_of_Broadcast_CVPRW_2021_paper.pdf)
