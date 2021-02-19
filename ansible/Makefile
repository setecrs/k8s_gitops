ROLES:=$(shell ls roles)

help:
	@echo "development                 install the cluster locally"
	@echo "production                  install argocd in production"
	@echo "test                        uses molecule to test these roles"
	@echo "  roles:"
	@for f in $(ROLES) ; do echo '    '$$f ; done

test: $(ROLES)

development:
	$(MAKE) -C $@ local_dev

production:
	$(MAKE) -C $@ production

$(ROLES):
	(cd roles/$@; molecule test)

.PHONY: help test development production $(ROLES)

