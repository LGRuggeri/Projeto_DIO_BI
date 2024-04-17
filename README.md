Pesquisa realizada para fazer a relação dos coloabores com os seus gerentes.

select concat(ee.fname," ",ee.minit," ",ee.lname) as nome_colaborador,concat(e1.fname," ",e1.minit," ",e1.lname) as nome_gerente,ee.ssn,ee.super_ssn from employee e
join employee ee on ee.super_ssn = e.super_ssn
left join employee e1 on e1.ssn = ee.super_ssn
group by ee.super_ssn,ee.ssn,nome_colaborador,nome_gerente;
