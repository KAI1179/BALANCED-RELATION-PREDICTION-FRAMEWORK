# BALANCED-RELATION-PREDICTION-FRAMEWORK

Reference this [repo](https://github.com/KaihuaTang/Scene-Graph-Benchmark.pytorch) for environmental configuration and dataset preparation

'''
 # train motifs + DCL(RW):
python tools\relation_train_net.py CUDA_VISIBLE_DEVICES=0 --config-file "configs/e2e_relation_X_101_32_8_FPN_1x.yaml" MODEL.ROI_RELATION_HEAD.USE_GT_BOX True MODEL.ROI_RELATION_HEAD.USE_GT_OBJECT_LABEL True MODEL.ROI_RELATION_HEAD.PREDICTOR MotifPredictor SOLVER.IMS_PER_BATCH 12 TEST.IMS_PER_BATCH 1 DTYPE "float16" SOLVER.MAX_ITER 30000 SOLVER.VAL_PERIOD 2500 SOLVER.CHECKPOINT_PERIOD 2500 GLOVE_DIR /data1/xukai_1/code/sgg/Scene-Graph-Benchmark.pytorch-master/glove MODEL.PRETRAINED_DETECTOR_CKPT /data1/xukai_1/checkpoints/pretrained_faster_rcnn/model_final.pth OUTPUT_DIR ./output/reweight-dcl/motifs-dcl-rw-precls
'''

More detailed instructions will be released later
