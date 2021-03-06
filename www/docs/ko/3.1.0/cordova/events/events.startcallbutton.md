---
license: >
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

title: startcallbutton
---

# startcallbutton

[이벤트](events.html) 시작 호출 단추를 누를 때 발생 합니다.

    document.addEventListener("startcallbutton", yourCallbackFunction, false);
    

## 세부 정보

대 한 [이벤트](events.html) 리스너를 등록할 수 있습니다 시작 호출 기본 동작을 재정의 해야 할 경우는 `startcallbutton` [이벤트](events.html).

일반적으로 응용 프로그램을 사용 해야 합니다 `document.addEventListener` 한번 [이벤트](events.html) 리스너를 [연결](../connection/connection.html) 하는 `[deviceready](events.deviceready.html)` 이벤트가 발생 합니다.

## 지원 되는 플랫폼

*   블랙베리 WebWorks (운영 체제 5.0와 더 높은)

## 빠른 예제

    document.addEventListener("startcallbutton", onStartCallKeyDown, false);
    
    function onStartCallKeyDown() {
        // Handle the start call button
    }
    

## 전체 예제

    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
                          "http://www.w3.org/TR/html4/strict.dtd">
    <html>
      <head>
        <title>Start Call Button Example</title>
    
        <script type="text/javascript" charset="utf-8" src="cordova.js"></script>
        <script type="text/javascript" charset="utf-8">
    
        // Wait for device API libraries to load
        //
        function onLoad() {
            document.addEventListener("deviceready", onDeviceReady, false);
        }
    
        // device APIs are available
        //
        function onDeviceReady() {
            // Register the event listener
            document.addEventListener("startcallbutton", onStartCallKeyDown, false);
        }
    
        // Handle the start call button
        //
        function onStartCallKeyDown() {
        }
    
        </script>
      </head>
      <body onload="onLoad()">
      </body>
    </html>