module.exports = class Address {
    constructor(addrport){
        if( new String(addrport.match(/:[0-9]+$/)) == "null" ){
            this.port = "*";
        } else {
            this.port = new String(addrport.match(/:[0-9]+$/)).slice(1);
        };

        if( new String(addrport.match(/\[.+\]:[0-9]+$/)) == "null" ){
            this.type = "v4";
        } else {
            this.type = "v6";
        };

        if ( new String(addrport.match(/\*:\*/)) == "null" ){
            this.addr = addrport.slice(0,(-1 * (this.port.length) - 1));
        } else {
            this.addr = "*";
        };
    }
}
