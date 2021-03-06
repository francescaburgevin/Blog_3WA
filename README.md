��#   B L O G   E N   P H P   N A T I V E 
 
 
 
 L e   b u t   d e   l ' e x e r c i c e   e s t   d e   m e t t r e   e n   p l a c e   u n e   s t r u c t u r e   d ' a p p l i c a t i o n   r e s p e c t a n t   l e   d i s g n P a t t e r n   M V C   v i a   u n   b l o g .   N o u s   a l l o n s   m e t t r e   e n   p l a c e   : 
 
         -   u n   r o u t e r   p e r m a t t a n t   d e   g � r e r   l e s   p a g e s   v i a   l e s   U R L 
 
         -   u n e   a u t h e n t i f i c a t i o n   p e r m e t t a n t   a u x   u t i l i s a t e u r   d e   s e   c o n n e c t e r 
 
         -   C R U D   d ' a r t i c l e   p e r m a t t a n t   d e   g � r e r   l e s   d o n n � e s 
 
         -   u n e   g e s t i o n   d e   f o r m u l a i r e   
 
     
 
 
 
 # #   E T A P E   1   :   R O U T E R 
 
 
 
 N o u s   a l l o n s   c o m m e n c e r   n o t r e   p r o j e t   p a r   l a   m i s e   e n   p l a c e   d u   r o u t e r .   L e   r o u t e r   p e r m e t   d ' � x e c u t e r   l e   c o n t r � l e u r   l i �   �   u n e   U R L ,   p o u r   r e n v o y e r   l a   v u e / t e m p l a t e   d e m a n d �   p a r   l e   c l i e n t . 
 
 
 
 # # #   I n d i c a t i o n s   :   
 
     
 
 L e   p r o j e t   s e   c o m p o s e   d e   4   r � p e r t o i r e s   p r i n c i p a u x   : 
 
     -   l i b   = >   c o r r e s p o n d   a u x   f o n c t i o n n a l i t � s   d e   n o t r e   a p p l i c a t i o n 
 
     -   p u b l i c   = >   c o r r e s p o n d   �   l a   p o r t e   d ' e n t r � e   d e   n o t r e   a p p l i c a t i o n ;   l e   n o m   d e   d o m a i n e   c i b l e   d i r e c t e m e n t   c e   r � p e r t o i r e ;   c e l a   p e r m e t   d e   l i m i t �   l ' a c c � s   d e s   u t i l o i s a t e u r s   a u x   f i c h i e r s   d e   l ' a p p l i c a t i o n 
 
     -   s r c   = >   p a r t i e   l o g i q u e   d e   n o t r e   a p p l i c a t i o n ;   u t i l i s e   l e s   f o n c t i o n n a l i t � s   s t o c k � e s   d a n s   l e   l i b ; 
 
     -   t e m p l a t e   = >   c o r r e s p o n d   a u x   v u e / t e m p l a t e   d e   n o t r e   a p p l i c a t i o n 
 
 L e   r o u t e r   e s t   d � j �   m i s   e n   p l a c e . 
 
 P o u r   l a n c e r   l e   s e r v e r ,   i l   f a u t   s e   m e t t r e   v i a   l e   t e r m i n a l   d a n s   l e   r � p e r t o i r e   r a c i n e   d e   p r o j e t   l e   u t i l i s e r   l a   c o m m a n d e   " p h p   - S   l o c a l h o s t : 8 0 0 0   - t   p u b l i c / " . 
 
 L a   p a g e   h o m e   e s t   a c c e s s i b l e   v i a   l ' u r l   " h t t p : / / l o c a l h o s t : 8 0 0 0 / " 
 
 A t t e n t i o n   p o u r   a c c � d e r   a u x   d i f f � r e n t e s   p a g e ,   i l   f a u t   u t i l i s �   " h t t p : / / l o c a l h o s t : 8 0 0 0 / ? p a g e = n o m _ p a g e " 
 
 
 
 # # #   C o n s i g n e s   : 
 
 
 
 M i s e   e n   p l a c e   d ' u n e   n o u v e l l e   p a g e .   S u r   l e   m � m e   m o d � l e   q u e   l a   p a g e   " h o m e "   c r � e r   u n e   n o u v e l l e   p a g e   n o m m � e   " c o n t a c t " .   I l   f a u d r a   p e n s e r   : 
 
     -   �   a j o u t e r   l a   r o u t e   d a n s   l a   c o n s t a n t e   R O U T I N G 
 
     -   c r � e r   u n   n o u v e a u   c o n t r o l l e r   " C o n t a c t C o n t r o l l e r " 
 
     -   c r � e r   l e   t e m p l a t e   d a n s   t e m p l a t e / c o n t a c t / c o n t a c t _ b a s e . p h t m l 
 
     -   P a s s e r   e n   p a r a m � t r e   d a n s   l a   m e t h o d e   r e n d e r V i e w ( ) ,   u n   t a b l e a u   p a r a m s   a v e c   p o u r   c l �   " m e s s a g e "   e t   e n   v a l e u r   " h e l l o   w o r l d " 
 
     -   A f f i c h e r   l e   m e s s a g e   s u r   l a   p a g e   " C o n t a c t " 
 
 
 
 
 
 # #   E T A P E   2   :   H A B I L L A G E 
 
 
 
 N o u s   a l l o n s   a j o u t e r   u n e   n a v b a r   d a n s   n o t r e   a p p l i c a t i o n   p o u r   f a c i l i t e r   l a   n a v i g a t i o n .   N o u s   a l l o n s   a u s s i   c h a n g e r   l e   b a c k g r o u d - c o l o r .   N o u s   a l l o n s   p o u r   f i n i r   a j o u t e r   u n   c a r r o u s e l . 
 
 V o u s   n ' � t e s   p a s   o b l i g �   d ' u t i l i s e r   b o o t s t r a p . 
 
 
 
 # # #   C o n s i g n e s   : 
 
 # # # # # #   N a v B a r 
 
 -   R e m p l a c e r   l e   c o n t e n u   h t m l   / t e m p l a t e / b a s e . p h t m l   p a r   l e   t e m p l a t e   d e   b a s e   d e   b o o t s t r a p   "   2 .   I n c l u d e   B o o t s t r a p  s   C S S   a n d   J S . "   ( h t t p s : / / g e t b o o t s t r a p . c o m / d o c s / 5 . 2 / g e t t i n g - s t a r t e d / i n t r o d u c t i o n / )   
 
 -   c r � e r   / t e e m p l a t e _ p a r t / _ _ n a v b a r . p h t m l ,   a j o u t e r   u n e   n a v b a r   b o o t s t r a p   ( h t t p s : / / g e t b o o t s t r a p . c o m / d o c s / 5 . 2 / c o m p o n e n t s / n a v b a r / # n a v ) .   A t t e n t i o n ,   i l   f a u t   n e t t o y e r   l e   c o d e .   
 
 -   D a n s   / t e m p l a t e / t e e m p l a t e _ p a r t / _ _ n a v b a r . p h t m l ,   m e t t r e   e n   p l a c e   d e s   l i e n s   v e r s   l e s   d e u x   p a g e s   d e   l ' p p l i c a t i o n 
 
 -   F a i r e   u n   i n c l u d e _ o n c e   d e   " _ _ n a v b a r . p h t m l "   d a n s   / t e m p l a t e / b a s e . p h t m l 
 
 # # # # # #   b a c k g r o u d - c o l o r 
 
 -   c r � e r   l e   f i c h i e r   / p u b l i c / c s s / m a i n . c s s 
 
 -   d a n s   l e   f i c h i e r   / p u b l i c / c s s / m a i n . c s s ,   a j o u t e r   l a   c l a s s e   " b a c k g r o u d - c o l o r   :   # b a d a 5 5 " 
 
 -   l i e r   l e   f i c h i e r   / p u b l i c / c s s / m a i n . c s s   a v e c   l e   f i c h i e r   t e m p l a t e / b a s e . p h t m l 
 
 # # # # # #   c a r r o u s e l 
 
 -   r � c u p � r e r   3   i m a g e s   a u   m o i n s   s u r   l e   s i t e   ( h t t p s : / / p i x a b a y . c o m / f r / ) 
 
 -   p l a c e r   l e s   i m a g e s   d a n s   l e   d o s s i e r   / p u b l i c / i m g / 
 
 -   c r � e r   u n   f i c h i e r   / t e m p l a t e / h o m e / _ _ c a r r o u s e l . p h t m l 
 
 -   r � c u p � r e r   l e   c a r r o u s e l   ( h t t p s : / / g e t b o o t s t r a p . c o m / d o c s / 5 . 2 / c o m p o n e n t s / c a r o u s e l / # w i t h - i n d i c a t o r s ) 
 
 -   i m p l � m e n t e r   l e s   i m g e s   d a n s   l e   c a r r o u s e l 
 
 -   i n c l u r e   l e   c a r r o u s e l   d a n s   l a   p a g e   " H O M E " 
 
 
 
 
 
 # #   E T A P E   3   :   A F F I C H E R   L E S   A R T I C L E S 
 
 
 
 E n   u t i l i s a n t   l a   b a s e   d e   d o n n � � s   d u   f i c h i e r   b a s e . s q l ,   a f f i c h e r   l e s   a r t i c l e s   s u r   u n e   n o u v e l l e   p a g e   n o m m � e   a r t i c l e .   L a   m i s e   e n   f o r m e   e s t   l i b r e ,   v o u s   p o u v e z   u t i l i s e r   b o o t s t r a p . 
 
 
 
 # # #   C o n s i g n e s   : 
 
 -   c r � e r   l a   n o u v e l l e   p a g e   a r t i c l e ,   q u i   c o n t i e n t   u n   t i t r e   " l i s t e   d e s     a r t i c l e s "   e t   u n   t a b l e   q u i   a   p o u r   c o l o n n e   " i d "   " t i t r e "   " d a t e   d e   p u b l i c a t i o n " . 
 
 -   d a n s   l e   f i c h i e r   l i b / R e p o s i t o r y / A b s t r a c t R e p o s i t o r y . p h p ,   c r � e r   l a   c l a s s   A b s t r a c t R e p o s i t o r y   a i n s i 
 
         -   c o n s t a n t e   :   
 
             -     p r i v a t e   c o n s t   D A T A B A S E _ N A M E   =   " m y s q l : h o s t = l o c a l h o s t ; p o r t = 3 3 0 6 ; d b n a m e = m i c r o _ f r a m e w o r k " ; 
 
             -   p r i v a t e   c o n s t   D A T A B A S E _ U S E R N A M E   =   " r o o t " ; 
 
             -   p r i v a t e   c o n s t   D A T A B A S E _ P A S S W O R D   =   " r o o t " ; 
 
         -   m e t h o d e   : 
 
             -   p r i v a t e   f u n c t i o n   c o n n e c t ( ) 
 
             -   p r o t e c t e d   f u n c t i o n   e x e c u t e Q u e r y ( s t r i n g   $ q u e r y ,   s t r i n g   $ c l a s s ,   a r r a y   $ p a r a m s   =   [ ] ) 
 
 -   C r � e r   l e   f i c h i e r   / s r c / M o d e l / A r t i c l e . p h p ,   q u i   e s t   l e   m o d e l   d e   l a   t a b l e   a r t i c l e . 
 
 -   C r � e r   l e   f i c h i e r   / s r c / R e p o s i t o r y / A r t i c l e R e p o s i t o r y . p h p   q u i   c o n t i e n t   l a   c l a s s e   e n f a n t   A r t i c l e R e p o s i t o r y   d e   l a   c l a s s   p a r e n t   A b s t r a c t R e p o s i t o r y 
 
 -   D a n s   l e   f i c h i e r   / s r c / R e p o s i t o r y / A r t i c l e R e p o s i t o r y . p h p ,   c r � e r   u n e   m e t h o d e   f i n d A l l ( )   q u i   r � c u p � r e   t o u s   l e s   a r t i c l e s . 
 
 -   U t i l i s e r   l a   m e t h o d e   f i n d A l l   d a n s   l e   A r t i c l e C o n t r o l l e r   p o u r   r � c u p � r e r   l e s   a r t i c l e s   e t   a f f i c h �   l e s   d a n s   l e   t a b l e   l a   p a g e   a r t i c l e . 
 
 
 
 
 
 # #   E T A P E   4   :   C R E A T I O N   U S E R 
 
 
 
 N o u s   a l l o n s   c r � e r   u n   f o r m u l a i r e   d e   c r � a t i o n   d ' u t i l i s a t e u r   a v e c   h a s h   d u   m o t   d e   p a s s e   e t   i n s e r t i o n   d a n s   l a   b a s e   d e   d o n n � e s . 
 
 
 
 # # #   C o n s i g n e s   :   
 
     -   c r � e r   l a   p a g e   u s e r _ a d d   ( u s e r _ a d d . p h t m l ) ,   a v e c   s o n   c o n t r o l l e r   ( U s e r C o n t r o l l e r - > a d d ( ) ; ) 
 
     -   c r � e r   u n   f o r m u l a i r e   / t e m p l a t e _ p a r t / _ _ a d d _ f o r m . p h t m l   p o u r   c r � e r   u n   u t i l i s a t e u r   d a n s   l a   p a g e   u s e r ,   f a i r e   u n   i n c l u d e   d a n s   l a   p a g e   u s e r _ a d d 
 
     -   c r � e r   l e   M o d e l   U S E R 
 
     -   c r � e r   l e   U s e r R e p o s i t o r y 
 
     -   s o u m e t t r e   l e   f o r m u l a i r e   u s e r _ a d d   s u r   l a   m � m e   p a g e   q u e   l ' a f f i c h a g e   d u   f o r m u l a i r e   
 
     -   u t i l i s �   u n e   c o n d i t i o n   a v e c   $ _ P O S T   p o u r   e x � c u t e r   l e   c o d e   d ' i n s e r t i o n   
 
     -   v � r i f i e r   l a   v a l i d i t �   d e s   d o n n � e s   e t   l e u r s   e x i s t e n c e s   
 
     -   v � r i f i e r   q u e   l e   u s e r n a m e   e s t   u n i q u e   �   u n   u t i l i s a t e u r . 
 
     -   h a s h   l e   m o t   d e   p a s s e   a v e c   p a s s w o r d _ h a s h   ( a l g o :   P A S S W O R D _ B C R Y P T   o p t i o n :   [ " c o s t "   = >   1 2 ] )   
 
     -   F a i r e   l ' i n s e r t   d a n s   l e   f i c h i e r   U s e r R e p o s i t o r y .   
 
     -   C r � e r   l e   n o u v e a u   u s e r   v i a   l e   m o d e l   U s e r . p h p   
 
     -   B o n u s   :   F a i r e   u n   s y s t � m e   d ' e r r e u r   q u i   r e n v o i e   u n   m e s s a g e   d u   s t y l e   " E r r e u r :   l e s   i n f o r m a t i o n s f o u r n i e s   n e   s o n t   p a s   v a l i d e . "   s i   l e s   i n f o r m a t i o n s   n e   s p o n t   p a s   v a l i d e   e t   "   U t i l i s a t e u r   c r � e r . "   s i   l ' u t i l i s a t e u r   e s t   c r � � . 
 
 
 
 
 
 
 
 # #   E T A P E   5   :   a u t h e n t i f i c a t i o n 
 
 
 
 N o u s   a l l o n s   m e t t r e   e n   p l a c e   l ' a u t h e n t i f i c a t i o n   d e s   u t i l i s a t e u r s .   
 
 
 
 # # #   C o n s i g n e s   : 
 
     -   m e t t r e   e n   p l a c e   l a   p a g e   u s e r _ c o n n e x i o n   ( U s e r C o n t r o l l e r - > c o n n e x i o n ( ) ; )   a v e c   u n   f o r m u l a i r e   d e   c o n n e x i o n   u s s e r _ c o n n e x i o n . p h t m l   ( u s e r n a m e ,   p a s s w o r d ) 
 
     -   d a n s   l e   c o n t r o l l e r   U s e r C o n t r o l l e r - > c o n n e x i o n ( )   m e t t r e   e n   p l a c e   l ' a u t h e n t i f i c a t i o n .   P o u r   f a i r e   u n e   a u t h e n t i f i c a t i o n   i l   f a u t   d ' a b o r d   r � c u p � r e r   l ' u t i l i s a t e u r   v i a   s o n   u s e r n a m e   a v n t   d e   v � r i f i �   a v e c   l a   m � t h o d e   p h p   p a s s w o r d _ v e r i f y ( )   l a   v a l i d i t �   d u   m o t   d e   p a s s e   ( h t t p s : / / w w w . p h p . n e t / m a n u a l / f r / f u n c t i o n . p a s s w o r d - v e r i f y . p h p ) 
 
     -   A t t e n t i o n   a v e n t   d e   v � r i f i e r   l e   m o t   d e   p a s s e   v � r i f i e r   q u e   l ' u t i l i s a t e u r   e x i s t e n c e s 
 
     -   L a   p a g e   q u i   s o u m e t   l e   f o r m u l a i r e   e s t   l a   m � m e   q u i   a f f i c h e   l a   v u e   
 
     -   l a   c o n n e c t i o n   s e   f a i t   v i a   l a   v a r i a b l e   g l o b a l e   $ _ S E S S I O N .   S i   l ' u t i l i s a t e u r   a   d o n n � e   d e s   i n f o r m a t i o n s   c o r r e c t e   c r � e r   $ _ S E S S I O N [ " u s e r _ i s _ c e n n e c t e d " ]   =   t r u e ;   A t t e n t i o n   p o u r   p o u v o i r   u t i l i s e r   l e   $ _ S E S S I O N ,   i l   f a u t   i n i t i a l i s e r   l e   s e s s i o n   a v e c   l a   m e t h o d e   s e s s i o n _ s t a r t ( ) ,   p o u r   p l u s   d e   s i m p l i s i t �   l e   p l a c e r   a u   d � b u t   d u   f i c h i e r   p u b l i c / i n d e x . p h p 
 
     -   A f f i c h e r   d a n s   l a   n a v b a r   u n   l i e n   s e   c o n n e c t e r   q u i   r e n v o i e   s u r   l a   p a g e   d e   c o n n e c t i o n   s i   a u c u n   u t i l i s a t e u r   n ' e s t   c o n n e c t e r   
 
     -   B o n u s   :   F a i r e   u n   s y s t � m e   d ' e r r e u r   q u i   r e n v o i e   u n   m e s s a g e   d u   s t y l e   " E r r e u r :   l ' u t i l i s a t e u r   o u   l e   m o t   d e   p a s s e   n e   s o n t   p a s   v a l i d e . "   s i   l e s   i n f o r m a t i o n s   n e   s p o n t   p a s   v a l i d e   e t   "   V o u s   � t e s   c o n n e c t � . "   s i   l ' u t i l i s a t e u r   a r r i v e   �   s e   c o n n e c t e r . 
 
 
 
 
 
 # #   E T A P E   6   :   A F F I C H A G E   D ' U N   A R T I C L E 
 
 
 
 N o u s   a l l o n s   c r � e r   u n e   p a g e   a v e c   n o t r e   a r t i c l e   e n   d � t a i l 
 
 
 
 # # #   C o n s i g n e s 
 
 
 
 
 
 # #   E T A P E   7   :   C R E A T I O N   D ' A R T I C L E 
 
 
 
 N o u s   a l l o n s   m e t t r e   e n   p l a c e   l a   c r � a t i o n   d ' a r t i c l e   l i � e   �   l ' u t i l i s a t e u r   c o u r a n t 
 
 
 
 # # #   C o n s i g n e s 
 
 
 
 
 
 # #   E T A P E   8   :   S U P P R E S S I O N   D ' A R T I C L E 
 
 
 
 N o u s   a l l o n s   m e t t r e   e n   p l a c e   l a   s u p p r e s s i o n   d ' a r t i c l e . 
 
 # # #   C o n s i g n e s 
 
 
 
 
 
 # #   E T A P E   9   :   M O D I F I C A T I O N   D ' A R T I C L E 
 
 
 
 N o u s   a l l o n s   m e t t r e   e n   p l a c e   l a   m o d i f i c a t i o n   d ' a r t i c l e . 
 
 # # #   C o n s i g n e s 
 
 
 
 
 
 # #   E T A P E   1 0   :   C A T E G O R Y 
 
 
 
 D a n s   u n e   n o u v e l l e   p a g e ,   n o u s   a l l o n s   c r � e r   l e   C R U D   p o u r   l e s   c a t e g o r i e s .   N o u s   a f f i c h e r o n s   e n s u i t e   l e s   c a t e g o r i e s   d a n s   u n e   n o u v e l l e   c o l o n n e   d a n s   l a   p a g e   d e   l a   l i s t e   d e   n o s   a r t i c l e s . 
 
 # # #   C o n s i g n e s 
 
 
 
 
 
 # #   E T A P E   1 0   :   C O M M E N T A I R E 
 
 
 
 D a n s   u n e   n o u v e l l e   p a g e ,   n o u s   a l l o n s   c r � e r   l e   C R U D   p o u r   l e s   c a t e g o r i e s .   N o u s   a f f i c h e r o n s   e n s u i t e   l e s   c a t e g o r i e s   d a n s   u n e   n o u v e l l e   c o l o n n e   d a n s   l a   p a g e   d e   l a   l i s t e   d e   n o s   a r t i c l e s . 
 
 # # #   C o n s i g n e s 
 
 
 
 
 
 
 
 
 
 