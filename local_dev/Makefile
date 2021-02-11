ROLES:=$(shell ls roles)

help:
	@echo "test                        uses molecule to test these roles"
	@echo "  roles:"
	@for f in $(ROLES) ; do echo '    '$$f ; done

test: $(ROLES)

$(ROLES):
	(cd roles/$@; molecule test)

.PHONY: help test $(ROLES)

