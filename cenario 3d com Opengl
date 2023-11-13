 	  #include <GL/glut.h>
	#include <stdlib.h>
	#include <stdio.h>
	#include <iostream>
	#include <windows.h>
	#include <iostream>
	#include <windows.h>
	#include <string>

using namespace std;

string a;


float R = 1;
float G = 1;
float B = 1;
// Função para tocar uma nota com uma frequência e duração especificadas
void playNote(int frequency, int duration) {
    Beep(frequency, duration);
}
	
	float angulo = 30.0;
	float anguloX = 0.0;
	float anguloY = 0.0;
	float fAspect = 0.0;
	
	bool luz1Ligada = true;
	bool luz2Ligada = true;

	
	GLfloat light_position[] = {0, 4,0.40, 0};  // Posicione a lâmpada acima da mesa
	
	// Variáveis globais para iluminação
	GLfloat luzAmbiente[] = {0.1, 0.06, 0.06, 1.0};
	GLfloat luzDifusa[] = {0.3, 0.3, 0.3, 1.0};
	GLfloat luzEspecular[] = {0.5, 0.5, 0.5, 1.0};
	
	
	int NUMERO_TECLAS = 17;

typedef struct Teclas {
  
    float pX_Teclas;
    
} Tecla;

	Teclas Teclas[17];

	
	
