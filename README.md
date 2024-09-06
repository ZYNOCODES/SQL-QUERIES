# SQL-QUERIES

#INDEXING:

-- First, ensure that the index is created 

CREATE INDEX idx_panne_agent ON panne (agent);

-- Then, add the foreign key constraint

ALTER TABLE panne

ADD CONSTRAINT fk_panne_agent

FOREIGN KEY (agent) REFERENCES agent(id)

ON DELETE CASCADE

ON UPDATE CASCADE;

