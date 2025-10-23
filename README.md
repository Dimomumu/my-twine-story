<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>零售客户普法小课堂</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(45deg, #2c3e50, #34495e);
            color: white;
            padding: 30px 20px;
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .header .subtitle {
            font-size: 1.2em;
            opacity: 0.9;
        }
        
        .story-content {
            padding: 30px;
            line-height: 1.8;
            font-size: 1.1em;
        }
        
        .scene {
            background: #f8f9fa;
            border-left: 5px solid #3498db;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
        }
        
        .character {
            font-weight: bold;
            color: #e74c3c;
        }
        
        .dialogue {
            color: #2c3e50;
            margin: 10px 0;
            padding-left: 20px;
        }
        
        .choices {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin: 30px 0;
        }
        
        .choice-btn {
            background: linear-gradient(45deg, #3498db, #2980b9);
            color: white;
            border: none;
            padding: 15px;
            border-radius: 8px;
            font-size: 1.1em;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .choice-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            background: linear-gradient(45deg, #2980b9, #3498db);
        }
        
        .outcome {
            background: #e8f5e8;
            border-left: 5px solid #27ae60;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
            display: none;
        }
        
        .positive {
            background: #e8f5e8;
            border-left-color: #27ae60;
        }
        
        .negative {
            background: #fde8e8;
            border-left-color: #e74c3c;
        }
        
        .restart-btn {
            background: linear-gradient(45deg, #e74c3c, #c0392b);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            font-size: 1.1em;
            cursor: pointer;
            margin: 20px auto;
            display: block;
            transition: all 0.3s ease;
        }
        
        .restart-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.4);
        }
        
        .scene-title {
            color: #3498db;
            font-size: 1.4em;
            margin-bottom: 15px;
            text-align: center;
        }
        
        @media (max-width: 600px) {
            .choices {
                grid-template-columns: 1fr;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .story-content {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>零售客户普法小课堂</h1>
            <div class="subtitle">守法经营 · 诚信为本 · 规范操作</div>
        </div>
        
        <div class="story-content">
            <div id="opening-scene">
                <div class="scene">
                    <h2 class="scene-title">开幕式</h2>
                    <p>清晨，阳光洒在"明诚超市"的招牌上。你是这家社区超市的老板<strong>李伟</strong>，经营卷烟已经五年了。今天像往常一样开门营业，你深知作为卷烟零售户，守法经营是生命线。</p>
                    
                    <p>这时，你的第一位顾客走了进来。他是老熟人<strong>张伯</strong>。</p>
                    
                    <div class="dialogue">
                        <span class="character">张伯：</span>"小李，来包'常青树'，还是老价钱吧？"
                    </div>
                    
                    <div class="dialogue">
                        <span class="character">你：</span>"是啊张伯，明码实价，童叟无欺。"
                    </div>
                    
                    <p style="text-align: center; margin: 20px 0; color: #e74c3c; font-weight: bold;">
                        (故事从这里开始分支，你的选择将决定李伟的未来…)
                    </p>
                    
                    <div class="choices">
                        <button class="choice-btn" onclick="showScene('scene1')">场景一：大宗采购请求</button>
                        <button class="choice-btn" onclick="showScene('scene2')">场景二：未成年人购烟</button>
                        <button class="choice-btn" onclick="showScene('scene3')">场景三：真烟外流风险</button>
                        <button class="choice-btn" onclick="showScene('scene4')">场景四：许可证管理</button>
                    </div>
                </div>
            </div>
            
            <!-- 场景一 -->
            <div id="scene1" class="scene" style="display: none;">
                <h2 class="scene-title">场景一：大宗采购请求</h2>
                <p>张伯刚走，一个穿着得体的陌生男子走进店里，神色匆匆。</p>
                
                <div class="dialogue">
                    <span class="character">陌生人：</span>"老板，你这儿'中华'有多少？我全要了，急着办事用。每包我多加五块钱！"
                </div>
                
                <p>你心里快速盘算了一下。按公司规定，这是明显的价格违规和大宗卷烟异常流动。但这笔生意利润可观，而且对方看起来确实很急。</p>
                
                <p><strong>你会怎么做？</strong></p>
                
                <div class="choices">
                    <button class="choice-btn" onclick="showOutcome('outcome1a')">坚守原则，按规定办理</button>
                    <button class="choice-btn" onclick="showOutcome('outcome1b')">心动应允，做成这笔生意</button>
                </div>
            </div>
            
            <!-- 场景二 -->
            <div id="scene2" class="scene" style="display: none;">
                <h2 class="scene-title">场景二：未成年人购烟</h2>
                <p>一个看起来年纪不大的男孩走进店里，神情有些紧张。</p>
                
                <div class="dialogue">
                    <span class="character">男孩：</span>"老板，买包烟。"
                </div>
                
                <p>你注意到他穿着校服，看起来可能还未成年。根据《未成年人保护法》，不得向未成年人销售烟草制品。</p>
                
                <div class="choices">
                    <button class="choice-btn" onclick="showOutcome('outcome2a')">要求出示身份证件</button>
                    <button class="choice-btn" onclick="showOutcome('outcome2b')">觉得麻烦，直接售卖</button>
                </div>
            </div>
            
            <!-- 结局 -->
            <div id="outcome1a" class="outcome positive" style="display: none;">
                <h3>👍 坚守原则 - 正确选择！</h3>
                <p>听了你的话，陌生人愣了一下，随即笑了。</p>
                
                <div class="dialogue">
                    <span class="character">陌生人：</span>"老板，你真是个实在人。行，就按规矩来，我确实是单位搞活动用，信息可以登记。"
                </div>
                
                <p>你按照规定流程做好了登记，并按标准价格完成了交易。虽然每包少赚了五块，但你心里非常踏实。</p>
                
                <p>几天后，客户经理小陈来访。</p>
                
                <div class="dialogue">
                    <span class="character">小陈：</span>"李老板，我得好好表扬你！上次那个采购方后来给我们反馈了，说你这儿特别规范，还主动宣传了防止卷烟外流的政策，给我们片区树立了正面形象！公司正在评选'诚信示范户'，我准备把你的名字报上去，这可关系到以后的紧俏货源倾斜政策！"
                </div>
                
                <p><strong>结果：</strong> 你因为坚守原则，不仅避免了处罚，还获得了荣誉和潜在的经营优势。</p>
                
                <button class="restart-btn" onclick="restartStory()">重新开始故事</button>
            </div>
            
            <div id="outcome1b" class="outcome negative" style="display: none;">
                <h3>❌ 心动应允 - 错误选择！</h3>
                <p>你暗自窃喜做成了这笔大生意，把店里所有的"中华"都卖给了那个陌生人。</p>
                
                <p>然而，好景不长。两周后，客户经理小陈和市场监管员一同上门，神情严肃。</p>
                
                <div class="dialogue">
                    <span class="character">小陈：</span>"李老板，根据系统监控和市场反馈，你店里的卷烟条包码出现在外地市场，存在真烟异常流动行为。同时，我们接到举报，你此前有溢价销售的行为。根据《诚信经营互助小组公约》和公司规定，我们将对你的档位进行下调，并暂停部分紧俏货源的供应一个月。"
                </div>
                
                <p>你如遭雷击，档位下降意味着长期收入受损，损失远大于当时那点"快钱"。你后悔莫及。</p>
                
                <p><strong>结果：</strong> 因违规经营受到处罚，经营受损。</p>
                
                <button class="restart-btn" onclick="restartStory()">重新开始故事</button>
            </div>
            
            <div id="outcome2a" class="outcome positive" style="display: none;">
                <h3>👍 规范操作 - 正确选择！</h3>
                <p>你礼貌地要求男孩出示身份证件，他支支吾吾拿不出来，最终承认自己还未满18岁。</p>
                
                <div class="dialogue">
                    <span class="character">你：</span>"同学，根据法律规定，我们不能向未成年人销售烟草制品。吸烟有害健康，等你长大了再考虑吧。"
                </div>
                
                <p>男孩有些不好意思地离开了。第二天，市场监管部门进行暗访检查，对你的规范操作给予了表扬。</p>
                
                <p><strong>结果：</strong> 遵守法律法规，避免了潜在的处罚风险。</p>
                
                <button class="restart-btn" onclick="restartStory()">重新开始故事</button>
            </div>
            
            <div id="outcome2b" class="outcome negative" style="display: none;">
                <h3>❌ 违规销售 - 错误选择！</h3>
                <p>你觉得多一事不如少一事，把烟卖给了这个男孩。</p>
                
                <p>一周后，男孩的家长找到店里，非常生气地指责你向未成年人售烟。同时，市场监管部门也接到了举报。</p>
                
                <div class="dialogue">
                    <span class="character">监管人员：</span>"根据《未成年人保护法》第五十九条规定，向未成年人销售烟草制品，可以处五万元以下罚款，情节严重的，责令停业整顿或吊销许可证。"
                </div>
                
                <p><strong>结果：</strong> 面临行政处罚，声誉受损。</p>
                
                <button class="restart-btn" onclick="restartStory()">重新开始故事</button>
            </div>
        </div>
    </div>

    <script>
        function showScene(sceneId) {
            // 隐藏所有场景
            document.querySelectorAll('.scene').forEach(scene => {
                scene.style.display = 'none';
            });
            
            // 隐藏所有结局
            document.querySelectorAll('.outcome').forEach(outcome => {
                outcome.style.display = 'none';
            });
            
            // 显示选中的场景
            document.getElementById(sceneId).style.display = 'block';
        }
        
        function showOutcome(outcomeId) {
            // 隐藏所有场景
            document.querySelectorAll('.scene').forEach(scene => {
                scene.style.display = 'none';
            });
            
            // 隐藏所有结局
            document.querySelectorAll('.outcome').forEach(outcome => {
                outcome.style.display = 'none';
            });
            
            // 显示选中的结局
            document.getElementById(outcomeId).style.display = 'block';
        }
        
        function restartStory() {
            // 隐藏所有场景和结局
            document.querySelectorAll('.scene').forEach(scene => {
                scene.style.display = 'none';
            });
            
            document.querySelectorAll('.outcome').forEach(outcome => {
                outcome.style.display = 'none';
            });
            
            // 显示开场场景
            document.getElementById('opening-scene').style.display = 'block';
        }
        
        // 初始化显示开场
        document.getElementById('opening-scene').style.display = 'block';
    </script>
</body>
</html>
