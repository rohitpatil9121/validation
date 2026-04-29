.PHONY: build clean post help

build: ## Build the website using Hugo and generate files in dist/
	hugo -t ananke

clean: ## Remove generated website files (dist directory)
	rm -rf dist

post: ## Create a new blog post using POST_NAME and POST_TITLE
	hugo -t ananke new posts/$(POST_NAME).md
	sed -i 's/title: .*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md
	sed -i 's/draft: true/draft: false/' content/posts/$(POST_NAME).md

help: ## Show this help usage
	@grep -E '^[a-zA-Z_-]+:.*##' Makefile | awk 'BEGIN {FS = ":.*##"}; {printf "%s: %s\n", $$1, $$2}'
