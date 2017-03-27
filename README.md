# Jokes App
App for [Udacity Android Nanodegree](https://www.udacity.com/course/android-developer-nanodegree-by-google--nd801), Build It Bigger App (Project 4)

# Demo Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=SjPsIqJ6mJY
" target="_blank"><img src="http://img.youtube.com/vi/SjPsIqJ6mJY/0.jpg" 
alt="Demo Video" width="240" height="180" border="10" /></a>

# Description
This Application tells jokes and has paid and free with Ads editions.

Joke App uses:
* JavaLib to get Jokes
* Google Cloud Endpoint to connect locally to JavaLib to get jokes and called from the application through AsyncTask.
* AndroidTest to test that the AsyncTask works successfully.
* AndroidLib that gets the joke in the intent extras and responsable to show this image into a nice activity.

Also The application has paid and free flavors, The free edition have banner and interstatial ads.

# Google Cloud Endpoint IP
Don't forget to add the server address or ip so the app can get the jokes successfully.
This IP exists in app/src/main/java/com/udacity/jokes/GCETask.java
```
  if (myApiService == null) {
            MyApi.Builder builder = new MyApi.Builder(AndroidHttp.newCompatibleTransport(),
                    new AndroidJsonFactory(), null)
                    .setRootUrl("http://<IP>:8080/_ah/api/")
                    .setGoogleClientRequestInitializer(new GoogleClientRequestInitializer() {
                        @Override
                        public void initialize(AbstractGoogleClientRequest<?> request) throws IOException {
                            request.setDisableGZipContent(true);
                        }
                    });
            myApiService = builder.build();
        }
```
                    
# Reference
If you're not familiar with Google Cloud Endpoints, check this link
[Google Cloud End Points](https://github.com/GoogleCloudPlatform/gradle-appengine-templates/tree/master/HelloEndpoints)

# Copyright
Copyright Hazem Madkour
