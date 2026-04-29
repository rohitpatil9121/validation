.PHONY: build clean post

build:
	hugo -t ananke

clean:
	rm -rf dist

post:
	hugo -t ananke new posts/$(POST_NAME).md
	sed -i 's/title: .*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md
	sed -i 's/draft: true/draft: false/' content/posts/$(POST_NAME).md
