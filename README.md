# SQL-QUERIES

#INDEXING:

-- First, ensure that the index is created

CREATE INDEX idx_panne_typepanne ON panne (panne);

-- Then, add the foreign key constraint

ALTER TABLE panne

ADD CONSTRAINT fk_panne_typepanne

FOREIGN KEY (panne) REFERENCES typepanne(id)

ON DELETE CASCADE

ON UPDATE CASCADE;

