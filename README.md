# project1
{
  "cells": [
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "r02z1E_Sz5On",
        "outputId": "0049c1e7-8a87-4951-cd25-8e9e0922e28f"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "Mounted at /content/drive\n"
          ]
        }
      ],
      "source": [
        "from google.colab import drive\n",
        "drive.mount('/content/drive')"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "qVjCB06C0TZr"
      },
      "outputs": [],
      "source": [
        "!cp '/content/drive/MyDrive/Module3' -r '/content/'"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "bHBs25VS0Xds",
        "outputId": "45dbfcb3-5143-4fe6-aed6-46a3f4a1f522"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "/content/Module3\n"
          ]
        }
      ],
      "source": [
        "%cd '/content/Module3/'"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "iGHj-AS16yT7",
        "outputId": "640a9dec-78d4-4887-ecbe-7004d321d311"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "Collecting asttokens==2.2.1 (from -r requirements.txt (line 1))\n",
            "  Downloading asttokens-2.2.1-py2.py3-none-any.whl (26 kB)\n",
            "Requirement already satisfied: backcall==0.2.0 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 2)) (0.2.0)\n",
            "Collecting blinker==1.6.2 (from -r requirements.txt (line 3))\n",
            "  Downloading blinker-1.6.2-py3-none-any.whl (13 kB)\n",
            "Collecting branca==0.6.0 (from -r requirements.txt (line 4))\n",
            "  Downloading branca-0.6.0-py3-none-any.whl (24 kB)\n",
            "Collecting certifi==2023.5.7 (from -r requirements.txt (line 5))\n",
            "  Downloading certifi-2023.5.7-py3-none-any.whl (156 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m157.0/157.0 kB\u001b[0m \u001b[31m5.4 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting charset-normalizer==3.1.0 (from -r requirements.txt (line 6))\n",
            "  Downloading charset_normalizer-3.1.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (199 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m199.3/199.3 kB\u001b[0m \u001b[31m18.3 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting click==8.1.3 (from -r requirements.txt (line 7))\n",
            "  Downloading click-8.1.3-py3-none-any.whl (96 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m96.6/96.6 kB\u001b[0m \u001b[31m8.6 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting colorama==0.4.6 (from -r requirements.txt (line 8))\n",
            "  Downloading colorama-0.4.6-py2.py3-none-any.whl (25 kB)\n",
            "Collecting comm==0.1.3 (from -r requirements.txt (line 9))\n",
            "  Downloading comm-0.1.3-py3-none-any.whl (6.6 kB)\n",
            "Collecting debugpy==1.6.7 (from -r requirements.txt (line 10))\n",
            "  Downloading debugpy-1.6.7-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (3.0 MB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m3.0/3.0 MB\u001b[0m \u001b[31m53.3 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting decorator==5.1.1 (from -r requirements.txt (line 11))\n",
            "  Downloading decorator-5.1.1-py3-none-any.whl (9.1 kB)\n",
            "Requirement already satisfied: et-xmlfile==1.1.0 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 12)) (1.1.0)\n",
            "Collecting executing==1.2.0 (from -r requirements.txt (line 13))\n",
            "  Downloading executing-1.2.0-py2.py3-none-any.whl (24 kB)\n",
            "Collecting Flask==2.3.2 (from -r requirements.txt (line 14))\n",
            "  Downloading Flask-2.3.2-py3-none-any.whl (96 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m96.9/96.9 kB\u001b[0m \u001b[31m13.0 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: folium==0.14.0 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 15)) (0.14.0)\n",
            "Requirement already satisfied: geographiclib==2.0 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 16)) (2.0)\n",
            "Requirement already satisfied: geopy==2.3.0 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 17)) (2.3.0)\n",
            "Collecting idna==3.4 (from -r requirements.txt (line 18))\n",
            "  Downloading idna-3.4-py3-none-any.whl (61 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m61.5/61.5 kB\u001b[0m \u001b[31m8.5 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting importlib-metadata==6.7.0 (from -r requirements.txt (line 19))\n",
            "  Downloading importlib_metadata-6.7.0-py3-none-any.whl (22 kB)\n",
            "Collecting ipykernel==6.24.0 (from -r requirements.txt (line 20))\n",
            "  Downloading ipykernel-6.24.0-py3-none-any.whl (152 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m152.8/152.8 kB\u001b[0m \u001b[31m18.7 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting ipython==8.14.0 (from -r requirements.txt (line 21))\n",
            "  Downloading ipython-8.14.0-py3-none-any.whl (798 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m798.7/798.7 kB\u001b[0m \u001b[31m53.5 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: itsdangerous==2.1.2 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 22)) (2.1.2)\n",
            "Collecting jedi==0.18.2 (from -r requirements.txt (line 23))\n",
            "  Downloading jedi-0.18.2-py2.py3-none-any.whl (1.6 MB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m1.6/1.6 MB\u001b[0m \u001b[31m76.1 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting Jinja2==3.1.2 (from -r requirements.txt (line 24))\n",
            "  Downloading Jinja2-3.1.2-py3-none-any.whl (133 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m133.1/133.1 kB\u001b[0m \u001b[31m18.3 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting jupyter_client==8.3.0 (from -r requirements.txt (line 25))\n",
            "  Downloading jupyter_client-8.3.0-py3-none-any.whl (103 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m103.2/103.2 kB\u001b[0m \u001b[31m9.9 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting jupyter_core==5.3.1 (from -r requirements.txt (line 26))\n",
            "  Downloading jupyter_core-5.3.1-py3-none-any.whl (93 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m93.7/93.7 kB\u001b[0m \u001b[31m9.0 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hCollecting MarkupSafe==2.1.3 (from -r requirements.txt (line 27))\n",
            "  Downloading MarkupSafe-2.1.3-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (25 kB)\n",
            "Requirement already satisfied: matplotlib-inline==0.1.6 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 28)) (0.1.6)\n",
            "Collecting nest-asyncio==1.5.6 (from -r requirements.txt (line 29))\n",
            "  Downloading nest_asyncio-1.5.6-py3-none-any.whl (5.2 kB)\n",
            "Collecting newsapi-python==0.2.7 (from -r requirements.txt (line 30))\n",
            "  Downloading newsapi_python-0.2.7-py2.py3-none-any.whl (7.9 kB)\n",
            "Collecting numpy==1.25.0 (from -r requirements.txt (line 31))\n",
            "  Downloading numpy-1.25.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (17.6 MB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m17.6/17.6 MB\u001b[0m \u001b[31m61.8 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: openpyxl==3.1.2 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 32)) (3.1.2)\n",
            "Collecting packaging==23.1 (from -r requirements.txt (line 33))\n",
            "  Downloading packaging-23.1-py3-none-any.whl (48 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m48.9/48.9 kB\u001b[0m \u001b[31m6.1 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: pandas==2.0.3 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 34)) (2.0.3)\n",
            "Collecting parso==0.8.3 (from -r requirements.txt (line 35))\n",
            "  Downloading parso-0.8.3-py2.py3-none-any.whl (100 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m100.8/100.8 kB\u001b[0m \u001b[31m13.1 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: pickleshare==0.7.5 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 36)) (0.7.5)\n",
            "Collecting platformdirs==3.8.1 (from -r requirements.txt (line 37))\n",
            "  Downloading platformdirs-3.8.1-py3-none-any.whl (16 kB)\n",
            "Collecting prompt-toolkit==3.0.39 (from -r requirements.txt (line 38))\n",
            "  Downloading prompt_toolkit-3.0.39-py3-none-any.whl (385 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m385.2/385.2 kB\u001b[0m \u001b[31m38.2 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: psutil==5.9.5 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 39)) (5.9.5)\n",
            "Collecting pure-eval==0.2.2 (from -r requirements.txt (line 40))\n",
            "  Downloading pure_eval-0.2.2-py3-none-any.whl (11 kB)\n",
            "Collecting Pygments==2.15.1 (from -r requirements.txt (line 41))\n",
            "  Downloading Pygments-2.15.1-py3-none-any.whl (1.1 MB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m1.1/1.1 MB\u001b[0m \u001b[31m67.8 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25hRequirement already satisfied: python-dateutil==2.8.2 in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 42)) (2.8.2)\n",
            "Collecting pytz==2023.3 (from -r requirements.txt (line 43))\n",
            "  Downloading pytz-2023.3-py2.py3-none-any.whl (502 kB)\n",
            "\u001b[2K     \u001b[90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━\u001b[0m \u001b[32m502.3/502.3 kB\u001b[0m \u001b[31m45.8 MB/s\u001b[0m eta \u001b[36m0:00:00\u001b[0m\n",
            "\u001b[?25h\u001b[31mERROR: Could not find a version that satisfies the requirement pywin32==306 (from versions: none)\u001b[0m\u001b[31m\n",
            "\u001b[0m\u001b[31mERROR: No matching distribution found for pywin32==306\u001b[0m\u001b[31m\n",
            "\u001b[0m"
          ]
        }
      ],
      "source": [
        "!pip install -r requirements.txt"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "-NVwbf090Xjn",
        "outputId": "6b85e4c5-1b11-4b90-9fc7-325bd7b6b15a"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "Collecting newsapi-python\n",
            "  Using cached newsapi_python-0.2.7-py2.py3-none-any.whl (7.9 kB)\n",
            "Requirement already satisfied: requests<3.0.0 in /usr/local/lib/python3.10/dist-packages (from newsapi-python) (2.31.0)\n",
            "Requirement already satisfied: charset-normalizer<4,>=2 in /usr/local/lib/python3.10/dist-packages (from requests<3.0.0->newsapi-python) (3.3.2)\n",
            "Requirement already satisfied: idna<4,>=2.5 in /usr/local/lib/python3.10/dist-packages (from requests<3.0.0->newsapi-python) (3.6)\n",
            "Requirement already satisfied: urllib3<3,>=1.21.1 in /usr/local/lib/python3.10/dist-packages (from requests<3.0.0->newsapi-python) (2.0.7)\n",
            "Requirement already satisfied: certifi>=2017.4.17 in /usr/local/lib/python3.10/dist-packages (from requests<3.0.0->newsapi-python) (2024.2.2)\n",
            "Installing collected packages: newsapi-python\n",
            "Successfully installed newsapi-python-0.2.7\n"
          ]
        }
      ],
      "source": [
        "!pip install newsapi-python"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "HKdexLTJ0TdE",
        "outputId": "9e200f41-b979-431d-b94c-8a66193a8ec4"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "Requirement already satisfied: flask in /usr/local/lib/python3.10/dist-packages (2.2.5)\n",
            "Requirement already satisfied: Werkzeug>=2.2.2 in /usr/local/lib/python3.10/dist-packages (from flask) (3.0.2)\n",
            "Requirement already satisfied: Jinja2>=3.0 in /usr/local/lib/python3.10/dist-packages (from flask) (3.1.3)\n",
            "Requirement already satisfied: itsdangerous>=2.0 in /usr/local/lib/python3.10/dist-packages (from flask) (2.1.2)\n",
            "Requirement already satisfied: click>=8.0 in /usr/local/lib/python3.10/dist-packages (from flask) (8.1.7)\n",
            "Requirement already satisfied: MarkupSafe>=2.0 in /usr/local/lib/python3.10/dist-packages (from Jinja2>=3.0->flask) (2.1.5)\n",
            "Collecting pyngrok\n",
            "  Downloading pyngrok-7.1.6-py3-none-any.whl (22 kB)\n",
            "Requirement already satisfied: PyYAML>=5.1 in /usr/local/lib/python3.10/dist-packages (from pyngrok) (6.0.1)\n",
            "Installing collected packages: pyngrok\n",
            "Successfully installed pyngrok-7.1.6\n"
          ]
        }
      ],
      "source": [
        "NGROK_TOKEN = '2f00PVf4uWtcmI3BSgK9fb15J2W_84fRCsurcAT1tatgm1LRu'\n",
        "\n",
        "!pip install flask\n",
        "!pip install pyngrok\n",
        "\n",
        "from pyngrok import ngrok, conf\n",
        "conf.get_default().auth_token=NGROK_TOKEN"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "3AKhTSru7DXd",
        "outputId": "6e6279ac-f692-461d-dac3-cc7dc3a5fdaa"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "/content/Module3\n"
          ]
        }
      ],
      "source": [
        "!pwd"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "colab": {
          "background_save": true,
          "base_uri": "https://localhost:8080/"
        },
        "id": "jOQll5S00XgQ",
        "outputId": "24427d11-0e76-4fc3-a892-4d41423e557e"
      },
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "[<__main__.Post object at 0x7b24a6d56830>, <__main__.Post object at 0x7b2476e86d10>, <__main__.Post object at 0x7b2476e86e30>, <__main__.Post object at 0x7b2476e86f80>, <__main__.Post object at 0x7b2476e86f50>, <__main__.Post object at 0x7b2476e870d0>]\n",
            "NgrokTunnel: \"https://91a7-34-81-185-210.ngrok-free.app\" -> \"http://localhost:5000\"\n",
            " * Serving Flask app '__main__'\n",
            " * Debug mode: off\n"
          ]
        },
        {
          "name": "stderr",
          "output_type": "stream",
          "text": [
            "INFO:werkzeug:\u001b[31m\u001b[1mWARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.\u001b[0m\n",
            " * Running on http://127.0.0.1:5000\n",
            "INFO:werkzeug:\u001b[33mPress CTRL+C to quit\u001b[0m\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:40:52] \"GET / HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:40:52] \"GET /static/css/login.css HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:40:53] \"GET /static/images/login_image.png HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:40:53] \"\u001b[33mGET /favicon.ico HTTP/1.1\u001b[0m\" 404 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:00] \"GET /signup HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:01] \"GET /static/css/signup.css HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:02] \"GET /static/images/signup.png HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:20] \"\u001b[32mPOST /signup HTTP/1.1\u001b[0m\" 302 -\n"
          ]
        },
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "email: musugusuryanarayana@gmail.com,username: VTU15584, password1: 123 ,  confirmpassword: 123\n"
          ]
        },
        {
          "name": "stderr",
          "output_type": "stream",
          "text": [
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:21] \"GET / HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:22] \"\u001b[36mGET /static/css/login.css HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:23] \"\u001b[36mGET /static/images/login_image.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:29] \"\u001b[32mPOST / HTTP/1.1\u001b[0m\" 302 -\n"
          ]
        },
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "username: VTU15584, password1: 123\n"
          ]
        },
        {
          "name": "stderr",
          "output_type": "stream",
          "text": [
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:30] \"GET /home HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:31] \"GET /static/css/home.css HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:31] \"GET /static/images/logo.png HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:41:31] \"GET /static/images/munu-icon.png HTTP/1.1\" 200 -\n"
          ]
        },
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "src chennaidestavadi\n"
          ]
        },
        {
          "name": "stderr",
          "output_type": "stream",
          "text": [
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:02] \"POST /home HTTP/1.1\" 200 -\n"
          ]
        },
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            "<Response [200]>\n",
            "Source: chennai, Destination: avadi\n"
          ]
        },
        {
          "name": "stderr",
          "output_type": "stream",
          "text": [
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:04] \"\u001b[36mGET /static/images/logo.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:04] \"\u001b[36mGET /static/images/munu-icon.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:04] \"GET /static/css/map_1.css HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:54] \"GET /dashboard HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:55] \"GET /static/images/user-3.png HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:55] \"\u001b[36mGET /static/images/munu-icon.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:56] \"GET /static/css/dashboard.css HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:43:56] \"\u001b[36mGET /static/images/logo.png HTTP/1.1\u001b[0m\" 304 -\n",
            "ERROR:__main__:Exception on /help [GET]\n",
            "Traceback (most recent call last):\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 2529, in wsgi_app\n",
            "    response = self.full_dispatch_request()\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1825, in full_dispatch_request\n",
            "    rv = self.handle_user_exception(e)\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1823, in full_dispatch_request\n",
            "    rv = self.dispatch_request()\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1799, in dispatch_request\n",
            "    return self.ensure_sync(self.view_functions[rule.endpoint])(**view_args)\n",
            "  File \"<ipython-input-8-70af5c52e82a>\", line 265, in help\n",
            "    return render_template('help.html', emergency_contact_number=emergency_contact, lat=latitude, long=longitude)\n",
            "NameError: name 'latitude' is not defined\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:44:01] \"\u001b[35m\u001b[1mGET /help HTTP/1.1\u001b[0m\" 500 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:44:28] \"GET /home HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:44:29] \"\u001b[36mGET /static/css/home.css HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:44:29] \"\u001b[36mGET /static/images/logo.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:44:29] \"\u001b[36mGET /static/images/munu-icon.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:45:03] \"GET /videos HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:45:04] \"GET /static/css/map_2.css HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:45:04] \"\u001b[36mGET /static/images/logo.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:45:04] \"\u001b[36mGET /static/images/munu-icon.png HTTP/1.1\u001b[0m\" 304 -\n",
            "ERROR:__main__:Exception on /help [GET]\n",
            "Traceback (most recent call last):\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 2529, in wsgi_app\n",
            "    response = self.full_dispatch_request()\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1825, in full_dispatch_request\n",
            "    rv = self.handle_user_exception(e)\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1823, in full_dispatch_request\n",
            "    rv = self.dispatch_request()\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1799, in dispatch_request\n",
            "    return self.ensure_sync(self.view_functions[rule.endpoint])(**view_args)\n",
            "  File \"<ipython-input-8-70af5c52e82a>\", line 265, in help\n",
            "    return render_template('help.html', emergency_contact_number=emergency_contact, lat=latitude, long=longitude)\n",
            "NameError: name 'latitude' is not defined\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:45:52] \"\u001b[35m\u001b[1mGET /help HTTP/1.1\u001b[0m\" 500 -\n",
            "ERROR:__main__:Exception on /help [GET]\n",
            "Traceback (most recent call last):\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 2529, in wsgi_app\n",
            "    response = self.full_dispatch_request()\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1825, in full_dispatch_request\n",
            "    rv = self.handle_user_exception(e)\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1823, in full_dispatch_request\n",
            "    rv = self.dispatch_request()\n",
            "  File \"/usr/local/lib/python3.10/dist-packages/flask/app.py\", line 1799, in dispatch_request\n",
            "    return self.ensure_sync(self.view_functions[rule.endpoint])(**view_args)\n",
            "  File \"<ipython-input-8-70af5c52e82a>\", line 265, in help\n",
            "    return render_template('help.html', emergency_contact_number=emergency_contact, lat=latitude, long=longitude)\n",
            "NameError: name 'latitude' is not defined\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:46:06] \"\u001b[35m\u001b[1mGET /help HTTP/1.1\u001b[0m\" 500 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:46:21] \"GET /map_2 HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:46:22] \"\u001b[36mGET /static/images/logo.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:46:22] \"\u001b[36mGET /static/images/munu-icon.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:46:22] \"\u001b[36mGET /static/css/map_2.css HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:47:30] \"GET /dashboard HTTP/1.1\" 200 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:47:31] \"\u001b[36mGET /static/css/dashboard.css HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:47:31] \"\u001b[36mGET /static/images/munu-icon.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:47:31] \"\u001b[36mGET /static/images/logo.png HTTP/1.1\u001b[0m\" 304 -\n",
            "INFO:werkzeug:127.0.0.1 - - [15/Apr/2024 07:47:31] \"\u001b[36mGET /static/images/user-3.png HTTP/1.1\u001b[0m\" 304 -\n"
          ]
        }
      ],
      "source": [
        "from flask import Flask, render_template, request, redirect, url_for,flash , jsonify\n",
        "import json\n",
        "import utils\n",
        "import random\n",
        "from pyngrok import ngrok\n",
        "\n",
        "\n",
        "template_dir = '/content/Module3/templates'\n",
        "static_dir = '/content/Module3/static'\n",
        "\n",
        "app = Flask(__name__, template_folder=template_dir, static_folder=static_dir)\n",
        "\n",
        "map = \"map\"\n",
        "\n",
        "global police_station_name\n",
        "global destination\n",
        "global routes_map\n",
        "global source\n",
        "global latitude\n",
        "global longitude\n",
        "\n",
        "#Delete this line\n",
        "# news_list = utils.get_news()[\"articles\"][:6]\n",
        "\n",
        "#Use these two lines\n",
        "news_list = utils.get_news()[\"articles\"]\n",
        "news_list = random.sample(news_list, 6)\n",
        "\n",
        "class Post:\n",
        "    def __init__(self, title, image_url):\n",
        "        self.title = title\n",
        "        self.image_url = image_url\n",
        "\n",
        "\n",
        "with open(\"details.json\", \"r\") as jf:\n",
        "    data = json.load(jf)\n",
        "\n",
        "\n",
        "# Sample posts\n",
        "posts = []\n",
        "for i in range(len(news_list)):\n",
        "    posts.append(Post(news_list[i][\"title\"], news_list[i][\"urlToImage\"]))\n",
        "\n",
        "print(posts)\n",
        "\n",
        "\n",
        "@app.route('/', methods=['GET', 'POST'])\n",
        "def login():\n",
        "    message = request.args.get('message')\n",
        "    if request.method == 'POST':\n",
        "        username = request.form['username']\n",
        "        password = request.form['password1']\n",
        "\n",
        "        # You can add your authentication logic here.\n",
        "        # For demonstration purposes, we'll just print the input data.\n",
        "        print(f'username: {username}, password1: {password}')\n",
        "\n",
        "        if username in data[\"login\"].keys() and data[\"login\"][username]==password:\n",
        "            return redirect(url_for('home'))\n",
        "\n",
        "    return render_template('./login.html' )\n",
        "\n",
        "\n",
        "@app.route('/signup', methods=['GET', 'POST'])\n",
        "def signup():\n",
        "    if request.method == 'POST':\n",
        "        email = request.form['email']\n",
        "        username = request.form['username']\n",
        "        password = request.form['password1']\n",
        "        confirmpassword = request.form['confirmpassword']\n",
        "\n",
        "        # You can add your authentication logic here.\n",
        "        # For demonstration purposes, we'll just print the input data.\n",
        "        print(f'email: {email},username: {username}, password1: {password} ,  confirmpassword: {confirmpassword}')\n",
        "\n",
        "        with open(\"details.json\", \"w\") as jfk:\n",
        "            data[\"login\"][username] = password\n",
        "            json.dump(data, jfk)\n",
        "\n",
        "        return redirect(url_for('login'))\n",
        "\n",
        "    return render_template('./signup.html')\n",
        "\n",
        "\n",
        "@app.route('/home' , methods=['GET', 'POST'] )\n",
        "def home():\n",
        "    # message = request.args.get('message')\n",
        "    global source\n",
        "    global destination\n",
        "    if request.method == 'POST':\n",
        "        source = request.form.get('source')\n",
        "        destination = request.form.get('destination')\n",
        "        print('src ' + source+ \"dest\"+ destination)\n",
        "        # optimize_safety = 'Optimize Safety' in request.form\n",
        "        # avoid_dark_areas = 'Avoid Dark Areas' in request.form\n",
        "\n",
        "         # You can process the form data here or perform any other desired actions\n",
        "        source_lat, source_long = utils.get_lat_long_from_address(source)\n",
        "        destination_lat, destination_long = utils.get_lat_long_from_address(destination)\n",
        "        route = utils.get_route(source_lat, source_long, destination_lat, destination_long)\n",
        "        print( route)\n",
        "        routes_map = utils.create_map(route)\n",
        "\n",
        "        print(f'Source: {source}, Destination: {destination}')\n",
        "\n",
        "\n",
        "\n",
        "        # return redirect(url_for('map_1' , map=routes_map._repr_html_()) )\n",
        "        return render_template('map_1.html' , map=routes_map._repr_html_(), source=source, destination=destination)\n",
        "\n",
        "    return render_template('home.html' , posts=posts)\n",
        "\n",
        "@app.route('/dashboard' , methods=['GET', 'POST'] )\n",
        "def dashboardv():\n",
        "    message = request.args.get('message')\n",
        "\n",
        "    user_details = data[\"profile\"]\n",
        "\n",
        "    if request.method == 'POST':\n",
        "        email = request.form.get('email')\n",
        "        username = request.form.get('username')\n",
        "        contact_number = request.form.get('contact-number')\n",
        "        home_address = request.form.get('home-address')\n",
        "        emergency_number = request.form.get('emergency-number')\n",
        "\n",
        "        # Print the form data to the console\n",
        "        print(f'Email: {email}')\n",
        "        print(f'Username: {username}')\n",
        "        print(f'Contact Number: {contact_number}')\n",
        "        print(f'Home Address: {home_address}')\n",
        "        print(f'Emergency Number: {emergency_number}')\n",
        "\n",
        "        # return redirect(url_for('home'))\n",
        "        with open(\"details.json\", \"w\") as jfd:\n",
        "            profile_data = {\"username\": username, \"email\":email, \"contact\":contact_number, \"address\":home_address, \"emergency\": emergency_number.strip()}\n",
        "            data[\"profile\"] = profile_data\n",
        "            json.dump(data, jfd)\n",
        "\n",
        "    return render_template('dashboard.html', user_details=user_details)\n",
        "\n",
        "\n",
        "\n",
        "@app.route('/dashboard/profile-picture-update', methods=['POST'])\n",
        "def update_profile_picture():\n",
        "    try:\n",
        "        # Check if the 'profilePicture' file is in the request\n",
        "        if 'profilePicture' not in request.files:\n",
        "            return jsonify({'error': 'No file provided'}), 400\n",
        "\n",
        "        file = request.files['profilePicture']\n",
        "        print(file)\n",
        "        # Check if the file is empty\n",
        "        if file.filename == '':\n",
        "            return jsonify({'error': 'No file selected'}), 400\n",
        "\n",
        "        # Save the file to the upload folder\n",
        "\n",
        "\n",
        "        # Return the path to the uploaded file\n",
        "        return jsonify({'profilePicturePath': file.filename})\n",
        "\n",
        "    except Exception as e:\n",
        "        return jsonify({'error': str(e)}), 500\n",
        "\n",
        "\n",
        "@app.route('/map_1' , methods=['GET', 'POST'] )\n",
        "def map_1():\n",
        "    message = request.args.get('message')\n",
        "    # if request.method == 'POST':\n",
        "        # source = request.form.get('source')\n",
        "        # destination = request.form.get('destination')\n",
        "        # # optimize_safety = 'Optimize Safety' in request.form\n",
        "        # # avoid_dark_areas = 'Avoid Dark Areas' in request.form\n",
        "\n",
        "        #  # You can process the form data here or perform any other desired actions\n",
        "\n",
        "        # print(f'Source: {source}, Destination: {destination}')\n",
        "\n",
        "        # return redirect(url_for('home'))\n",
        "\n",
        "\n",
        "    return render_template('map_1.html', source=source)\n",
        "\n",
        "# # Initialize variables\n",
        "# police_station_name = \"\"\n",
        "# destination = \"\"\n",
        "# routes_map = \"\"\n",
        "\n",
        "\n",
        "@app.route('/map_2' , methods=['GET', 'POST'] )\n",
        "def map_2():\n",
        "\n",
        "   try:\n",
        "        # police_station_name = \"Lalbagh Police Station\"\n",
        "        # destination = \"XH3P+H62, Lalbagh Gate, Lal Bagh Rd, Jaya Nagar\"\n",
        "        # routes_map = \"\"\n",
        "\n",
        "        global police_station_name\n",
        "        global destination\n",
        "        global routes_map\n",
        "        global latitude\n",
        "        global longitude\n",
        "\n",
        "        data = request.get_json()\n",
        "        longitude = data.get('longitude')\n",
        "        latitude = data.get('latitude')\n",
        "        print(f'longitude: {longitude}')\n",
        "        print(f'latitude: {latitude}')\n",
        "\n",
        "        police_station_list = utils.get_nearest(latitude, longitude)[\"results\"][0]\n",
        "        police_station_name = police_station_list[\"name\"]\n",
        "        destination = police_station_list[\"address\"]\n",
        "        dest_lat, dest_long = police_station_list[\"location\"][\"lat\"], police_station_list[\"location\"][\"lng\"]\n",
        "        route = utils.get_route(latitude, longitude, dest_lat, dest_long)\n",
        "        routes_map = utils.create_map(route)\n",
        "        print(f'Police Station: {police_station_name}')\n",
        "\n",
        "\n",
        "        return jsonify({\"status\": \"success\", \"police_station_name\": police_station_name , \"destination\": destination, \"map\": routes_map._repr_html_(), })\n",
        "\n",
        "   except Exception as e:\n",
        "         return render_template('map_2.html')\n",
        "\n",
        "\n",
        "\n",
        "@app.route('/map_2/police' , methods=['GET', 'POST'] )\n",
        "def map_2_police():\n",
        "    global police_station_name\n",
        "    global destination\n",
        "    global routes_map\n",
        "\n",
        "    if request.method == 'POST':\n",
        "        print(\"Contact to police\")\n",
        "        # return redirect(url_for('home'))\n",
        "        message =  \"Connected to police\"\n",
        "        return render_template('map_2.html',message = message )\n",
        "\n",
        "    # Pass the data to the HTML template\n",
        "    return render_template('map_2.html', police_station_name=police_station_name,destination=destination , map=routes_map)\n",
        "\n",
        "\n",
        "\n",
        "@app.route('/help', methods=['GET', 'POST'])\n",
        "def help():\n",
        "    message = request.args.get('message')\n",
        "\n",
        "    global latitude\n",
        "    global longitude\n",
        "\n",
        "    # Placeholder for emergency contact number (replace with actual logic to fetch or set the number)\n",
        "    emergency_contact = data[\"profile\"][\"emergency\"]\n",
        "    user_name = data[\"profile\"][\"username\"]\n",
        "\n",
        "    if request.method == 'POST':\n",
        "        print(\"SOS Request received!\")\n",
        "\n",
        "        try:\n",
        "            utils.send_email(emergency_contact, user_name, latitude, longitude)\n",
        "        except Exception as e:\n",
        "            print(e)\n",
        "            return jsonify({\"status\": \"Failed\", \"emergency_contact_number\": emergency_contact})\n",
        "\n",
        "        return jsonify({\"status\": \"success\", \"emergency_contact_number\": emergency_contact})\n",
        "\n",
        "    return render_template('help.html', emergency_contact_number=emergency_contact, lat=latitude, long=longitude)\n",
        "\n",
        "@app.route('/hospital_map' , methods=['GET', 'POST'] )\n",
        "def hospital_map():\n",
        "\n",
        "   try:\n",
        "        # police_station_name = \"Lalbagh Police Station\"\n",
        "        # destination = \"XH3P+H62, Lalbagh Gate, Lal Bagh Rd, Jaya Nagar\"\n",
        "        # routes_map = \"\"\n",
        "\n",
        "        global hospital_name\n",
        "        global dest\n",
        "        global hospital_map\n",
        "        global lat\n",
        "        global longi\n",
        "\n",
        "        data = request.get_json()\n",
        "        longi = data.get('longitude')\n",
        "        lat = data.get('latitude')\n",
        "        print(f'longitude: {longi}')\n",
        "        print(f'latitude: {lat}')\n",
        "\n",
        "        hospital_list = utils.get_nearest_hospital(lat, longi)[\"results\"][0]\n",
        "        hospital_name = hospital_list[\"name\"]\n",
        "        dest = hospital_list[\"address\"]\n",
        "        dest_lat, dest_long = hospital_list[\"location\"][\"lat\"], hospital_list[\"location\"][\"lng\"]\n",
        "        route = utils.get_route(lat, longi, dest_lat, dest_long)\n",
        "        hospital_map = utils.create_map(route)\n",
        "        print(f'Hospital: {hospital_name}')\n",
        "\n",
        "\n",
        "        return jsonify({\"status\": \"success\", \"hospital_name\": hospital_name , \"destination\": dest, \"map\": hospital_map._repr_html_(), })\n",
        "\n",
        "   except Exception as e:\n",
        "         return render_template('hospital_map.html')\n",
        "\n",
        "\n",
        "@app.route('/videos', methods=['GET', 'POST'])\n",
        "def videos():\n",
        "\n",
        "    return render_template('videos.html')\n",
        "\n",
        "\n",
        "ngrok_tunnel = ngrok.connect(5000)\n",
        "print(ngrok_tunnel)\n",
        "\n",
        "if __name__ == '__main__':\n",
        "    app.run(port=5000)"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "YsDAhjmj7Sff"
      },
      "outputs": [],
      "source": []
    }
  ],
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "display_name": "Python 3",
      "name": "python3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "nbformat": 4,
  "nbformat_minor": 0
}
