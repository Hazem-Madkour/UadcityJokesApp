# Jokes App
Udacity Android Nanodegree Build It Bigger App (Project 4)

# Description
This Application uses JavaLib to get Jokes, Google Cloud Endpoint to connect locally to JavaLib to get jokes and called from the application through AsyncTask, AndroidTest to test that the AsyncTask works successfully , and AndroidLib that gets the joke in the intent extras and responsable to show this image into a nice activity.
Also The application has paid and free flavors, The free edition have banner and interstatial ads.

# Google Cloud Endpoint IP
Don't forget to add the server address or ip so the app can get the jokes successfully.
This IP exists in app/src/main/java/com/udacity/jokes/GCETask.java

 new AndroidJsonFactory(), null)
                    .setRootUrl("http://<IP>:8080/_ah/api/")
                    .setGoogleClientRequestInitializer(new GoogleClientRequestInitializer() {
                        @Override
                        public void initialize(AbstractGoogleClientRequest<?> request) throws IOException {
                            request.setDisableGZipContent(true);
                        }
                    });
                    
# Reference
If you're not familiar with Google Cloud Endpoints, check this link
[GoogleCloudEndPoints link](https://github.com/GoogleCloudPlatform/gradle-appengine-templates/tree/master/HelloEndpoints)

# Copyright
Copyright Hazem Madkour
