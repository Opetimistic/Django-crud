# Django-crud
Creating Views for a Blog app with a Post model.- Zuri Task89


# Created a new GitHub repository with a README.md, and Python .gitignore file.

Cloned it to my machine/computer, to create a new folder on my computer with my repository’s content.

Created a new virtual environment in a cloned folder named env and installed django in it.

Created a new django project using my Zuriboard Student ID as the name of the project.

Created a new application called blog using the django startapp command.

Added the blog app to the main_projects INSTALLED_APPS.

Replaced the content of blog/models.py with the content of this starter file: https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/models.py . We should now have a Post model in blog/models.py.

Created migrations for my new model using the makemigrations django command. 

Ran all migrations using, migrate django command.

Registered the Post model in blog/admin.py to make my Post model accessible from the admin site, 

 
## #Now for the views.# 

#Created a new view/class PostListView in blog/views.py, which inherits django’s generic ListView,  and it’s config/attributes is:

model = Post

 
#Created another view, PostCreateView, which inherits django’s generic CreateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 
#Created another view, PostDetailView, which inherits django’s generic DetailView, with attributes:

model = Post

 
#Create another view PostUpdateView, which inherits django’s generic UpdateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)


#Create another view PostDeleteView, which inherits django’s generic DeleteView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 

# ##Time to create templates.

Create a new folder templates under the blog app.  

Copy all the files and folders from https://github.com/TobeTek/Zuri/tree/main/starter-files/Django-CRUD/templates to blog/templates folder.

 

Create a file, blog/urls.py, if it doesn’t already exist.

Replace the content of blog/urls.py with the content of https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/urls.py 

 

Go to your project_app/urls.py and add a new url pattern with the following content:

path("blog/", include("blog.urls", namespace="blog"))

 

Stage and Commit your Django project and push your changes to your GitHub repository. 