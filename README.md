## interactive_sound_design
### ΤΜΗΜΑ ΤΕΧΝΩΝ ΗΧΟΥ ΚΑΙ ΕΙΚΟΝΑΣ
ΙΟΝΙΟ ΠΑΝΕΠΙΣΤΗΜΙΟ,
ΠΡΟΓΡΑΜΜΑ ΜΕΤΑΠΤΥΧΙΑΚΩΝ ΣΠΟΥΔΩΝ,
«ΟΠΤΙΚΟΑΚΟΥΣΤΙΚΕΣ ΤΕΧΝΕΣ ΣΤΗΝ ΨΗΦΙΑΚΗ ΕΠΟΧΗ»

## **"White Noise"**


###### Χατζημιχαηλίδου Χριστίνα

###### ava.ada2116



##### Διαδραστικός Ηχητικός Σχεδιασμός

Κωδικός Μαθήματος: ΥΚΒ6

Διδάσκων: Ιωάννης Ζάννος

Κέρκυρα, Χειμερινό Εξάμηνο 2021 - 2021


### Θεωρητική προσέγγιση
>Παραμένοντας σιωπηλοί στο σκοτάδι με μοναδικό ερέθισμα το ροζ θόρυβο ο εγκέφαλός μας αρχίζει να δημιουργεί την ατμόσφαιρα, συμπληρώνοντας ήχους, τους οποίους δεν ακούμε αλλά φανταζόμαστε, αντλώντας τους από την εμπειρία μας στην φύση. Ο λευκός θόρυβος παραπέμπει στο βουητό των ισχυρών ανέμων, στο ορμητικό ποτάμι και το κύμα, στην αδιάκοπη ροή των στοιχείων της φύσης που “καθαρίζουν” την ατμόσφαιρα. Αντίστοιχα ο λευκός θόρυβος “καθαρίζει” το μυαλό από όλες τις περιττές πληροφορίες, την πληθώρα ερεθισμάτων. Αποτελεί δίαυλο καθαρής ροής και ενέργειας προερχόμενης από το συλλογικό ασύνειδο της ζωής στην φύση.         
>
>"Το ηχητικό ερέθισμα του λευκού θορύβου λειτουργεί μέσω μιας διαδικασίας που ονομάζεται ηχητική απόκρυψη ή απόκρυψη θορύβου", δήλωσε ο Michael Grandner, ο οποίος διευθύνει το ερευνητικό πρόγραμμα για τον ύπνο και την υγεία στο Κολέγιο Ιατρικής του Πανεπιστημίου της Αριζόνα.
"Δημιουργεί ένα πέπλο ήχου γύρω σας που απορροφά άλλα ηχητικά κύματα, έτσι ώστε να μην φτάνουν στον εγκέφαλό σας και να μην ανταποκρίνεστε σε αυτά", δήλωσε ο Grandner.
"Ένας άλλος λόγος που ο λευκός θόρυβος ή άλλοι ήχοι μπορεί να προκαλέσουν ύπνο είναι ότι έχουν γίνει μέρος της "τελετουργίας του ύπνου" σας, εκείνων των νυχτερινών συνηθειών που κάνετε και έχουν εκπαιδεύσει τον εγκέφαλό σας να ξεκουράζεται."
### Λειτουργία
>Για την υλοποίηση της εργασίας χρησιμοποιήθηκε ένας αισθητήρας φωτός (photocell), ο οποίος στέλνει δεδομένα στο πρόγραμμα του arduino. Το arduino είναι συνδεδεμένο με το SuperCollider, το οποίο δημιουργεί και διαμορφώνει τον ήχο. 
Η πλακέτα λαμβάνει μετρήσεις από τον αισθητήρα για πέντε δευτερόλεπτα κατά την εκκίνηση ορίζοντας την υψηλότερη και τη χαμηλότερη τιμή που λαμβάνει. Αυτές οι μετρήσεις του αισθητήρα, καθορίζουν την ελάχιστη και τη μέγιστη αναμενόμενη τιμή για τις μετρήσεις που λαμβάνονται κατά τη διάρκεια του βρόχου.
To Super Collider διαβάζει τις προσλαμβάνουσες τιμές και τις εισάγει σε μια Synth. Δημιουργεί θόρυβο (BrownNoise), του οποίου το φάσμα έχει ίση ισχύ σε όλες τις συχνότητες. Διαβάζει τις τιμές που λαμβάνει μέσω της SerialPort και δίνει την φιλτραρισμένη έκδοση αυτού του ήχου καθώς περνάει απο την filterSweep. Με την filterSweep, αλλάζει ο θόρυβος, αντικαθιστώντας τις τιμές στην μεταβλητή freq κατά την αναπαραγωγή. H SynthDef παράγει μια μελωδία με την παραμετροποίηση τυχαίων τιμών ανεξάρτητων απο τις τιμές του αισθητήρα. 
Εναλλάσσοντας τις τιμές της φωτεινότητας που προσλαμβάνει ο αισθητήρας, αυξομειώνεται αντίστοιχα και η συχνότητα του θορύβου. Οι ομόκεντροι μεταλλικοί κύκλοι μέσα απο την κίνηση αντανακλούν το φως δίνοντας περιοδικότητα στον ήχο. Ο παραγόμενος ήχος με αυτόν τον τρόπο “ερμηνεύει” την ένταση, την διάρκεια και τον ρυθμό του αντανακλώμενου φωτός, απο την φωτεινή πηγή στην διάρκεια της ημέρας.
### 
#### [Video](https://youtu.be/saGR-2Q7ig8)
<details>
  <summary>Arduino code</summary>

