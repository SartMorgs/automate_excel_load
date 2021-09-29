FROM python:3.9.1

ARG model_bucket
ARG model_folder
ARG model_filename
ARG query_filename
ARG region_name
ARG start_row
ARG start_column
ARG last_column
ARG data_name_sheet

ENV MODEL_BUCKET=$model_bucket
ENV MODEL_FOLDER=$model_folder
ENV MODEL_FILENAME=$model_filename
ENV QUERY_FILENAME=$query_filename
ENV REGION_NAME=$region_name
ENV START_ROW=$start_row
ENV START_COLUMN=$start_column
ENV LAST_COLUMN=$last_column
ENV DATA_NAME_SHEET=$data_name_sheet

RUN apt-get update
ADD code/. /automate-excel-load/code
ADD tmp/. /automate-excel-load/tmp
ADD requirements.txt /automate-excel-load
WORKDIR /automate-excel-load
RUN pip install -r requirements.txt