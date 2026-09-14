# Permanent data storage on Render

This build is configured for a paid Render Web Service with a 1 GB persistent disk mounted at `/var/data`. The Flask app uses `MANDI_DATA_DIR=/var/data`, so SQLite databases, uploaded files, profiles, and user accounts stored by the app remain under the persistent disk across deploys and restarts.

The app also includes Existing Customer Sign In and New Customer Sign Up. The first registered account becomes the administrator; later self-registered accounts are viewers.

Important: a persistent disk does not recover SQLite files that were already lost from a previous Free Render instance. Before switching, export/backup any data that still exists.
