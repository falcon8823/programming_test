# プログラミングテスト模範プログラム

#1.
<pre>
size(400, 400);
translate(200, 200);

float r = 150;
for(float theta = 0.0; theta <= 2 * PI; theta += PI / 6) {
  float x = r * cos(theta);
  float y = r * sin(theta);
  
  ellipse(x, y, 30, 30);
}
</pre>

# 2.
sin, cosの引数の値を変化させて回転させる方法
<pre>
float r;
float t;

void setup() {
  size(400, 400);
  smooth();
  
  r = 150;
  t = 0;
}

void draw() {
  background(0);
  translate(200, 200);
  
  for(float theta = 0; theta <= 2 * PI; theta += PI / 6) {
    float x = r * cos(theta + t);
    float y = r * sin(theta + t);
    
    ellipse(x, y, 30, 30);
  }
  
  t += 10;
}

</pre>

rotateを使って回転させる方法
<pre>
float r;
float t;

void setup() {
  size(400, 400);
  smooth();
  
  r = 150;
  t = 0;
}

void draw() {
  background(0);
  translate(200, 200);
  
  rotate(t);
  
  for(float theta = 0; theta <= 2 * PI; theta += PI / 6) {
    float x = r * cos(theta);
    float y = r * sin(theta);
    
    ellipse(x, y, 30, 30);
  }
  
  t += 10;
}

</pre>

# 3.
<pre>
size(400, 400);
smooth();

for(int y = 0; y < 10; y++) {
  for(int x = 0; x < 10; x++) {
    rect(40 * x + 2.5, 40 * y + 2.5, 35, 35);
  }
}
</pre>

# 4.
<pre>
size(400, 400);
smooth();

for(int y = 0; y < 10; y++) {
  for(int x = 0; x < 10; x++) {
    fill((x + y) % 2 == 0 ? 0 : 255);
    
    rect(40 * x + 2.5, 40 * y + 2.5, 35, 35);
  }
}
</pre>