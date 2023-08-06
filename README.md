# Để file about chung vị trí với home, base, my-blog


# Cho cái này vào views.py:
@views.route('/my-blog', methods=['GET', 'POST'])
@login_required
def myBlog():
    posts = Post.query.filter_by(user_id=current_user.id)



# Cho cái này vào file css:
.aboutbox{
    position: absolute;
    left: 25%;
    height: fit-content;
    min-height: 600px;
    max-width:fit-content;
    background: transparent;
    border-radius: 20px;
    box-shadow: 0 0 30px rgba(0,0,0,0.5);
    backdrop-filter: blur(20px);
    display: flex;
    justify-content: center;
    align-items: center;
    text-overflow: clip;


}
.text{
    position: relative;
    top: 10px;
    padding: 20px;
    font-weight: 500;
    color:white;
}
.text .abouttitle{
    text-align: center;
    font-size: 2em;

    color: white;

}
.line{
    align-items: center;
    font-weight: 300;
    color: white;
    backdrop-filter: blur(20px);
}
.blogheader{
    border-bottom: 2px white blur(20px);
    position: absolute;
    font-size: 1.5em;
    top: 0;
    left: 20px;
    color: white;
}
