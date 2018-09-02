function [A] = load_sparse ( filename )
E = load ( filename );
n = max( max (E (: ,1:2) ));
A = sparse (E(: ,1) , E(: ,2) , 1, n, n);
A = A + A ';
end
