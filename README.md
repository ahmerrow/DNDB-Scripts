# DNDB-Scripts
Scripts for accessing data from DND Beyond that may be useful to DM's
I have this set up for personal (and my party's) use, but feel free to branch and input your own character numbers.
Character numbers go in the character_list dict in the Table Output cell.  Having the correct names here doesn't matter, as they're pulled from the JSON later.
DND Beyond doesn't have a public API yet, and their JSON files are structured so that you have almost everything you need for calculations, but doesn't surface the finished calcs.  Fortunately the math is well known, you just have to find where the data comes from in the JSON.
Right now, a lot of manual overrides don't work (for example, custom magic bonus to AC isn't tagged as an AC increase in the JSON so it's hard to identify).  Additionally, manually input custom items from the "manage inventory" button don't seem to work, and there seems to be a bug in item customization persistence anyway.  I haven't really tested whether homebrew items work properly, but they seem to.
I'd love to add spell slots used/remaining but I don't want to do the work to calculate available slots as best I can tell it requires inputting all the table info.  You can easily see spells used, but the spells available field in the json is always 0.
Adding columns to the table should be easy to do if you edit table_output(). I don't have scripts for passive investigation or passive insight, but I may update the get_pass_perception to be get_pass_ability and pass in the desired ability as an argument.  