void chao() {
			// Cores do material
		GLfloat camurcaAmbiente[] = {0.6, 0.3, 0.1, 1.0};    // Cor ambiente da camurça
		GLfloat camurcaDifusa[] = {0.6, 0.3, 0.1, 1.0};      // Cor difusa da camurça
		GLfloat camurcaEspecular[] = {0.2, 0.2, 0.2, 1.0};   // Cor especular da camurça
		GLfloat brilho = 1.0;                                  // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, camurcaAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, camurcaDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, camurcaEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    glColor3f(0.47, 0.79, 0.47);
	    glPushMatrix();
	    glTranslated(1, 0.2, 0.8);
	    glScaled(3.0, 0.2, 3.0);
	    glutSolidCube(1.0);
	    glPopMatrix();
	}
	
	void paredeFundo() {
		GLfloat gessoAmbiente[] = {0.9, 0.9, 0.9, 1.0};    // Cor ambiente do gesso
		GLfloat gessoDifusa[] = {0.9, 0.9, 0.9, 1.0};      // Cor difusa do gesso
		GLfloat gessoEspecular[] = {0.2, 0.2, 0.2, 1.0};   // Cor especular do gesso
		GLfloat brilho = 0.0;                                // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, gessoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, gessoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, gessoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    glColor3f(0.5, 0.5, 0.5);
	    glPushMatrix();
	    glTranslated(1, 1.10, -0.7);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(3.0, 0.03, 2.0);
	    glutSolidCube(1.0);
	    glPopMatrix();
	}
	
	void paredeFrente() {
		GLfloat gessoAmbiente[] = {0.9, 0.9, 0.9, 1.0};    // Cor ambiente do gesso
		GLfloat gessoDifusa[] = {0.9, 0.9, 0.9, 1.0};      // Cor difusa do gesso
		GLfloat gessoEspecular[] = {0.2, 0.2, 0.2, 1.0};   // Cor especular do gesso
		GLfloat brilho = 0.0;                                // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, gessoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, gessoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, gessoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	    glColor3f(0.5, 0.5, 0.5);
	    glPushMatrix();
	    glTranslated(-0.529, 1.10, 0.8);//(esquerda direita,cima baixo,frente fundo)
	    glRotated(90.0, 0.0, 1.0, 0.0);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(3.0, 0.06, 2.0);//(x,grossura,z)
	    glutSolidCube(1.0);
	    glPopMatrix();
	}
	
	void tecladoMusical(){
		
			// Cores do material
		GLfloat plasticoPretoAmbiente[] = {0.0, 0.0, 0.0, 1.0};  // Cor ambiente do plástico preto
		GLfloat plasticoPretoDifusa[] = {0.0, 0.0, 0.0, 1.0};    // Cor difusa do plástico preto
		GLfloat plasticoPretoEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular do plástico preto
		GLfloat brilho = 0.5;                                      // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, plasticoPretoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, plasticoPretoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, plasticoPretoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
		glPushMatrix();
	    glTranslated(-0.29, 0.83,0.40);
	    glScaled(0.2, 0.01, 0.5);
	    glutSolidCube(1.0);
	    glPopMatrix();
	
	    // Tampa
	    glPushMatrix();
	    glTranslated(1, 1.0,-0.45);
	    glScaled(1.0, 0.05, 0.5);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	    glTranslated(1, 1.05,-0.6);
	    glScaled(1.0, 0.08, 0.2);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    
	    //perna esquerda
	    
	     glPushMatrix();
	    glTranslated(1.4, 0.5,-0.5);
	    glScaled(0.08, 1, 0.1);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	      glPushMatrix();
	    glTranslated(1.4, 0.3,-0.5);
	    glScaled(0.08, 0.1, 0.4);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	    //perna direita
	    
	     glPushMatrix();
	    glTranslated(0.6, 0.5,-0.5);
	    glScaled(0.08, 1, 0.1);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	    glPushMatrix();
	    glTranslated(0.6, 0.3,-0.5);
	    glScaled(0.08, 0.1, 0.4);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	    
		
		
		
	}
	
	 void 	tecla(float x){
		
				// Cores do material
		GLfloat plasticoPretoAmbiente[] = {0.0, 0.0, 0.0, 1.0};  // Cor ambiente do plástico preto
		GLfloat plasticoPretoDifusa[] = {0.0, 0.0, 0.0, 1.0};    // Cor difusa do plástico preto
		GLfloat plasticoPretoEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular do plástico preto
		GLfloat brilho = 3;                                      // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, plasticoPretoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, plasticoPretoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, plasticoPretoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	
	    // tecla
	    glPushMatrix();
	    glTranslated(x, 1.02,-0.40);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	    
	  //0.6 $$ 1.5  de 0.5
	      
		
	}
	
	void estante() {
		
			// Cores do material
		GLfloat madeiraEscuraAmbiente[] = {0.2, 0.1, 0.0, 1.0};  // Cor ambiente da madeira escura
		GLfloat madeiraEscuraDifusa[] = {0.2, 0.1, 0.0, 1.0};    // Cor difusa da madeira escura
		GLfloat madeiraEscuraEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular da madeira escura
		GLfloat brilho = 0.0;                                     // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraEscuraAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraEscuraDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEscuraEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	    // Fundo
	    glColor3f(0.50, 0.30, 0.10);
	    glPushMatrix();
	    glTranslated(0.5, 1.15, -0.7);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.7, 0.02, 0.86);
	    glutSolidCube(2.0);
	    glPopMatrix();
	
	    // Lateral traseira
	    glPushMatrix();
	    glTranslated(-0.2, 1.15, -0.6);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.04, 0.12, 0.86);
	    glutSolidCube(2.0);
	    glPopMatrix();
	
	    // Lateral frontal
	    glPushMatrix();
	    glTranslated(1.2, 1.15, -0.6);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.04, 0.12, 0.86);
	    glutSolidCube(2.0);
	    glPopMatrix();
	
	    // Topo
	    glPushMatrix();
	    glTranslated(0.5, 1.95, -0.58);
	    glScaled(0.7, 0.06, 0.10);
	    glutSolidCube(2.0);
	    glPopMatrix();
	
	    // Meio
	    glPushMatrix();
	    glTranslated(0.5, 1.15, -0.58);
	    glScaled(0.7, 0.06, 0.10);
	    glutSolidCube(2.0);
	    glPopMatrix();
	
	    // Base
	    glPushMatrix();
	    glTranslated(0.5, 0.35, -0.58);
	    glScaled(0.7, 0.06, 0.10);
	    glutSolidCube(2.0);
	    glPopMatrix();
	}
	
	
	
	
	void telapc() {
		
		// Cores do material
		GLfloat vidroAmbiente[] = {0.1, 0.1, 0.1, 0.5};   // Cor ambiente do vidro
		GLfloat vidroDifusa[] = {0.8, 0.8, 0.8, 0.5};     // Cor difusa do vidro
		GLfloat vidroEspecular[] = {1.0, 1.0, 1.0, 0.5};  // Cor especular do vidro
		GLfloat brilho = 2.0;                             // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, vidroAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, vidroDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, vidroEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    float x = -0.50, y = 1.2, z = 0.40;
	    glPushMatrix();
	    glColor3f(0.0, 0.8, 0.990);
	    glTranslated(x, y, z);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.06, 0.9, 0.5);
	    glutSolidCube(1.0);
	    glPopMatrix();
	}
	
	void mesa() {
		
		
		GLfloat madeiraAmbiente[] = {0.6, 0.3, 0.1, 1.0};   // Cor ambiente da madeira
		GLfloat madeiraDifusa[] = {0.6, 0.3, 0.1, 1.0};     // Cor difusa da madeira
		GLfloat madeiraEspecular[] = {0.2, 0.2, 0.2, 1.0};  // Cor especular da madeira
		GLfloat brilho = 0.0;                              // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	
	    glColor3f(0.50, 0.30, 0.10);
	
	    // Tampa
	    glPushMatrix();
	    glTranslated(-0.29, 0.8,0.4);
	    glScaled(0.5, 0.05, 1.5);
	    glutSolidCube(1.0);
	    glPopMatrix();
	
	   
	
	    // Pé esquerdo frente
	    glPushMatrix();
	    glTranslated(-0.29, 0.5, 1.15);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.5, 0.05, 0.64);
	    glutSolidCube(1.0);
	    glPopMatrix();
	
	
	    // Pé direito frente
	    glPushMatrix();
	    glTranslated(-0.29, 0.5, -0.35);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.5, 0.05, 0.64);
	    glutSolidCube(1.0);
	    glPopMatrix();
	}
	
	void teclado(){
		
			// Cores do material
		GLfloat plasticoPretoAmbiente[] = {0.0, 0.0, 0.0, 1.0};  // Cor ambiente do plástico preto
		GLfloat plasticoPretoDifusa[] = {0.0, 0.0, 0.0, 1.0};    // Cor difusa do plástico preto
		GLfloat plasticoPretoEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular do plástico preto
		GLfloat brilho = 0.2;                                      // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, plasticoPretoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, plasticoPretoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, plasticoPretoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
		glPushMatrix();
	    glTranslated(-0.29, 0.83,0.40);
	    glScaled(0.2, 0.01, 0.5);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    
	    //plastico tela
	     float x = -0.51, y = 1.2, z = 0.40;
	    glPushMatrix();
	    glColor3f(0.0, 0.8, 0.990);
	    glTranslated(x, y, z);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.07, 0.95, 0.6);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    
	    //suporte tela
	    glPushMatrix();
	    glColor3f(0.0, 0.8, 0.990);
	    glTranslated(-0.51,  1.1, 0.40);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.07, 0.04, 0.6);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    
	    //suporte base
	    
		glPushMatrix();
	    glTranslated(-0.49, 0.85,0.40);
	    glScaled(0.1, 0.03, 0.4);
	    glutSolidCube(1.0);
	    glPopMatrix();
	
	}
	void computador(){
		
		// Cores do material
		GLfloat plasticoPretoAmbiente[] = {0.0, 0.0, 0.0, 1.0};  // Cor ambiente do plástico preto
		GLfloat plasticoPretoDifusa[] = {0.0, 0.0, 0.0, 1.0};    // Cor difusa do plástico preto
		GLfloat plasticoPretoEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular do plástico preto
		GLfloat brilho = 1.5;                                      // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, plasticoPretoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, plasticoPretoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, plasticoPretoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
		
		 // Pé esquerdo frente
	    glPushMatrix();
	    glTranslated(-0.29, 1.1, -0.23);
	    glRotated(-90.0, 1.0, 0.0, 0.0);
	    glScaled(0.5, 0.2, 0.64);
	    glutSolidCube(1.0);
	    glPopMatrix();
	
	
	}
	void cama() {
				
					/// Cores do material
			GLfloat panoVermelhoAmbiente[] = {0.9, 0.0, 0.0, 1.0};   // Cor ambiente do pano vermelho
			GLfloat panoVermelhoDifusa[] = {0.8, 0.0, 0.0, 1.0};     // Cor difusa do pano vermelho
			GLfloat panoVermelhoEspecular[] = {0.2, 0.2, 0.2, 1.0};  // Cor especular do pano vermelho
			GLfloat brilho = -3;                                   // Brilho do material
			
			// Aplicação das cores do material
			glMaterialfv(GL_FRONT, GL_AMBIENT, panoVermelhoAmbiente);
			glMaterialfv(GL_FRONT, GL_DIFFUSE, panoVermelhoDifusa);
			glMaterialfv(GL_FRONT, GL_SPECULAR, panoVermelhoEspecular);
			glMaterialf(GL_FRONT, GL_SHININESS, brilho);
			glColor3f(1, 0.30, 0.10);
			
			//cama
			glPushMatrix();
			glTranslated(2.1, 0.4, 0.3); // Posição da tampa da cama
			glScaled(0.7, 0.4, 1.98);
			glutSolidCube(1.0);
			glPopMatrix();
	
	   
	}
	void estrutura_cama(){
			
					
			GLfloat madeiraAmbiente[] = {0.6, 0.3, 0.1, 1.0};   // Cor ambiente da madeira
			GLfloat madeiraDifusa[] = {0.6, 0.3, 0.1, 1.0};     // Cor difusa da madeira
			GLfloat madeiraEspecular[] = {0.5, 0.5, 0.2, 1.0};  // Cor especular da madeira
			GLfloat brilho = 1;                              // Brilho do material
			
			// Aplicação das cores do material
			glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraAmbiente);
			glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraDifusa);
			glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEspecular);
			glMaterialf(GL_FRONT, GL_SHININESS, brilho);
		
		
		    glColor3f(0.50, 0.30, 0.10);
		    
			//base
			glPushMatrix();
			glTranslated(2.1, 0.4, 0.3); // Posição da tampa da cama
			glScaled(0.8, 0.2, 2);
			glutSolidCube(1.0);
			glPopMatrix();
			
				//base
			glPushMatrix();
			glTranslated(2.1, 0.8, -0.65); // Posição da tampa da cama
			glScaled(0.8, 0.6, 0.08);
			glutSolidCube(1.0);
			glPopMatrix();
		
	}
	
	void copo(){
		
		
		// Cores do material
		GLfloat vidroAmbiente[] = {0.1, 0.1, 0.1, 0.5};   // Cor ambiente do vidro
		GLfloat vidroDifusa[] = {0.8, 0.8, 0.8, 0.5};     // Cor difusa do vidro
		GLfloat vidroEspecular[] = {1.0, 1.0, 1.0, 0.5};  // Cor especular do vidro
		GLfloat brilho = -0.5;                             // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, vidroAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, vidroDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, vidroEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    // Posição do copo
	    glTranslatef(-0.29, 1,1);
	
	    // Cor do copo
	    glColor3f(1, 1, 1);
		glRotatef(90, 1, 0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do copo
	    GLUquadricObj* copoObj = gluNewQuadric();
	    gluCylinder(copoObj, 0.05, 0.05, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj);
	
	    // Desenha a base do copo
	    glTranslatef(0,0,0.167);
	    glutSolidCone(0.08, 0.008, 32, 32);
	
	    glPopMatrix();
	    
	}
	
	void plateleira() {
		
		
		GLfloat madeiraAmbiente[] = {0.6, 0.3, 0.1, 1.0};   // Cor ambiente da madeira
		GLfloat madeiraDifusa[] = {0.6, 0.3, 0.1, 1.0};     // Cor difusa da madeira
		GLfloat madeiraEspecular[] = {0.5, 0.5, 0.2, 1.0};  // Cor especular da madeira
		GLfloat brilho = 0.0;                              // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	
	    glColor3f(0.50, 0.30, 0.10);
	
	    // Tampa
	    glPushMatrix();
	    glTranslated(0.7,1.8 ,-0.55);
	    glScaled(1.1, 0.05, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
}

void boneco() {
    // Cores do material
    GLfloat corAmbiente[] = {0.8, 0.6, 0.4, 1.0};     // Cor ambiente do boneco
    GLfloat corDifusa[] = {0.8, 0.6, 0.4, 1.0};       // Cor difusa do boneco
    GLfloat corEspecular[] = {0.5, 0.5, 0.5, 1.0};    // Cor especular do boneco
    GLfloat brilho = 1.3;                             // Brilho do material

    // Aplicação das cores do material
    glMaterialfv(GL_FRONT, GL_AMBIENT, corAmbiente);
    glMaterialfv(GL_FRONT, GL_DIFFUSE, corDifusa);
    glMaterialfv(GL_FRONT, GL_SPECULAR, corEspecular);
    glMaterialf(GL_FRONT, GL_SHININESS, brilho);

    glColor3f(1, 0.6, 0.4);

    // Corpo
    glPushMatrix();
    glTranslated(0.7, 1.96, -0.55);
    glScaled(0.06, 0.1, 0.06);
    glutSolidCube(1.0);
    glPopMatrix();

    
    //pernas  esquerda
	glPushMatrix();
    glTranslated(0.68, 1.88, -0.55);
    glScaled(0.03, 0.1, 0.06);
    glutSolidCube(1.0);
    glPopMatrix();

    
    //perna Direita
	glPushMatrix();
    glTranslated(0.72, 1.88, -0.55);
    glScaled(0.03, 0.1, 0.06);
    glutSolidCube(1.0);
    glPopMatrix();
    

    // Braço direito
    glPushMatrix();
    glTranslated(0.64, 1.977, -0.5);
    glScaled(0.03, 0.04, 0.18);
    glutSolidCube(1.0);
    glPopMatrix();

    // Braço esquerdo
    glPushMatrix();
    glTranslated(0.77, 1.97, -0.55);
    glScaled(0.03, 0.15, 0.04);
    glutSolidCube(1.0);
    glPopMatrix();
}
void cabecaboneco(){
	 // Cores do material
    GLfloat corAmbiente[] = {0.8, 0.6, 0.4, 1.0};     // Cor ambiente do boneco
    GLfloat corDifusa[] = {0.8, 0.6, 0.4, 1.0};       // Cor difusa do boneco
    GLfloat corEspecular[] = {0.5, 0.5, 0.5, 1.0};    // Cor especular do boneco
    GLfloat brilho = -6;                             // Brilho do material

    // Aplicação das cores do material
    glMaterialfv(GL_FRONT, GL_AMBIENT, corAmbiente);
    glMaterialfv(GL_FRONT, GL_DIFFUSE, corDifusa);
    glMaterialfv(GL_FRONT, GL_SPECULAR, corEspecular);
    glMaterialf(GL_FRONT, GL_SHININESS, brilho);

    glColor3f(1, 0.6, 0.4);
	// Cabeça
    glPushMatrix();
    glTranslated(0.7, 2.09, -0.55);
    glutSolidSphere(0.068, 15, 15);
    glPopMatrix();
    
}

void espada(){
	
		// Cores do material
		GLfloat vidroAmbiente[] = {0.1, 0.1, 0.1, 0.5};   // Cor ambiente do vidro
		GLfloat vidroDifusa[] = {0.8, 0.8, 0.8, 0.5};     // Cor difusa do vidro
		GLfloat vidroEspecular[] = {1.0, 1.0, 1.0, 0.5};  // Cor especular do vidro
		GLfloat brilho = 3.0;                             // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, vidroAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, vidroDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, vidroEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	
		
	    glPushMatrix();
	    glTranslated(0.64, 2.1, -0.45);
	    glScaled(0.01, 0.3, 0.02);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    
	    //punhal
	    glPushMatrix();
	    glTranslated(0.64, 2.01, -0.45);
	    glScaled(0.05, 0.01, 0.02);
	    glutSolidCube(1.0);
	    glPopMatrix();
    
	
}


	 void 	tecla_preta(){	
	 	// Cores do material
		GLfloat plasticoPretoAmbiente[] = {0.0, 0.0, 0.0, 1.0};  // Cor ambiente do plástico preto
		GLfloat plasticoPretoDifusa[] = {0.0, 0.0, 0.0, 1.0};    // Cor difusa do plástico preto
		GLfloat plasticoPretoEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular do plástico preto
		GLfloat brilho = 0.5;                                      // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, plasticoPretoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, plasticoPretoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, plasticoPretoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	
	    // tecla
	    glPushMatrix();
	    glTranslated(0.625, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    
	    
	    // tecla
	    glPushMatrix();
	    glTranslated(0.725, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	     // tecla
	    glPushMatrix();
	    glTranslated(0.775, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	      // tecla
	    glPushMatrix();
	    glTranslated(0.825, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	       // tecla
	    glPushMatrix();
	    glTranslated(0.925, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    //teclas
	    glPushMatrix();
	    glTranslated(0.975, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    //teclas
	    glPushMatrix();
	    glTranslated(1.025, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    //teclas
	    glPushMatrix();
	    glTranslated(1.125, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	     //teclas
	    glPushMatrix();
	    glTranslated(1.225, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	    //teclas
	    glPushMatrix();
	    glTranslated(1.275, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	     //teclas
	    glPushMatrix();
	    glTranslated(1.325, 1.03,-0.48);
	    glScaled(0.04, 0.02, 0.3);
	    glutSolidCube(1.0);
	    glPopMatrix();
	    glPushMatrix();
	   
	    
	
	      
		
	}
	
	

void abajur(){
	
	    //Cores do material
		GLfloat vidroAmbiente[] = {0.1, 0.1, 0.1, 0.5};   // Cor ambiente do vidro
		GLfloat vidroDifusa[] = {0.8, 0.8, 0.8, 0.5};     // Cor difusa do vidro
		GLfloat vidroEspecular[] = {1.0, 1.0, 1.0, 0.5};  // Cor especular do vidro
		GLfloat brilho = -3;                             // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, vidroAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, vidroDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, vidroEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    // Posição do abajur
	    glTranslatef(2.1,1.1,2);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(270, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj = gluNewQuadric();
	    gluCylinder(copoObj, 0.06, 0.03, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj);
	    
	     glPopMatrix();
	
	
}


	void tapete(){
		
			/// Cores do material
			GLfloat panoVermelhoAmbiente[] = {0.9, 0.0, 0.0, 1.0};   // Cor ambiente do pano vermelho
			GLfloat panoVermelhoDifusa[] = {0.8, 0.0, 0.0, 1.0};     // Cor difusa do pano vermelho
			GLfloat panoVermelhoEspecular[] = {0.5, 0.2, 0.3, 1.0};  // Cor especular do pano vermelho
			GLfloat brilho = -3;                                   // Brilho do material
			
			// Aplicação das cores do material
			glMaterialfv(GL_FRONT, GL_AMBIENT, panoVermelhoAmbiente);
			glMaterialfv(GL_FRONT, GL_DIFFUSE, panoVermelhoDifusa);
			glMaterialfv(GL_FRONT, GL_SPECULAR, panoVermelhoEspecular);
			glMaterialf(GL_FRONT, GL_SHININESS, brilho);
			
			glColor3f(1, 0.30, 0.10);
	
	    // Posição do copo
	    glTranslatef(-0.29, 0.988,1);
	    glRotatef(90, 1, 0, 0.0); // Gira em torno do eixo Y
		
		
		 // Desenha a base do copo
	    glTranslatef(1,-0.55,0.68);
	    glutSolidCone(0.8, 0.008, 32, 32);
	
	    glPopMatrix();
		
		
	}
	
	

void Estante(){

  
 			GLfloat madeiraAmbiente[] = {0.4, 0.1, 0.1, 1.0};   // Cor ambiente da madeira
			GLfloat madeiraDifusa[] = {0.6, 0.3, 0.1, 1.0};     // Cor difusa da madeira
			GLfloat madeiraEspecular[] = {0.5, 0.5, 0.2, 1.0};  // Cor especular da madeira
			GLfloat brilho = 1;                              // Brilho do material
			
			// Aplicação das cores do material
			glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraAmbiente);
			glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraDifusa);
			glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEspecular);
			glMaterialf(GL_FRONT, GL_SHININESS, brilho);
		
		
		    glColor3f(0.50, 0.30, 0.10);
		    
			//base
			glPushMatrix();
			glTranslated(2.3, 0.5, 2); // Posição da tampa da cama
			glScaled(0.4, 0.5, 0.5);
			glutSolidCube(1.0);
			glPopMatrix();
			
			//plateleira
			glPushMatrix();
			glTranslated(2.28, 0.36, 2);
			glScaled(0.4, 0.35, 0.5);
			glutSolidCube(1.0);
			glPopMatrix();
			
			//plateleira
			glPushMatrix();
			glTranslated(2.28, 0.65, 2);
			glScaled(0.4, 0.15, 0.5);
			glutSolidCube(1.0);
			glPopMatrix();
			
			//puxador
			glPushMatrix();
			glTranslated(2.08, 0.65, 2);
			glScaled(0.05, 0.05, 0.1);
			glutSolidCube(1.0);
			glPopMatrix();
			
				//puxador
			glPushMatrix();
			glTranslated(2.08, 0.4, 2);
			glScaled(0.05, 0.05, 0.1);
			glutSolidCube(1.0);
			glPopMatrix();
	    
	    
	    
	}
	
	

void CompAbajur(){
	
	
	//Cores do material
		GLfloat vidroAmbiente[] = {0.1, 0.1, 0.1, 0.5};   // Cor ambiente do vidro
		GLfloat vidroDifusa[] = {0.8, 0.8, 0.8, 0.5};     // Cor difusa do vidro
		GLfloat vidroEspecular[] = {1.0, 1.0, 1.0, 0.5};  // Cor especular do vidro
		GLfloat brilho = 0;                             // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, vidroAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, vidroDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, vidroEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    // Posição do abajur
	    glTranslatef(2.3,0.5,2);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(270, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj = gluNewQuadric();
	    gluCylinder(copoObj, 0.02, 0.02, 0.6, 32, 32);
	    gluDeleteQuadric(copoObj);
	    
	     glPopMatrix();
	     
	     
	    // Posição do abajur
	    glTranslatef(2.08,1.3,2);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(90, 1,1, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj1 = gluNewQuadric();
	    gluCylinder(copoObj1, 0.02, 0.02, 0.3, 32, 32);
	    gluDeleteQuadric(copoObj1);
	    
	     glPopMatrix();
	     
	       // Posição do abajur
	    glTranslatef(2.3,0.75,2);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(270, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj2 = gluNewQuadric();
	    gluCylinder(copoObj2, 0.08, 0.02, 0.05, 32, 32);
	    gluDeleteQuadric(copoObj2);
	    
	     glPopMatrix();
	     
	       // Posição do abajur
	    glTranslatef(2.1,1.3,2);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(270, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj3 = gluNewQuadric();
	    gluCylinder(copoObj3, 0.03, 0.001, 0.003, 32, 32);
	    gluDeleteQuadric(copoObj3);
	    
	     glPopMatrix();
	     
	     
	     
	
	
	
	
}

void violao(){
	
	
 			GLfloat madeiraAmbiente[] = {0.4, 0.1, 0.1, 1.0};   // Cor ambiente da madeira
			GLfloat madeiraDifusa[] = {0.3, 0.0, -0.8, 1.0};     // Cor difusa da madeira
			GLfloat madeiraEspecular[] = {0.5, 0.5, 0.2, 1.0};  // Cor especular da madeira
			GLfloat brilho = -3;                              // Brilho do material
			
			// Aplicação das cores do material
			glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraAmbiente);
			glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraDifusa);
			glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEspecular);
			glMaterialf(GL_FRONT, GL_SHININESS, brilho);
		
		
		glColor3f(0.30, 0.15, 0.05);
	
		glTranslatef(-0.4, 1, 1.7);
		
		glRotatef(270, 0, 1, 0.0); // Gira em torno do eixo Y
		
		// Desenha o corpo do abajur
		GLUquadricObj* copoObj = gluNewQuadric();
		gluQuadricDrawStyle(copoObj, GLU_FILL); // Configura o estilo para preenchimento
		
		// Desenha o cilindro
		gluCylinder(copoObj, 0.21, 0.21, 0.1, 32, 32);
		
		gluQuadricOrientation(copoObj, GLU_INSIDE); // Inverte a orientação para a esfera interior
		gluDisk(copoObj, 0, 0.21, 32, 1); // Desenha o disco inferior
		
		gluDeleteQuadric(copoObj);
		
		glPopMatrix();
		
		glTranslatef(-0.4, 1.25, 1.7);
		// Cor do abajur
		glColor3f(1, 0, 0);
		glRotatef(270, 0, 1, 0.0); // Gira em torno do eixo Y
		
		// Desenha o corpo do abajur
		GLUquadricObj* copoObj1 = gluNewQuadric();
		gluQuadricDrawStyle(copoObj, GLU_FILL); // Configura o estilo para preenchimento
		
		// Desenha o cilindro
		gluCylinder(copoObj1, 0.17, 0.17, 0.1, 32, 32);
		
		gluQuadricOrientation(copoObj1, GLU_INSIDE); // Inverte a orientação para a esfera interior
		gluDisk(copoObj1, 0, 0.17, 32, 1); // Desenha o disco inferior
		
		gluDeleteQuadric(copoObj);
		
		glPopMatrix();
		
		 glColor3f(0.50, 0.30, 0.10);
		    
			//cabo
			glPushMatrix();
			glTranslated(-0.4, 1.65, 1.7); // Posição da tampa da cama
			glScaled(0.05, 0.8, 0.08);
			glutSolidCube(1.0);
			glPopMatrix();
			
			//cabo
			glPushMatrix();
			glTranslated(-0.4, 2, 1.7); // Posição da tampa da cama
			glScaled(0.08, 0.18, 0.12);
			glutSolidCube(1.0);
			glPopMatrix();
			
			//cavalete
			glPushMatrix();
			glTranslated(-0.4, 0.95, 1.7); // Posição da tampa da cama
			glScaled(0.05, 0.04, 0.18);
			glutSolidCube(1.0);
			glPopMatrix();
			
			
		

					
}
void violao2(){
	
	
 			GLfloat madeiraAmbiente[] = {0.4, 0.1, 0.1, 1.0};   // Cor ambiente da madeira
			GLfloat madeiraDifusa[] = {0.3, 0.0, -0.8, 1.0};     // Cor difusa da madeira
			GLfloat madeiraEspecular[] = {0.5, 0.5, 0.2, 1.0};  // Cor especular da madeira
			GLfloat brilho = 0;                              // Brilho do material
			
			// Aplicação das cores do material
			glMaterialfv(GL_FRONT, GL_AMBIENT, madeiraAmbiente);
			glMaterialfv(GL_FRONT, GL_DIFFUSE, madeiraDifusa);
			glMaterialfv(GL_FRONT, GL_SPECULAR, madeiraEspecular);
			glMaterialf(GL_FRONT, GL_SHININESS, brilho);
		
		
		glColor3f(0.30, 0.16, 0.05);
	
		glTranslatef(-0.39, 1.15, 1.7);
		
		glRotatef(270, 0, 1, 0.0); // Gira em torno do eixo Y
		
		// Desenha o corpo do abajur
		GLUquadricObj* copoObj = gluNewQuadric();
		
		gluQuadricOrientation(copoObj, GLU_INSIDE); // Inverte a orientação para a esfera interior
		gluDisk(copoObj, 0, 0.09, 32, 1); // Desenha o disco inferior
		
		gluDeleteQuadric(copoObj);
		
		glPopMatrix();
	
}


void cadeira(){
	
		//Cores do material
		GLfloat vidroAmbiente[] = {0.1, 0.1, 0.1, 0.5};   // Cor ambiente do vidro
		GLfloat vidroDifusa[] = {0.8, 0.8, 0.8, 0.5};     // Cor difusa do vidro
		GLfloat vidroEspecular[] = {1.0, 1.0, 1.0, 0.5};  // Cor especular do vidro
		GLfloat brilho = 10;                             // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, vidroAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, vidroDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, vidroEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
	
	    // Posição do abajur
	    glTranslatef(0.3,0.44,0.5);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(270, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj = gluNewQuadric();
	    gluCylinder(copoObj, 0.03, 0.03, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj);
	    
	     glPopMatrix();
	     
	     
	    // Posição do abajur
	    glTranslatef(0.32,0.45,0.5);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(90, 1,1, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj1 = gluNewQuadric();
	    gluCylinder(copoObj1, 0.02, 0.02, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj1);
	    
	     glPopMatrix();
	       
	    // Posição do abajur
	    glTranslatef(0.295,0.45,0.52);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(45, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj2 = gluNewQuadric();
	    gluCylinder(copoObj2, 0.02, 0.02, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj2);
	    
	     glPopMatrix();
	        
	    // Posição do abajur
	    glTranslatef(0.29,0.45,0.48);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(138, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj3 = gluNewQuadric();
	    gluCylinder(copoObj3, 0.02, 0.02, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj3);
	    
	     glPopMatrix();
	     
	      // Posição do abajur
	    glTranslatef(0.285,0.45,0.48);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(275, -1,1, 0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj4 = gluNewQuadric();
	    gluCylinder(copoObj4, 0.02, 0.02, 0.2, 32, 32);
	    gluDeleteQuadric(copoObj4);
	    
	     glPopMatrix();
	     
	     
		     
	    glColor3f(1, 0.6, 0.4);
		// Cabeça
	    glPushMatrix();
	    glTranslated(0.29,0.3, 0.65);
	    glutSolidSphere(0.036, 15, 15);
	    glPopMatrix();
	    
	     glColor3f(1, 0.6, 0.4);
		// Cabeça
	    glPushMatrix();
	    glTranslated(0.29,0.3, 0.35);
	    glutSolidSphere(0.036, 15, 15);
	    glPopMatrix();
	     glColor3f(1, 0.6, 0.4);
		// Cabeça
	    glPushMatrix();
	    glTranslated(0.46,0.3, 0.5);
	    glutSolidSphere(0.036, 15, 15);
	    glPopMatrix();
	     glColor3f(1, 0.6, 0.4);
	// Cabeça
	    glPushMatrix();
	    glTranslated(0.15,0.3, 0.5);
	    glutSolidSphere(0.036, 15, 15);
	    glPopMatrix();
	    glColor3f(1, 0.6, 0.4);
	    
	    //SUPORTE ENCOSTO
	    
	    // Posição do abajur
	    glTranslatef(0.48,0.65,0.5);
	
	    // Cor do abajur
	    glColor3f(1, 0, 1);
		glRotatef(270, 1,0, 0.0); // Gira em torno do eixo Y
	    // Desenha o corpo do abajur
	    GLUquadricObj* copoObj5 = gluNewQuadric();
	    gluCylinder(copoObj5, 0.035, 0.035, 0.25, 32, 32);
	    gluDeleteQuadric(copoObj5);
	    
	     glPopMatrix();
	    
	     
	
	
}

void Encostos(){
	
		// Cores do material
		GLfloat plasticoPretoAmbiente[] = {0.0, 0.0, 0.0, 1.0};  // Cor ambiente do plástico preto
		GLfloat plasticoPretoDifusa[] = {0.0, 0.0, 0.0, 1.0};    // Cor difusa do plástico preto
		GLfloat plasticoPretoEspecular[] = {0.1, 0.1, 0.1, 1.0}; // Cor especular do plástico preto
		GLfloat brilho = 0.5;                                      // Brilho do material
		
		// Aplicação das cores do material
		glMaterialfv(GL_FRONT, GL_AMBIENT, plasticoPretoAmbiente);
		glMaterialfv(GL_FRONT, GL_DIFFUSE, plasticoPretoDifusa);
		glMaterialfv(GL_FRONT, GL_SPECULAR, plasticoPretoEspecular);
		glMaterialf(GL_FRONT, GL_SHININESS, brilho);
 
	     //ACENTO
	     glPushMatrix();
				glTranslated(0.31,0.65,0.5);
				glScaled(0.35, 0.05, 0.39);
				glutSolidCube(1.0);
				glPopMatrix();
				
				
		
	     //ACENTO escosto
	     glPushMatrix();
				glTranslated(0.45,1,0.5);
				glScaled(0.05, 0.3, 0.35);
				glutSolidCube(1.0);
				glPopMatrix();
				
				
	     //ACENTO mao esquerda
	     glPushMatrix();
				glTranslated(0.35,0.73,0.7);
				glScaled(0.03, 0.15, 0.03);
				glutSolidCube(1.0);
				glPopMatrix();
				
				 glPushMatrix();
				glTranslated(0.35,0.8,0.7);
				glScaled(0.2, 0.03, 0.045);
				glutSolidCube(1.0);
				glPopMatrix();



	     //ACENTO mao direita
	      glPushMatrix();
				glTranslated(0.35,0.73,0.3);
				glScaled(0.03, 0.15, 0.03);
				glutSolidCube(1.0);
				glPopMatrix();
				
				 glPushMatrix();
				glTranslated(0.35,0.8,0.3);
				glScaled(0.2, 0.03, 0.045);
				glutSolidCube(1.0);
				glPopMatrix();


}

void tocaMusica(unsigned char key, int x, int y) {
    int frequencia = 0;
    int duracao = 500;  // Duração padrão de 500ms

    switch (key) {
        case 'C':
        case 'c':
            frequencia = 520;  // Dó (C)
            break;
        case 'D':
        case 'd':
            frequencia = 592;  // Ré (D)
            break;
        case 'E':
        case 'e':
            frequencia = 643;  // Mi (E)
            break;
        case 'F':
        case 'f':
            frequencia = 690;  // Fá (F)
            break;
        case 'G':
        case 'g':
            frequencia = 392; 
			break; // Sol (G)
        case 'A':
        case 'a':
            frequencia = 440; 
			break; // Lá (A)
        case 'B':
        case 'b':
            frequencia = 493;
			break;  // Si (B)
            
            
        case 'l':
        case 'L':
		    luz1Ligada = !luz1Ligada; 
			printf("Tecla L pressionada. Luz 1 ligada: %d\n", luz1Ligada); // Inverte o estado da luz 1
		   
		    break;
		case 'k':
		case 'K':
		    luz2Ligada = !luz2Ligada;  // Inverte o estado da luz 2
		    
		    break;
        default:
            // Se a tecla pressionada não corresponder a nenhuma nota ou controle de luz, saia da função
            return;
    }

   //glutPostRedisplay();  // Solicita uma atualização da tela

    // Toca a nota com a frequência especificada
    Beep(frequencia, duracao);
}


void Cores (int key) {
    

    switch (key) {
        case '1':
                R = 1;
                G = 0;
                B = 0;
            break;
        default:
            // Se a tecla pressionada não corresponder a nenhuma nota ou controle de luz, saia da função
            return;
    }

}

void iluminacao() {
	    glEnable(GL_LIGHTING);
	    
		  if (luz1Ligada ) {
	        glEnable(GL_LIGHT0);
	         printf("Luz 1 está ligada\n");
	        // Configurar parâmetros de luz para GL_LIGHT0 aqui
	    } else {
	        glDisable(GL_LIGHT0);
	        printf("Luz 1 está desligada\n");
	    }
	
	    if (luz2Ligada ) {
	        glEnable(GL_LIGHT1);
	        // Configurar parâmetros de luz para GL_LIGHT1 aqui
	    } else {
	        glDisable(GL_LIGHT1);
	    }
	
	    glEnable(GL_DEPTH_TEST);
	
	 
	    // Luz da lâmpada
	    GLfloat luzLampadaAmbiente[] = {0.03, 0.03, 0.03, 1.0}; // Reduzido para evitar cores muito claras
	    GLfloat luzLampadaDifusa[] = {0.2,0.2, 0.2, 0.2};
	    GLfloat luzLampadaEspecular[] = {R, G, B, 0.8};
	    
	    // Luz ambiente suave
	    glLightfv(GL_LIGHT0, GL_AMBIENT, luzAmbiente);
	    glLightfv(GL_LIGHT0, GL_DIFFUSE, luzDifusa);
	    glLightfv(GL_LIGHT0, GL_SPECULAR, luzEspecular);
	    
	     // Posição da luz da lâmpada
	    GLfloat luzLampadaPosicao1[] = {0.6, 4,0.3, 0};
	    glLightfv(GL_LIGHT0, GL_POSITION, luzLampadaPosicao1);
	
	    // Defina a direção da luz da lâmpada (apontando para baixo)
	    GLfloat direcaoSpot1[] = {-1, -1, 0};
	    glLightfv(GL_LIGHT0, GL_SPOT_DIRECTION, direcaoSpot1);
	    glLightf(GL_LIGHT0, GL_SPOT_CUTOFF,10.0);    // Ângulo de abertura do cone de luz
	    glLightf(GL_LIGHT0, GL_SPOT_EXPONENT,40.0);
	
	
	    glLightfv(GL_LIGHT1, GL_AMBIENT, luzLampadaAmbiente);
	    glLightfv(GL_LIGHT1, GL_DIFFUSE, luzLampadaDifusa);
	    glLightfv(GL_LIGHT1, GL_SPECULAR, luzLampadaEspecular);
	
	    // Posição da luz da lâmpada
	    GLfloat luzLampadaPosicao[] = {0.6, 4,0.3, 0};
	    glLightfv(GL_LIGHT1, GL_POSITION, luzLampadaPosicao);
	
	    // Defina a direção da luz da lâmpada (apontando para baixo)
	    GLfloat direcaoSpot[] = {-1, -1, 0};
	    glLightfv(GL_LIGHT1, GL_SPOT_DIRECTION, direcaoSpot);
	    glLightf(GL_LIGHT1, GL_SPOT_CUTOFF,10.0);    // Ângulo de abertura do cone de luz
	    glLightf(GL_LIGHT1, GL_SPOT_EXPONENT,20.0); // Expoente de atenuação da luz

	}
	
	void parametrosVisualizacao() {
	    glMatrixMode(GL_PROJECTION);
	    glLoadIdentity();
	    gluPerspective(angulo, fAspect, 0.1, 500);
	    glMatrixMode(GL_MODELVIEW);
	    glLoadIdentity();
	    gluLookAt(5.0, 5.0, 5.0, 0, 1, 0, 0.0, 1.0, 0.0);
	    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
	   
	}
	
	void moveCamera(int key, int x, int y) {
	    if (key == GLUT_KEY_UP) {
	        anguloY -= 1;
	    } else if (key == GLUT_KEY_DOWN) {
	        anguloY += 1;
	    } else if (key == GLUT_KEY_LEFT) {
	        anguloX -= 1;
	    } else if (key == GLUT_KEY_RIGHT) {
	        anguloX += 1;
	    }
	
	    parametrosVisualizacao();
	    glutPostRedisplay();
	    
	}
	
void inicializa() {
	 glClearColor(0.11f, 0.2, 0.25f, 1.0f);
	    angulo = 45;
	    
	       for (int i = 0; i < NUMERO_TECLAS; i++) {
      
        Teclas[i].pX_Teclas = 0.6 + 0.05 * i;
    }
 
}
	void alteraTamanhoJanela(int w, int h) {
	    if (h == 0) h = 1;
	    glViewport(0, 0, w, h);
	    fAspect = (float)w / h;
	    parametrosVisualizacao();
	}
	
	void gerenciaMouse(int button, int state, int x, int y) {
	    if (button == GLUT_RIGHT_BUTTON) {
	        if (state == GLUT_DOWN && angulo < 170) {
	            angulo += 5;
	        }
	    } else if (button == GLUT_LEFT_BUTTON) {
	        if (state == GLUT_DOWN && angulo > 10) {
	            angulo -= 5;
	        }
	    }
	
	    parametrosVisualizacao();
	    glutPostRedisplay();
	    
	}
	
	void renderBitmapString(float x, float y, void *font, const char *string) {
    glRasterPos2f(x, y);

    while (*string) {
        glutBitmapCharacter(font, *string);
        string++;
    }
}

	
	void desenhaPrincipal() {
		
				
	    glRotated(anguloX, 0.0, 1.0, 0.0);
	    glRotated(anguloY, 1.0, 0.0, 0.0);
	    
	    // Mantenha a luz ambiente
	    glLightModelfv(GL_LIGHT_MODEL_AMBIENT, luzAmbiente);
	
	    
		    // Luz pc
	    if (luz1Ligada) {
	        glEnable(GL_LIGHT0);
	        printf("Luz 0 está ligada\n");
			
	    } else {
	        glDisable(GL_LIGHT0);
	        printf("Luz 0 está desigada\n");
	
	       
	    }
	
	    // Defina a posição da lâmpada
	    GLfloat luzLampadaPosicao1[] = {2, 3, 1.95, 1};
	    glLightfv(GL_LIGHT0, GL_POSITION, luzLampadaPosicao1);
	
	    // Defina a direção da lâmpada (apontando para baixo)
	    GLfloat direcaoSpot1[] = {0.0, -1.0, 0.0};
	    glLightfv(GL_LIGHT0, GL_SPOT_DIRECTION, direcaoSpot1);
	
	    // Defina o ângulo de abertura do cone de luz
	    GLfloat anguloAbertura1 = 50.0;
	    glLightf(GL_LIGHT0, GL_SPOT_CUTOFF, anguloAbertura1);

	
		     // Luz pc
	    if (luz2Ligada ) {
	        glEnable(GL_LIGHT1);
	        	
	    } else {
	        glDisable(GL_LIGHT1);
	   
   		 }

	    // Defina a posição da lâmpada
	    GLfloat luzLampadaPosicao[] = {light_position[0], light_position[1], light_position[2], 1.0};
	    glLightfv(GL_LIGHT1, GL_POSITION, luzLampadaPosicao);
	
	    // Defina a direção da lâmpada (apontando para baixo)
	    GLfloat direcaoSpot[] = {0.0, -1.0, 0.0};
	    glLightfv(GL_LIGHT1, GL_SPOT_DIRECTION, direcaoSpot);
	
	    // Defina o ângulo de abertura do cone de luz
	    GLfloat anguloAbertura = 50.0;
	    glLightf(GL_LIGHT1, GL_SPOT_CUTOFF, anguloAbertura);

	     
		glEnable(GL_LIGHT2);
	  

	    
	    for (int i = 0; i < NUMERO_TECLAS; i++) {
        tecla(Teclas[i].pX_Teclas);
    }
	
	  	tecla_preta();
		tecladoMusical();
	    chao();
	    paredeFundo();
	    paredeFrente();
	    cama();
	    telapc();
	    mesa();
	    teclado();
	    computador();
		plateleira();
		boneco();
		cabecaboneco();
		espada();
		estrutura_cama();
		copo();
    	tapete();
		Estante();
		abajur();
		CompAbajur();
		violao();
		violao2();
		cadeira();
		Encostos();
	
		
		glColor3f(1.0, 1.0, 1.0);
		
		
    // Example: Render text at coordinates (10, 10)
    	renderBitmapString(3, 4, GLUT_BITMAP_9_BY_15, "NOTAS MUSICAIS:");
    	renderBitmapString(3.19, 3.8, GLUT_BITMAP_9_BY_15, "Do = c");
    	renderBitmapString(3.22, 3.7, GLUT_BITMAP_9_BY_15, "RE = d");
    	renderBitmapString(3.24, 3.6, GLUT_BITMAP_9_BY_15, "Mi = e");
    	renderBitmapString(3.27, 3.5, GLUT_BITMAP_9_BY_15, "Fa = f");
    	renderBitmapString(3.29, 3.4, GLUT_BITMAP_9_BY_15, "Sol = g");
    	renderBitmapString(3.32, 3.3, GLUT_BITMAP_9_BY_15, "La = a");
    	renderBitmapString(3.34, 3.2, GLUT_BITMAP_9_BY_15, "Si = b");
    	
    	renderBitmapString(-15, 1.5, GLUT_BITMAP_9_BY_15, "Ligar e Desligar Luz do Abajur = L");
    	renderBitmapString(-15.3, 1.2, GLUT_BITMAP_9_BY_15, "Ligar e Desligar Luz do Computador = K");
    	



 
        glFlush();
        
	}
	
	
	
	
	
	
	int main(int argc, char** argv) {
	    glutInit(&argc, argv);
	    glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB | GLUT_DEPTH);
	    glutInitWindowSize(1300, 800);
	    glutCreateWindow("Ambiente 3D");
	    glutDisplayFunc(desenhaPrincipal);
	    glutReshapeFunc(alteraTamanhoJanela);
	    glutSpecialFunc(moveCamera);
	    glutMouseFunc(gerenciaMouse);
	    glutKeyboardFunc(tocaMusica);
	   
	    inicializa();
	   
	
	    iluminacao();
	    parametrosVisualizacao();
	    glutMainLoop();
	    return 0;
	}
	
	  
