# SQL-QUERIES

#ADD INDEXING:

-- First, ensure that the index is created 

CREATE INDEX idx_panne_agent ON panne (agent);

#ADD FOREIGN KEY
-- Then, add the foreign key constraint

ALTER TABLE panne

ADD CONSTRAINT fk_panne_agent

FOREIGN KEY (agent) REFERENCES agent(id)

ON DELETE CASCADE

ON UPDATE CASCADE;

#DELETE 

ALTER TABLE `avancement` DROP FOREIGN KEY `fk_global_geniecivil`;

#MAKE A COLUMN UNIQUE

ALTER TABLE profile ADD CONSTRAINT unique_username UNIQUE (username);