```C++
int value;
int sensorValue = 0;         // the sensor value
int sensorMin = 1023;        // minimum sensor value
int sensorMax = 0;       
void setup() {
  // put your setup code here, to run once:
  Serial.begin(115200);
  while (millis() < 10000) {
    sensorValue = analogRead(0);

    // record the maximum sensor value
    if (sensorValue > sensorMax) {
      sensorMax = sensorValue;
    }

    // record the minimum sensor value
    if (sensorValue < sensorMin) {
      sensorMin = sensorValue;
    }
  }

}

void loop() {
  // put your main code here, to run repeatedly:
  value = analogRead(0);
  Serial.print(map(value,sensorMin,sensorMax,0,255));
  Serial.print('a');
  delay(1);
}
 ``` 
  </details>
 
 <details>
  <summary>Super Collider code</summary>

```sclang
                                
                               
Tdef.all.do(_.stop);
SerialPort.closeAll;
SerialPort.devices;
~port = SerialPort.new("COM5", 115200);


(
~intArray = [ ];
Tdef(\readValues, {
	{
		~ascii = ~port.read;
		case

		{~ascii == nil} {nil}

		//if arduino sends a digit, add it to the array
		{~ascii.asAscii.isDecDigit}
		{~intArray = ~intArray.add(~ascii.asAscii.digit)}

		//if arduino sends an alphabetic character, convert the array
		//digits to an integer and then clear the array
		{~ascii.asAscii.isAlpha}
		{
			~val = ~intArray.convertDigits;
			~intArray = [ ];
		}

		{true} {nil};
	}.loop;
}).play;
)

(
Tdef(\postValues, {
	{
		~val.postln;
		0.05.wait;
	}.loop;
}).play
)

s.boot;


(
~synth = {
	arg freq=3000;
	var sig;
	sig = BrownNoise.ar(1!2).scope(\brown);
	sig = LPF.ar(sig, freq, 0.05);
}.play;
)





.......................«aurora borealis» by nicolaariutti...................
(
~root = -13;
~revSend = Bus.audio(s, 2);
)
(
s.waitForBoot(
	{

		SynthDef(\bell, {
			|
			freq=556, findex=0, frate=2,
			dur=5, pos=0,
			amp=0.25,
			out=0
			|
			var sigA, sigB, sigC, sig, env, fmod;
			env = EnvGen.ar(Env.triangle(5), doneAction:2);
			fmod = findex * SinOsc.kr(frate, mul:0.5, add:0.5) * Line.kr(0, 1, 7);
			sigA = Pulse.ar(freq + fmod, LFNoise2.kr(1).range(0.2, 0.8) );
			sigB = VarSaw.ar(freq + fmod);
			sigC = WhiteNoise.ar() * 0.125;
			sig = SelectX.ar(LFNoise2.kr(2).range(0, 2), [sigA, sigB, sigC]);
			sig = LPF.ar(sig, freq*4 );
			sig = sig * env * amp;
			Out.ar(out, Pan2.ar(sig, pos));
		}).add;

		s.sync;

		SynthDef(\rev, {
			arg in=0, out=0, mix=1, room=0.8;
			var sig;
			sig = In.ar(in, 2);
			sig = FreeVerb.ar(sig, mix, room);
			Out.ar(out, sig);
		}).add;

		s.sync;

		~rev = Synth(\rev, [\in, ~revSend]);

		x = Pbind(
			\instrument, \bell,
			\out, ~revSend,
			\root, Pfunc({~root}),
			\octave, Pwrand([4, 5, 6, 7], [6,8,4,2].normalizeSum, inf),
			\degree, Prand(Scale.lydian.degrees, inf),
			\ctranspose, Pwhite( -0.05, 0.05, inf),
			\amp, 1.1 * Pexprand(0.001, 0.7) * (1/(Pkey(\octave)+1)),
			\findex, Pexprand(2, 20),
			\frate, Pwhite(1, 25, inf),
			\pos, Pwhite(-0.8, 0.8, inf),
			\dur, Pwhite(0.1, 0.5),
		).asEventStreamPlayer;
		x.play;

});
)


(
Tdef(\filterSweep, {
	{
		//make sure to set appropriate min/max values here
		~synth.set(\freq, ~val.linexp(50,1010,100,6500),\noiseHz,24);
		0.001.wait;
	}.loop;
}).play
)

Tdef(\filterSweep).stop;
~synth.free;
  ```
  </details>


### Βιβλιογραφία (Έντυπη και Ηλεκτρονική)
  * Matthew R.Ebben. Peter Yan, Ana C.Krieger. "The effects of white noise on sleep and duration in individuals living in a high noise environment in New York City" (6 April 2021) https://doi.org/10.1016/j.sleep.2021.03.031 *
  * Sandee LaMotte. "White noise (and pink and brown): The science behind the sounds. Cable News Network. Inc. a Time Warner Company. May 3, 2021." https://edition.cnn.com/2021/03/18/health/white-pink-brown-noise-sleep-wellness/index.html*
  * Michael Grandner. "Sleep and Health".1st Edition - April 16, 2019.*
  * Kelsey McKinney. "THE ART AND SCIENCE OF WHITE NOISE". PACIFIC STANDARD STAFF. https://psmag.com/news/the-art-and-science-of-white-noise*
  
