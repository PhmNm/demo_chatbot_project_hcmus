ChatterBot Django Example
=========================

This is an example Django app that shows how to create a simple chat bot web
app using [Django](https://www.djangoproject.com) and [ChatterBot](https://github.com/gunthercox/ChatterBot).
See our [report](https://github.com/PhmNm/demo_chatbot_project_hcmus/blob/master/report_final.pdf) about the chatbot
Documentation
-------------
### Before installation
+ Download [Chatterbot1.0.8](https://github.com/gunthercox/ChatterBot/releases/tag/1.0.8)
+ Đối với hệ thống sử dụng python >= 3.8:
    + Mở file setup.py trong thư mục, search "python_requires" và chỉnh mục 3.8 thành 3.10 hoặc xoá mục "<=3.8"
+ Đối với tất cả phiên bản python >=3.4. Ta tuỳ chỉnh một số dependency:
    + Mở file dev-requirements.txt:
        +  Xoá mục yêu cầu phiên bản của spacy
        +  Sửa dòng "git+git..." thành chatterbot_corpus
    + Nếu sử dụng chatterbot với ngôn ngữ mặc định (tiếng Anh), mở file "/ chatterbot/tagging.py" đến dòng số 13 chỉnh thành "self.nlp = spacy.load("en_core_web_sm")"

-----
### Installation

```terminal
cd ChatterBot-1.0.8
pip install .
pip install -r dev-requirements.txt
pip install django>=2.1,<2.2
```
-----
### Start django app
Migrate database
```django
python3 manage.py migrate
```
Runserver
```django
python3 manage.py runserver
```
Open localhost at port [:8000](http://127.0.0.1:8000/) (default django port)

Further documentation on getting set up with Django and ChatterBot can be
found in the [`ChatterBot documentation`](http://chatterbot.readthedocs.io/en/stable/django/index.html).
