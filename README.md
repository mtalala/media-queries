Media Queries são uma ferramenta essencial em CSS que possibilita criar layouts responsivos e adaptáveis a diversos dispositivos e formatos de tela. Elas possibilitam que os criadores criem estilos específicos com base nas características do dispositivo, tais como largura, altura e orientação. Utilizando media queries, é viável aprimorar a apresentação de conteúdo para aprimorar a experiência do usuário, assegurando que o design permaneça eficiente e atraente em computadores, tablets e smartphones, além de oferecer suporte para formatação apropriada em impressões. Isso torna o desenvolvimento na internet mais dinâmico e acessível, refletindo as diversas maneiras pelas quais os usuários se relacionam com a web.

A seguir, vamos contextualizar as funcionalidades fundamentais que estão presentes na prova conteceitual deste repositório.

1. Mobile View (Máximo 600px)

``` 
@media (max-width: 600px) {
    .gallery img {
        flex: 1 1 100%; 
    }
}
```

Cada imagem na galeria ocupa 100% da largura disponível em dispositivos com uma resolução máxima de 600 pixels. Isso torna a visualização em uma coluna única, ideal para celulares.

2. Tablet View (601px a 900px)

```
@media (min-width: 601px) and (max-width: 900px) {
    .gallery img {
        flex: 1 1 calc(50% - 20px);
    }
}
```

Para dispositivos com dimensões entre 601px e 900px, as imagens na galeria ocupam 50% da largura, permitindo que duas imagens sejam exibidas lado a lado, com um espaço de 20px entre elas.

3. Desktop View (Mínimo 901px)

```
@media (min-width: 901px) {
    .gallery img {
        flex: 1 1 calc(33.33% - 20px); 
    }
}
```

Em dispositivos com uma resolução superior a 901 pixels, as imagens ocupam 33.33% da largura, permitindo a exibição de três imagens por linha, mantendo um espaçamento de 20px.

4. Impressão

```
@media print {
    header {
        display: none;
    }

    .gallery img {
        flex: 1 1 calc(33.33% - 20px); 
    }

    .gallery img { 
        border-radius: 30px;
    }
}
```

Durante a impressão, o cabeçalho é ocultado para otimizar o espaço disponível. As imagens na galeria estão dispostas em três colunas, assim como na visualização para computador, com bordas arredondadas de 30px para um visual mais agradável.

5. Orientação Portrait

```
@media (orientation: portrait) {
    .gallery img {
        flex: 1 1 100%; 
    }
}
```

Para dispositivos de orientação retrato, as imagens ocupam a totalidade da largura, apresentando uma coluna única.

6. Orientação Landscape

```
@media (orientation: landscape) {
    .gallery img {
        flex: 1 1 calc(33.33% - 20px); 
    }
}
```

Para dispositivos de orientação paisagem, as imagens ocupam 33.33% da largura, o que permite a exibição de três imagens por linha.

Essas media queries permitem que a galeria de imagens seja responsiva e adequada para diversos dispositivos e formatos de visualização, aprimorando a experiência do usuário em telas pequenas, médias e grandes, além de melhorar a apresentação em impressões.

























