# sin(x), x in [0, 2]
```matlab
%% def arg x
x = 0 : 0.1 : 2 ;

%% def func y
y = sin(x) ;

%% generate 2dplots in a new figure : y(x)
figure ;
title("y = sin(x)")
plot(x, y) ;

%% set axis for figure1, 2d
% set dispaly range
xlim([0 2*pi]) ;

% set axislabels
xlabel("x") ;
ylabel("y") ; 
```

# 200exp(-0.05x)sin(x), 0.8exo(-0.5x)sin(10x)
```matlab
%% def arg x
x = 0 : 1 : 20 ;

%% def func y1 y2
y1 = 200*exp(-0.05*x).*sin(x);
y2 = 0.8*exp(-0.5*x).*sin(10*x);

%% generate 2dplots in a new figure : y1(x), y2(x)
figure ;
title('Multiple Decay Rates') ;
[AX,H1,H2] = plotyy(x,y1,x,y2,'plot');	% generate [y1(x), y2(x)], save [all plots, y1(x)'s y_axel, y2(x)'s y_axel] to [AX, H1, H2]
set(H1,'LineStyle','--')	% set y1's linestyle
set(H2,'LineStyle',':')	% set y2's linestyle

%% set axis for figure1, 2d
xlabel('Time(\musec)') ;
set(get(AX(1),'Ylabel'),'String','Slow Decay') ;
set(get(AX(2),'Ylabel'),'String','Fast Decay') ;
```

# helix
```matlab
%% def arg : x,y,z
x = sin(t) ;
y = cos(t) ; 
z = 0: pi/50: 10*pi;

%% generate 3dplots in a new figure : (x,y,z)
plot3(sin(t),cos(t),t)
grid on %把图片绘制出来，在图片中加一些网格线
axis square %使整个图（连同坐标系）呈方体

%% set axis for figure1, 3d
xlabel('sin(t)')
ylabel('cos(t)')
zlabel('t')

%hold on
%hold off %不保留当前操作
```

# 2 peaks
```matlab
%% def arg : x, y, z
[x, y, z] = peak(100) ;

%% generate 3dplots in a new fiugre : (x, y, z)
mesh(x,y,z)
grid
```
