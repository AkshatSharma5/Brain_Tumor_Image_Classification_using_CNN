Brain Tumor Image Classification and Explanable AI (using ResNet50)

- Dataset: 4-class T1-CE Brain MRI (Glioma/Meningioma/Pituitary/No Tumor)
- Image size: {yaml.safe_load(open('config.yaml'))['data']['img_size']}
- Training: Transfer learning + fine-tuning (see training_log.csv)
- Checkpoint: best_model.h5 (saved to Drive)
- Metrics: See classification_report.txt, confusion_matrix.png
- Explainability: See Grad-CAM overlays in reports/figures

Run order (Colab):
1) Preprocess: python -m src.data.preprocess
2) Train: python -m src.train
3) Evaluate: python -m src.evaluate
4) Grad-CAM demo: python -m src.predict data/processed/test//
