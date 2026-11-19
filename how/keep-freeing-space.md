# Freeing up space without losing a photo

[日本語](keep-freeing-space.ja.md) · [How it works](README.md)

Tethr Keep never removes a photo from the Photos library on trust.

Photos are handled a year at a time, or a month at a time when a year is large, by the date they were taken.

1. **Copy.** The original goes to the owner's own drive. Once it is written, it is read back and compared with what was sent.
2. **Make the lighter version.** The lighter copy is made from the original on the drive — not read again from iCloud.
3. **Check everything again.** Before anything changes in Photos, every copy is read once more and compared with the record.
   A photo that has been edited in Photos since it was copied is left out.
4. **Swap in small batches.** For each small batch, "add the lighter version" and "take out the original" happen as one change to the Photos library.
   So there is no moment when a photo is missing from Photos, and the 30 days in Recently Deleted stay as they are.

Live Photos, RAW+JPEG pairs, edited photos and a few other kinds are left out for now: Keep does not touch them in Photos.
The original comes back with one tap.
