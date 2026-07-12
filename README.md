# Workflow-CI

Repositori ini dibuat khusus untuk memenuhi **Kriteria 3: Membuat Workflow CI** pada kelas Membangun Sistem Machine Learning (Dicoding).

## Struktur Repositori

```
Workflow-CI
├── .github/workflows/
│   └── mlflow_ci.yml
├── .workflow/
│   └── mlflow_ci.yml
└── MLProject/
    ├── modelling.py
    ├── conda.yaml
    ├── MLproject
    ├── requirements.txt
    ├── namadataset_preprocessing/
    └── DOCKERHUB.md
```

## Deskripsi

- **MLProject/**: Folder utama project MLflow.
  - `modelling.py`: Melakukan baseline training dan mencatat parameter, metrik, serta model artifact secara otomatis dengan `mlflow.autolog()`.
  - `conda.yaml` & `requirements.txt`: Spesifikasi dependencies untuk reproduction.
  - `MLproject`: File konfigurasi entry points MLflow.
  - `namadataset_preprocessing/`: Data hasil preprocessing yang siap digunakan untuk training.
  - `DOCKERHUB.md`: Berisi tautan repository Docker Hub image yang telah berhasil dibangun.
- **Workflow CI**: Dikonfigurasi menggunakan GitHub Actions (`mlflow_ci.yml`) untuk otomatis melakukan setup environment, dependencies installation, training execution, build Docker container, serta mem-backup metrics & model artifacts kembali ke Git repository menggunakan Git LFS.
