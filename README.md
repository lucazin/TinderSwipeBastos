
# TinderSlideCard
Componente completo para quem precisa de um baralho de cartas dinamico e interativo para Android. Muito parecido com o que encontramos no Tinder. Código totalmente aberto para modificações e melhorias.

| Gif | Video |
| --- | --- |
| ![TinderSwipeBastos_animated](https://meucomercioeletronico.com/tutorial/TinderSwipeBastos_animated.gif)  | [![VIDEO](https://img.youtube.com/vi/r6qHrTARf2U/0.jpg)](https://www.youtube.com/watch?v=r6qHrTARf2U) |
  

## Instalação e uso
Basta importar o projeto do Git para o seu editor ( Android Studio / Eclipse, etc... )

## Configurações e informações úteis ##

#### Populando os cartões
No arquivo SquipeCardFragment.java ( Veja arquivo: https://goo.gl/sIBxC4 ), possuímos o seguinte código:

```
    //Populo o POJO com registros de teste ( Pode busca-los da sua API )
    recordSet = new ArrayList<>();
    
    Notification notification1 =  new Notification();
    notification1.setNome("Guilherme");
    notification1.setSobrenome("B. Bastos");
    notification1.setFoto("uploads/userprofile/A20CF1B8FFB203B95C40EB3BAFE4F78C.jpg");
    notification1.setNome_cidade("São Paulo");
    notification1.setNome_estado("SP");
    recordSet.add(notification1);
    
    Notification notification3 =  new Notification();
    notification3.setNome("Mark");
    notification3.setSobrenome("Zuckerberg");
    notification3.setFoto("uploads/userprofile/A20CF1B8FFA5f64as5saopds58asAFE4F78C.jpg");
    notification3.setNome_cidade("Palo Alto");
    notification3.setNome_estado("CA");
    recordSet.add(notification3);
    
    Notification notification2 =  new Notification();
    notification2.setNome("Bill");
    notification2.setSobrenome("Gates");
    notification2.setFoto("uploads/userprofile/A20CF1B8FFA84d58ad6s89qBAFE4F78C.jpg");
    notification2.setNome_cidade("Washington");
    notification2.setNome_estado("NE");
    recordSet.add(notification2);
    
    Notification notification4 =  new Notification();
    notification4.setNome("Stev");
    notification4.setSobrenome("Jobs");
    notification4.setFoto("uploads/userprofile/ADHJOD8asd121B8FFAd6s89qBAFE4F78C.jpg");
    notification4.setNome_cidade("Palo Alto");
    notification4.setNome_estado("CA");
    recordSet.add(notification4);
```
O código acima popula um POJO, gerando uma List<Notification> recordSet, cada instancia nesta lista será um novo Card.


#### Quais as dependências do gradle?

Para tratar a imagem utilizamos os:
```
    compile 'com.mikhaellopez:circularimageview:3.0.2'
    compile 'com.squareup.picasso:picasso:2.5.2'
```

#### Como alterar o angulo de rotação do cartão?

Para alterar o angulo de rotação do card basta alterar a contante:
```
    private float ROTATION_DEGREES = 10.f;
```
Que está na linha 27 do arquivo SwipeLaunchAdapterView.java ( Veja arquivo: https://goo.gl/50faC5 ).
Ou pode-se alterar o mesmo no XML alterando a mesma constante ROTATION_DEGREES.

#### Como executar o slide do cartão programaticamente?

Para fazer com que o cartão seja removido com a animação programaticamente basta criar o seu Listener com o seguinte código ex:

```
    viewHolder.btnIgnore.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            flingContainer.getTopCardListener().selectRight();
        }
    });
```

#### Onde está a constante da BASE-URL de carregamento das imagens?

Essa contante é o prefixo ( Base Url ) para carregamento das imagens, está no arquivo SquipeCardFragment.java ( Veja arquivo: https://goo.gl/sIBxC4 ) linha 32.

```
    private static final Object API = "http://findme.meucomercioeletronico.com/";
```


### Conclusão

Com este componente podemos fazer diversas aplicações, de forma fácil e rápida.
Espero que tenha ajudado!

Fico a disposição para tirar dúvidas:
guilhermeborgesbastos@gmail.com

## Agradecimentos

com.nkdroid


## Contato
[![VIDEO](https://media.licdn.com/mpr/mpr/shrinknp_100_100/AAEAAQAAAAAAAAgiAAAAJGMwMTQwNTMyLTU2N2EtNDM1NS1iZDMxLTI2ZjVhZDRlNjM2Mw.jpg)](https://www.facebook.com/guilherme.borgesbastos)
