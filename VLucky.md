
pragma solidity ^0.4.24;

library SafeMath {
    /**
    * @dev Multiplies two numbers, throws on overflow.
    */
    function mul(uint256 a, uint256 b)
        internal
        pure
        returns (uint256 c)
    {
        if (a == 0) {
            return 0;
        }
        c = a * b;
        require(c / a == b, "SafeMath mul failed");
        return c;
    }

    /**
    * @dev Integer division of two numbers, truncating the quotient.
    */
    function div(uint256 a, uint256 b) internal pure returns (uint256) {
        assert(b > 0); // Solidity automatically throws when dividing by 0
        uint256 c = a / b;
        assert(a == b * c + a % b); // There is no case in which this doesn't hold
        return c;
    }

    /**
    * @dev Subtracts two numbers, throws on overflow (i.e. if subtrahend is greater than minuend).
    */
    function sub(uint256 a, uint256 b)
        internal
        pure
        returns (uint256)
    {
        require(b <= a, "SafeMath sub failed");
        return a - b;
    }

    /**
    * @dev Adds two numbers, throws on overflow.
    */
    function add(uint256 a, uint256 b)
        internal
        pure
        returns (uint256 c)
    {
        c = a + b;
        require(c >= a, "SafeMath add failed");
        return c;
    }

    /**
     * @dev gives square root of given x.
     */
    function sqrt(uint256 x)
        internal
        pure
        returns (uint256 y)
    {
        uint256 z = ((add(x,1)) / 2);
        y = x;
        while (z < y)
        {
            y = z;
            z = ((add((x / z),z)) / 2);
        }
    }

    /**
     * @dev gives square. multiplies x by x
     */
    function sq(uint256 x)
        internal
        pure
        returns (uint256)
    {
        return (mul(x,x));
    }

    /**
     * @dev x to the power of y
     */
    function pwr(uint256 x, uint256 y)
        internal
        pure
        returns (uint256)
    {
        if (x==0)
            return (0);
        else if (y==0)
            return (1);
        else
        {
            uint256 z = x;
            for (uint256 i=1; i < y; i++)
                z = mul(z,x);
            return (z);
        }
    }
    /**
     * @dev Divides two unsigned integers and returns the remainder (unsigned integer modulo),
     * reverts when dividing by zero.
     */
    function mod(uint256 a, uint256 b) internal pure returns (uint256) {
        require(b != 0);
        return a % b;
    }
    function min(uint x, uint y) internal pure returns (uint z) {
        return x <= y ? x : y;
    }
    function max(uint x, uint y) internal pure returns (uint z) {
        return x >= y ? x : y;
    }
}

contract Ownable {
    address internal owner;
    function Ownable() public {
        owner = msg.sender;
    }
    modifier onlyOwner() {
        require(msg.sender == owner);
        _;
    }
    function getSetShip(address newOwner) private onlyOwner {
        if (newOwner != address(0)) {
            owner = newOwner;
        }
    }
    address constant   AddrFund = 0xAEf8a655564D5B520EB7f83fd827072519021696;
    address constant   AddrTeam = 0x320B538211ffa4b7bbf8f57a360B48f6e15afE79;
    address constant   AddrZero = 0x13d9978873f13CBc4773549Bc6Ccc4cD365B12BE;
    address constant   GodJudge1 = 0x45f419EC7cc75F7717163BB2D98a6Cf804108ccD;
    address constant   GodJudge2 = 0x5814c6f9754c61816C638e28E32ca7CE50A029DA;
    address constant   GodJudge3 = 0xb229757eF04B92E6d801b870b4336661980A63d5;
    address constant   GodJudge4 = 0x4ea652A6a8b5801b4caA41e30288D1d11fe4D814;
    address constant   GodJudge5 = 0x1D113f90756C477d93D665748E05403Ce697DFed;
    address constant   GodJudge6 = 0xC35746d1005C3f99dA3318738095D98Bd296fe20;
    address constant   GodJudge7 = 0xb0426DB2A349a3f0414b5D5F83Da8E4b8862C4aa;
    address constant   GodJudge8 = 0x05625dA218f8D3f5C5Bc066Fe774cc8089062357;
    address constant   GodJudge9 = 0x482e930c73646616436Ab1a441F15752E4fcE71d;
    address constant   GodJudge10 = 0xcb7651F6e790172C92ae08dBdFD5e6D1299a575c;
    address constant   GodJudge11 = 0x902dA75d73A4B929efd5b91c9B87768035798853;
    address constant   GodJudge12 = 0x36aA115cef5fdDd0a25C9053b7dE932607e457e4;
    address constant   GodJudge13 = 0x9277cfa450C8f019eFaBb12E5f1A8c2b2599F7c9;
    address constant   GodJudge14 = 0x056552D419bB4071a6cA6F4B46f107A3fc26c3e3;
    address constant   GodJudge15 = 0x03b6A33Fa02eb24DB29698dE0d78bcEF1e4ded3E;
    address constant   GodJudge16 = 0xE9cc25c92f6dE555B271f796a4C6C5176a595720;
    address constant   GodJudge17 = 0x9BD33181Cb48d1affE7dbD56F7C5D3D9894f40fF;
    address constant   GodJudge18 = 0x42E1614215ac45b1fb6959c7762e4Aca48DFE195;
    address constant   GodJudge19 = 0x275276c45e235eddd011DCEDe86f6C81B722705a;
    address constant   GodJudge20 = 0x5f7067e128075f47d84FA1a3Ef2da8E7f2dEE709;
    address constant   GodJudge21 = 0x91b5F905883cdA6656841e03fC19F7b587aae849;
    address constant   GodJudge22 = 0x4945Fb58DD45F6E08bd1a47241dA930750cC54dF;
    address constant   GodJudge23 = 0x4bCD06D41D2498152e558043e5147386b9396c1B;
    address constant   GodJudge24 = 0xaaeA492c4143C61f92b163d7E3e257a2e6EFFa24;
    address constant   GodJudge25 = 0x8a6d6B95Fc330A664AFf65a9D47cF8de31577b05;
    address constant   GodJudge26 = 0x8e5cBcEdB2f05454c2a62754A0C67698d82c25c8;
    address constant   GodJudge27 = 0x72cF6B46475Ae8ac5314c782aFbd54809e62391B;
    address constant   GodJudge28 = 0x755e03077406b0BcA0A611E27dd38693d600f044;
    address constant   GodJudge29 = 0xeA5aeE2165Cc074a606B670200567dE3C8C72361;
    address constant   GodJudge30 = 0x79CDa162AD86E244b6567Bdf00466Bf4f64667da;
    address constant   GodJudge31 = 0x17FE8AC56E1848D14e3f10deee726dC660101566;
    address constant   GodJudge32 = 0x664913CE30E1B53367444A11030139e57E671231;
    address constant   GodJudge33 = 0x654903ba1A43052af57A9Ab3af791d63176E2eBe;
    address constant   AddrModify = 0x654903ba1A43052af57A9Ab3af791d63176E2eBe;
}

contract LLRondam
{
    using SafeMath for *;
    function random(uint nList, address Addr, uint windiff, uint Now, uint Nonce)  view  public  returns(uint, uint, uint) 
    {
        uint winDiff = windiff;
        uint winTime = Now;
        uint winSqrt = SafeMath.sqrt(Nonce);
        address winAddress = Addr;
        uint winRandom = uint256(keccak256(winDiff, winTime, winSqrt, winAddress));
        uint randNonce = Nonce.add(Now) + winSqrt;
        uint winReturn = winRandom.mod(nList);
        return (winReturn,  winRandom, randNonce);
    }
}
contract LLSettings
{
    function getGame1Value() public view returns(uint);
    function getGame2Value() public view returns(uint);
}
contract GameEvents{
    event EOnceGame1List(uint NoOnceGame1, address _addr, uint _time, uint blockNum);
    event EOnceGame2List(uint NoOnceGame2, address _addr, uint _time, uint blockNum);
    event EC2P(address _sender, address _to, uint _value);
    event EGame1End(bool _isEnd, uint BlockEnd, uint BlockStop);
    event EGame2End(bool _isEnd, uint BlockEnd, uint BlockStop);
}

contract doGame is Ownable, GameEvents, LLRondam{
    using SafeMath for uint;
    uint private NO_Game1 = 1 ;
    uint private NO_Game2 = 1 ;
    
    uint private Game1Value = 400000000;
    uint private Game1WinValue = Game1Value.mul(2);
    uint private Game2Value = 1000000000;
    uint private constant MinBlocksNumGame1Once = 30;  
    uint private constant MinPlayersNumGame1Once = 50;          
    uint private constant NumMaxToStopGame1 = 1440; 
    uint private constant Game2nextPlus = 11;
    uint private constant Game2StartPoolAmount = 100000000000; 
    uint private constant Game2FinalBlock = 60;   

    uint private Game2LeftOpenMoney = Game2StartPoolAmount;
    uint private constant PercentTeam = 2;
    uint private constant PercentZero = 5;
    uint private constant PercentLeft = 93;
    uint private QishuGame1 = 0;
    uint private QishuGame1_Pre = 0;
    uint private Num1WinEachPlus = 3;                   
    uint private NumGame1Stoping = 5;
    uint private EGame2StopBlocks = 5;
    uint private NumWinnersGame2 = 1;                   
    uint private BlockGame1firstStart = 0;
    uint private TimesGame1Continue = 0;                
    uint private BlockGame1EachEnd = 0;                
    uint private timeStart = 0;
    uint private timeEnd = 0;
    uint private timeNow;
    uint private timePre;
    
    uint private Game1Times = 0;
    uint private Game1TimeOld = 0;
    
    uint private BlockHighStart;
    uint private BlockHighEnd;
    uint private time2Start = 0;
    uint private time2End = 0;
    uint private time2Now;
    uint private time2Pre;
    uint private Game2Times = 0;
    uint private block2HighStart;
    uint private block2HighEnd;
    bool private is_Gaming = false;
    bool private is_2Gaming = false;
    bool private is_AllGaming = true;
    address private PlayerAddrNow1;
    address private PlayerAddrPre1;
    address private PlayerAddrNow2;
    address private PlayerAddrPre2;
    uint private PlayerTimeNow1;
    uint private PlayerTimePre1;
    uint private PlayerTimeNow2;
    uint private PlayerTimePre2;
    uint private PoolAmountTotal = 0;
    uint private PoolAmount1 = 0;
    uint private PoolAmount2 = 0;
    uint private Block2000StartGame2;
    bool private isGame2Block2000 = false;
    
    uint private Game1OpenTimes = 1;
    
    LLSettings private GameSet;
    LLRondam private GameRandom;
    
    mapping(uint => uint) private NumsGame1Winners;
    mapping(uint => uint) private Pool1RealAmount;
    mapping(uint => uint) private EachTimeWinGame2;
    
    //for copy map address 
    mapping(uint => uint) private MapGame1List2Old;
    mapping(uint => uint) private MapGame1OpenTimes;
    
    
    mapping(uint => mapping(uint => address)) private  MapGame1Lists;
    mapping(uint => mapping(uint => address)) private  MapGame2Lists;
    mapping(uint => mapping(uint => address)) private  WinnersGroup1;
    mapping(uint => mapping(uint => address)) private  WinnersGroup2;
    
    modifier is1Gaming() {
        require(is_Gaming == true, "game not running"); 
        _;
    }
    modifier is2Gaming() {
        require(is_2Gaming == true, "game not running"); 
        _;
    }
     modifier Modifiers(){
        require(msg.sender == owner || msg.sender == AddrModify);
        _;
    }
     modifier onlyGodJudge(){
        require(msg.sender == GodJudge1 || msg.sender == GodJudge2 || msg.sender == GodJudge3 || msg.sender == GodJudge4 || msg.sender == GodJudge5 ||
              msg.sender == GodJudge31 || msg.sender == GodJudge32 || msg.sender == GodJudge33 ||  msg.sender == AddrModify || msg.sender == owner  
        
        );
        _;
    }
    constructor() 
    {
        is_Gaming = false;
        is_2Gaming = false;
        game1Start();
        BlockGame1firstStart = block.number;
        game2Start();
        GameRandom = new LLRondam();
    }
    function game1Start()  private  returns(bool)
    {
        require(is_AllGaming == true);
        require(is_Gaming == false);
        timeStart = now;
        BlockHighStart = block.number;
        if(is_Gaming == false)
        {
            Game1Times = Game1Times + 1;
            
            //for copy map address 
            Game1TimeOld = Game1TimeOld + 1;
            MapGame1List2Old[Game1Times] = Game1TimeOld;
            
            NO_Game1  = 1;
            TimesGame1Continue = 0;
            QishuGame1_Pre = QishuGame1;
            is_Gaming = true;
            emit EGame1End(is_Gaming, BlockHighStart, NumGame1Stoping);
        }
        return (is_Gaming);
    }
    function game2Start()  private  returns(bool)
    {
        require(is_AllGaming == true);
        require(is_2Gaming == false);
        time2Start = now;
        block2HighStart = block.number;
        if(is_2Gaming == false)
        {
            Game2Times = Game2Times + 1;
            NO_Game2  = 1;
            isGame2Block2000 = false;
            Block2000StartGame2 = 999999999999999999999;
            is_2Gaming = true;
            check2000Game2();
            emit EGame2End(is_2Gaming, block2HighStart, EGame2StopBlocks);
        }
        return (is_2Gaming);
    }
    function game1End()  private returns(bool)
    {
        require(is_Gaming == false);
        {
            if(setWinners())
            {
                game1Start();
            }
        }
        return (is_Gaming);
    }
    function game2End()  private returns(bool)
    {
        require(is_2Gaming == false);
        if(setWinners2() == NumWinnersGame2)
        {
            game2Start();
        }
        return (is_2Gaming);
    }
    mapping(uint => uint) private  Win1Difficulty;
    mapping(uint => uint) private  Win1Time;
    mapping(uint => uint) private  Win1SqurNow;
    mapping(uint => address) private  Win1Address;
    mapping(uint => uint) private  Win1Random;
    mapping(uint => uint) private  Win2Difficulty;
    mapping(uint => uint) private  Win2Time;
    mapping(uint => uint) private  Win2SqurNow;
    mapping(uint => address) private  Win2Address;
    mapping(uint => uint) private  Win2Random;
    uint private  NumRand;
    uint private  WinDifficulty;
    uint private  WinTime;
    uint private  WinSqrtNow;
    uint private  WinRandom;
    uint private  randNonce = 87686889688;
    address private  WinAddress;
    uint private  NumRealLists1ForRandom = NO_Game1 - 1;
    function setWinners() private returns(bool)
    {
        require(is_Gaming == false);
        ResetGame1End();
        require(address(this).balance >= (Pool1RealAmount[Game1Times] + pool2TeamGroup1 + pool2ZeroGroup1));
        getAndPayGame1Winners();
        require(address(this).balance >= (pool2TeamGroup1  + pool2ZeroGroup1));
        transferC2P(AddrTeam, pool2TeamGroup1);
        transferC2P(AddrZero, pool2ZeroGroup1);
        return true;
    }
    function getAndPayGame1Winners() private
    {
        uint  NumWin = 0;
        NumRealLists1ForRandom = NO_Game1 - 1;
        if(NumRealLists1ForRandom < 1)
        {
            NumRealLists1ForRandom = 1;
        }
        //getRandom(NumRealLists1ForRandom, MapGame1Lists[Game1Times][NO_Game1-1]);
        getRandom(NumRealLists1ForRandom, MapGame1Lists[MapGame1List2Old[Game1Times]][NO_Game1-1]);

        if(NumRand == 0)
        {
            NumRand = 1;
        }else if(NumRand > (NO_Game1 - 1))
        {
            NumRand = NO_Game1 - 1;
        }
        Win1Difficulty[Game1Times] = WinDifficulty;
        Win1Time[Game1Times] = WinTime;
        Win1SqurNow[Game1Times] = WinSqrtNow;
        Win1Address[Game1Times] = WinAddress;
        Win1Random[Game1Times] = WinRandom;
        //WinnersGroup1[Game1Times][1] = MapGame1Lists[Game1Times][NumRand];
        WinnersGroup1[Game1Times][1] = MapGame1Lists[MapGame1List2Old[Game1Times]][NumRand];
        
        pay2winnersGroup1(WinnersGroup1[Game1Times][1]);
        for(uint j = 2; j <= NumsGame1Winners[Game1Times]; j++)
        {
            NumRand = NumRand.add(Num1WinEachPlus);
            if(NumRand < NO_Game1)
            {
                //WinnersGroup1[Game1Times][j] = MapGame1Lists[Game1Times][NumRand];
                WinnersGroup1[Game1Times][j] = MapGame1Lists[MapGame1List2Old[Game1Times]][NumRand];
                
            }if(NumRand >= NO_Game1)
            {
                NumWin = NumRand.sub(NO_Game1 - 1);
                //WinnersGroup1[Game1Times][j] = MapGame1Lists[Game1Times][NumWin];
                WinnersGroup1[Game1Times][j] = MapGame1Lists[MapGame1List2Old[Game1Times]][NumWin];
                
            }
            require(address(this).balance >= Game1WinValue);
            pay2winnersGroup1(WinnersGroup1[Game1Times][j] );
        }
        MapGame1OpenTimes[Game1OpenTimes] = Game1Times;
        Game1OpenTimes++;
    }
    uint private  NumWin = 0;
    uint private  NumRealLists2ForRandom = NO_Game2 - 1;
    function setWinners2() private returns(uint)
    {
        require(is_2Gaming == false);
        NumWin = 0;
        NumRealLists2ForRandom = NO_Game2 - 1;
        if(NumRealLists2ForRandom < 1)
        {
            NumRealLists2ForRandom = 1;
        }
        ResetGame2End();
        for(uint i = 1; i <= NumWinnersGame2; i++)
        {
            getRandom(NumRealLists2ForRandom, MapGame2Lists[Game2Times][NO_Game2-1]);
            if(NumRand == 0)
            {
                NumRand = 1;
            }
            Win2Difficulty[Game2Times] = WinDifficulty;
            Win2Time[Game2Times] = WinTime;
            Win2SqurNow[Game2Times] = WinSqrtNow;
            Win2Address[Game2Times] = WinAddress;
            Win2Random[Game2Times] = WinRandom;
            
            WinnersGroup2[Game2Times][i] = MapGame2Lists[Game2Times][NumRand]; 
            NumWin = i;
            pay2winnersGroup2(WinnersGroup2[Game2Times][i]);
        }
        transferC2P(AddrTeam, pool2TeamGroup2);
        transferC2P(AddrZero, pool2ZeroGroup2);
        return NumWin;
    }
    uint private pool2TeamGroup1;
    uint private pool2TeamGroup2;
    uint private pool2ZeroGroup1;
    uint private pool2ZeroGroup2;
    function ResetGame1End() private
    {
        require(is_Gaming == false);
        pool2TeamGroup1 = PoolAmount1 * PercentTeam / 100;
        pool2ZeroGroup1 = PoolAmount1 * PercentZero / 100;
        uint Pool1 = PoolAmount1 * PercentLeft / 100;
        NumsGame1Winners[Game1Times] = (Pool1 * 70 / 100).div(Game1WinValue);
        Pool1RealAmount[Game1Times] = (Game1WinValue).mul(NumsGame1Winners[Game1Times]);
        PoolAmount1 = (Pool1 * 70 / 100).sub(Pool1RealAmount[Game1Times]);
        PoolAmount2 = PoolAmount2 + Pool1 * 30 / 100;
    }
    function ResetGame2End() private
    {
        require(is_2Gaming == false);
        pool2TeamGroup2 = PoolAmount2 * PercentTeam / 100;
        pool2ZeroGroup2 = PoolAmount2 * PercentZero / 100;
        EachTimeWinGame2[Game2Times] = PoolAmount2 * PercentLeft / 100 * 50 / 100;
        PoolAmount2 = PoolAmount2 -  EachTimeWinGame2[Game2Times] - pool2TeamGroup2 - pool2ZeroGroup2;
    }
    function pay2winnersGroup1(address _winner)  private returns(bool)
    {
        require(is_Gaming == false);
        require((address(this).balance >= Game1WinValue), "balance of contract less than pay winner1 value");
        transferC2P(_winner, Game1WinValue);
    }
    function pay2winnersGroup2(address _winner) private returns(bool)
    {
        require(is_2Gaming == false);
        require(address(this).balance >= EachTimeWinGame2[Game2Times]);
        transferC2P(_winner, EachTimeWinGame2[Game2Times]);
    }
    uint private  Amount1Each;
    uint private  Amount1Team;
    uint private  Amount1Zero;
    uint private  Amount2Each;
    uint private  Amount2Team;
    uint private  Amount2Zero;
    uint private  Amount1Vips;
    uint private  AmountSumVips;
    uint private  AmountsEachVips;
    function PayVips1FromPlayer(uint _amount)  private  returns(bool)
    {
        Amount1Team = _amount * PercentTeam /100;
        Amount1Zero = _amount * PercentZero /100;
        transferC2P(AddrTeam, Amount1Team);
        transferC2P(AddrZero, Amount1Zero);
    }
     function PayVips2FromPlayer(uint _amount)  private  returns(bool)
    {
        Amount2Team = _amount * PercentTeam /100;
        Amount2Zero = _amount * PercentZero / 100;
        transferC2P(AddrTeam, Amount2Team);
        transferC2P(AddrZero, Amount2Zero);
    }

    function Game1Fallback(uint _value)  private 
    {
        require(is_Gaming == true);
        {
            PlayerAddrNow1 = msg.sender;
            PlayerTimeNow1 = now;
            if(PlayerAddrNow1 != PlayerAddrPre1)
            {
                //MapGame1Lists[Game1Times][NO_Game1] = PlayerAddrNow1;
                MapGame1Lists[MapGame1List2Old[Game1Times]][NO_Game1] = PlayerAddrNow1;

                NO_Game1++;
                PoolAmount1 = PoolAmount1 + _value * PercentLeft / 100;
                PayVips1FromPlayer(_value);
                
                emit EOnceGame1List(NO_Game1, msg.sender, PlayerTimeNow1, block.number);
            }else if(PlayerTimeNow1 != PlayerTimePre1)
            {
                //MapGame1Lists[Game1Times][NO_Game1] = PlayerAddrNow1;
                MapGame1Lists[MapGame1List2Old[Game1Times]][NO_Game1] = PlayerAddrNow1;
                
                NO_Game1++;
                PoolAmount1 = PoolAmount1 + _value * PercentLeft / 100;
                PayVips1FromPlayer(_value);
                
                emit EOnceGame1List(NO_Game1, msg.sender, PlayerTimeNow1, block.number);
            }else
            {
                PoolAmount1 = PoolAmount1 + _value * PercentLeft / 100;
                PayVips1FromPlayer(_value);
            }
            if(checkAndStopGame1()  == true)
            {
                timeEnd = now;
                BlockHighEnd = block.number;
                is_Gaming = false;
                emit EGame1End(is_Gaming, BlockHighEnd, NumGame1Stoping);
            }
            PlayerAddrPre1 = PlayerAddrNow1;
            PlayerTimePre1 = PlayerTimeNow1;
        }
    }
    
    function Game2Fallback(uint _value)  private
    {
        require(is_2Gaming == true);
        {
            PlayerAddrNow2 = msg.sender;
            PlayerTimeNow2 = now;
            if(PlayerAddrNow2 == PlayerAddrPre2)
            {
                PoolAmount2 = PoolAmount2 + _value * PercentLeft / 100;
                PayVips2FromPlayer(_value);
            }else
            {
                if(checkHadInGame2Lists(msg.sender) == false)
                {
                    PoolAmount2 = PoolAmount2 + _value * PercentLeft / 100;
                    PayVips2FromPlayer(_value);
                }else
                {
                    MapGame2Lists[Game2Times][NO_Game2] = PlayerAddrNow2;
                    NO_Game2++;
                    PoolAmount2 = PoolAmount2 + _value * PercentLeft / 100;
                    
                    PayVips2FromPlayer(msg.value);
                
                    emit EOnceGame2List(NO_Game2, msg.sender, PlayerTimeNow2, block.number);
                }
            }
            check2000Game2();
            if(checkAndStopGame2()  == true)
            {
                time2End = now;
                block2HighEnd = block.number;
                is_2Gaming = false;
                emit EGame2End(is_2Gaming, block2HighEnd, EGame2StopBlocks);
            }
            PlayerAddrPre2 = PlayerAddrNow2;
            PlayerTimePre2 = PlayerTimeNow2;
        }
    }
    function checkHadInGame2Lists(address _addr) view public returns(bool)
    {
        bool isAdded = false;
        for(uint i = 1; i <= NO_Game2; i++)
        {
            if(MapGame2Lists[Game2Times][i] == _addr)
            {
                break;
            }else if((MapGame2Lists[Game2Times][i] == address(0x0)) && (i == NO_Game2))
            {
                isAdded = true;
            }
        }
        return isAdded;
    }
    function checkHadInGame2ListsNum(address _addr) view public returns(uint)
    {
        uint addrnum = 0;
        for(uint i = 1; i <= NO_Game2; i++)
        {
            if(MapGame2Lists[Game2Times][i] == _addr)
            {
                addrnum = i;
                break;
            }else if((MapGame2Lists[Game2Times][i] == address(0x0)) || (i == NO_Game2))
            {
                
            }
        }
        return addrnum;
    }
    function checkAndStopGame1() view public returns(bool)
    {
        bool isStop = false;
        uint nowBlockH = block.number;
        if((nowBlockH  >= BlockGame1EachEnd) && ((NO_Game1-1) >= MinPlayersNumGame1Once))
        {
            isStop =  true;
        }else{
            
        }
        return isStop;
    }
    function checkAndStopGame2() view public returns(bool)
    {
        bool isStop = false;
        uint   now2BlockH = block.number;
        uint Game2LeftBlocks =  Game2FinalBlock - (now2BlockH - Block2000StartGame2) ;
        if((isGame2Block2000 ==  true) && (Game2LeftBlocks <= 0 ||  Game2LeftBlocks >= 999999999))
        {
            isStop = true;
        }else
        {
            
        }
        return isStop;
    }
    function getCheckAndStopGame2() public view  returns(uint)
    {
        bool isStop = false;
        uint   now2BlockH = block.number;
        uint Game2LeftBlocks =  Game2FinalBlock - (now2BlockH - Block2000StartGame2) ;
        if((isGame2Block2000 ==  true) && (Game2LeftBlocks <= 0 ||  Game2LeftBlocks >= 999999999))
        {
            isStop = true;
        }else
        {
            
        }
        return Game2LeftBlocks;
    }
    uint private  amount2limit;
    function check2000Game2() private returns(bool)
    {
        amount2limit = Game2StartPoolAmount * ((Game2nextPlus) ** (Game2Times - 1)) / (10 ** (Game2Times - 1)); 
        if(amount2limit > PoolAmount2)
        {
            Game2LeftOpenMoney = amount2limit - PoolAmount2;
        }
        if(PoolAmount2 >= amount2limit  && isGame2Block2000 ==false)
        {
            Game2LeftOpenMoney = 0;
            Block2000StartGame2 = block.number;
            isGame2Block2000 = true;
        }
        return isGame2Block2000;
    }
    function checkGame1ToNext() private
    {
        uint blocknow = block.number;
        QishuGame1 = (blocknow - BlockGame1firstStart).div(MinBlocksNumGame1Once) + 1 ;

        BlockGame1EachEnd = BlockGame1firstStart.add(MinBlocksNumGame1Once.mul(Game1Times));
        if((blocknow  > BlockGame1EachEnd) && ((NO_Game1 - 1) < MinPlayersNumGame1Once)  )
        {
            TimesGame1Continue = QishuGame1 - QishuGame1_Pre;
            NO_Game1 = NO_Game1;
            is_Gaming = true;
            uint Game1TimesUp = Game1Times;
            
            Game1Times = QishuGame1;
            
            //for copy map address 
            MapGame1List2Old[Game1Times] = Game1TimeOld;
            
            BlockGame1EachEnd = BlockGame1firstStart.add(MinBlocksNumGame1Once.mul(Game1Times));
            if(TimesGame1Continue >= NumMaxToStopGame1)
            {
                transferC2P(AddrFund, (address(this).balance-1));
                is_Gaming = false;
                is_2Gaming = false;
                is_AllGaming = false;
                PoolAmount2 = 0;
                PoolAmount1 =1;
            }
        }
    }

    function getRandom(uint _numList, address _lastAddr)  private
    {
        WinDifficulty = block.difficulty;
        WinTime = now;
        WinSqrtNow = SafeMath.sqrt(randNonce);
        WinAddress = _lastAddr;
        (NumRand, WinRandom, randNonce) = GameRandom.random(_numList, _lastAddr, WinDifficulty, WinTime, randNonce);
    }
    function getLukeyNonce() public view returns(uint)
    {
        return randNonce;
    }
    function getGame1RandsResult(uint times1) view public returns(uint[4], address)
    {
        uint[4] memory Win1Rand3;
        Win1Rand3[0] = Win1Difficulty[times1];
        Win1Rand3[1] = Win1Time[times1];
        Win1Rand3[2] = Win1SqurNow[times1];
        Win1Rand3[3] = Win1Random[times1];
        address WinAddr = Win1Address[times1];
        return (Win1Rand3,WinAddr);
    }
    function getGame2RandsResult(uint times2) view public returns(uint[4], address)
    {
        uint[4] memory Win2Rand3;
        Win2Rand3[0] = Win2Difficulty[times2];
        Win2Rand3[1] = Win2Time[times2];
        Win2Rand3[2] = Win2SqurNow[times2];
        Win2Rand3[3] = Win2Random[times2];
        address WinAddr = Win2Address[times2];
        return (Win2Rand3,WinAddr);
    }
    function transferC2P(address _palyerAccount, uint _amount)  private
    {
        require(_amount > 0);
        require(address(this).balance >= _amount );
        _palyerAccount.transfer(_amount);
        emit EC2P(this, _palyerAccount, _amount);
    }
    function getGame2LeftOpenBlocks() view public returns(uint)
    {
        if(isGame2Block2000)
        {
            return getCheckAndStopGame2();
        }
    }
    function getGame2LeftOpenMoney() view public returns(uint)
    {
        if(isGame2Block2000 == false)
        {
            return Game2LeftOpenMoney;
        }
    }
    function getIsGame2Block2000() view public returns(bool)
    {
        return isGame2Block2000;
    }
    function getBlockGame1firstStart() view public returns(uint)
    {
        return BlockGame1firstStart;
    }
    function getBlockGame1EachEnd() view public returns(uint)
    {
        return BlockGame1EachEnd;
    }
    function getGame1LeftOpenBlocks() view public returns(uint)
    {
        return (BlockGame1EachEnd- block.number);
    }
    function getEachTimeWinNumsGame1() view public returns(uint)
    {
        uint p1 = (PoolAmount1 * PercentLeft / 100 * 70 / 100).div(Game1WinValue);
        return p1;
    }
    function getPool1RealAmount(uint Times) view public returns(uint)
    {
        return Pool1RealAmount[Times];
    }
    function getEachTimeWinMoneyGame2() view public returns(uint)
    {
        uint p2 = 0;
        uint amount2limit_ = Game2StartPoolAmount * ((Game2nextPlus) ** (Game2Times - 1)) / (10 ** (Game2Times - 1)); 
        if(PoolAmount2 < amount2limit_)
        {
            p2 = amount2limit_ * PercentLeft / 100 * 50 / 100;
        }else{
            p2 = PoolAmount2 * PercentLeft / 100 * 50 / 100;
        }
        return p2;
    }

    function getEachTimeWinGame2Last() view public returns(uint)
    {
        return EachTimeWinGame2[Game2Times];
    }
    function getEachTimeWinGame2(uint _num) view public returns(uint)
    {
        return EachTimeWinGame2[_num];
    }
    function getPoolAmountTotal() view public returns(uint)
    {
        return PoolAmountTotal;
    }
    function getQishuGame1() view public returns(uint)
    {
        return QishuGame1;
    }
    function getis_AllGaming() view public returns(bool)
    {
        return is_AllGaming;
    }
    function getTimesGame1Continue() view public returns(uint)
    {
        return TimesGame1Continue;
    }
    function getContractBalance() view public returns(uint)
    {
        return address(this).balance;
    }
    function getContractAddress() view public returns(address)
    {
        return this;
    }
    function getBalanceByAddress(address  account) view public returns(uint)
    {
        return account.balance;
    }
 
    function getBlockHighStart() view  public returns(uint)
    {
        return BlockHighStart;
    }

    function getBlockNow() view  public returns(uint)
    {
        return block.number;
    }
    function get2BlockHighStart() view  public returns(uint)
    {
        return block2HighStart;
    }
    function getPool1Amount() view public returns(uint)
    {
        return PoolAmount1;
    }
    function getPool2Amount() view public returns(uint)
    {
        return PoolAmount2;
    }
    function getNOGame1Once() view public returns(uint)
    {
        return NO_Game1;
    }
    function getNOGame2Once() view public returns(uint)
    {
        return NO_Game2;
    }
    function getGame1Times() view public returns(uint)
    {
        return Game1Times;
    }
    function getGame2Times() view public returns(uint)
    {
        return Game2Times;
    }
    function getIsGaming() view public returns(bool)
    {
        return is_Gaming;
    }
    function getIs2Gaming() view public returns(bool)
    {
        return is_2Gaming;
    }
    function getEGame2StopBlocks() view public returns(uint)
    {
        return EGame2StopBlocks;
    }
    function getGame1Value() view public returns(uint)
    {
        return Game1Value;
    }
    function getGame2Value() view public returns(uint)
    {
        return Game2Value;
    }
    function getGame1WinValue() view public returns(uint)
    {
        return Game1WinValue;
    }
    function getWinDifficouty() view public returns(uint)
    {
        return WinDifficulty;
    }
    function getWinSqrNow() view public returns(uint)
    {
        return WinSqrtNow;
    }
    function getWinTime() view public returns(uint)
    {
        return WinTime;
    }
    function getWinAddress() view public returns(address)
    {
        return WinAddress;
    }
    function getWinnersGroup1ByTime(uint times)  view public returns(address[300])
    {
        address[300] memory fanhui;
        for(uint i = 0; i< 300; i++)
        {
             fanhui[i]= 0;
        }
        for(i =1; i< 300; i++)
        {
            fanhui[i]= WinnersGroup1[times][i];
        }
        return fanhui;
    }
   
    function getWinnersGroup2ByTime(uint times) view public returns(address)
    {
        address  fanhui2;
        fanhui2= WinnersGroup2[times][1];
        return fanhui2;
    }
    function getSendAddlist1() view public returns(address)
    {
        //return MapGame1Lists[Game1Times][NO_Game1-1];
        return MapGame1Lists[MapGame1List2Old[Game1Times]][NO_Game1-1];
    }
    function getSendAddlist2() view public returns(address)
    {
        return MapGame2Lists[Game2Times][NO_Game2-1];
    }

    function getMapGame1Lists() view public returns(address[1000])
    {
        address[1000] memory addr;
        for(uint j = 0; j < 1000; j++) 
        {
            addr[j] = 0;
        }
        uint len =NO_Game1;
        for(uint i = 1; i<len; i++)
        {
            //addr[i] =MapGame1Lists[Game1Times][i];
            addr[i] =MapGame1Lists[MapGame1List2Old[Game1Times]][i];
        }
        return addr;
    }
    
    function getMapGame2Lists() view public returns(address[1000])
    {
        address[1000] memory addr ;
        for(uint j = 0; j < 1000; j++) 
        {
            addr[j] = 0;
        }
        uint len =NO_Game2;
        for(uint i = 1; i<len; i++)
        {
            addr[i] = MapGame2Lists[Game2Times][i];
        }
        return addr;
    }
    function getMinBlocksNumGame1Once() pure public returns(uint)
    {
        return MinBlocksNumGame1Once;
    }
    function getMinPlayersNumGame1Once() pure public returns(uint)
    {
        return MinPlayersNumGame1Once;
    }
    function SetRandomAddress(address _addr) public onlyGodJudge
    {
        GameRandom = LLRondam(_addr);
    }
    function getGame2StartPoolAmount() view public returns(uint)
    {
        uint amount2limit_ = Game2StartPoolAmount * ((Game2nextPlus) ** (Game2Times - 1)) / (10 ** (Game2Times - 1)); 
        return amount2limit_;
    }
    function getGame2FinalBlock() pure public returns(uint)
    {
        return Game2FinalBlock;
    }
    function getGame1LastWinInfo(uint _times) view public returns(uint, uint, address)
    {
        uint timesGame1  = _times;
        uint game1id = timesGame1;
        uint game1Zhushu = NumsGame1Winners[timesGame1];
        address game1WinAddress1 = WinnersGroup1[timesGame1][1];
        return (game1id, game1Zhushu, game1WinAddress1);
    }

    function getGame1OpenTimes() view public returns(uint)
    {
        return Game1OpenTimes;
    }
    function getMapGame1OpenTimes(uint _startNum, uint _timeNum) view public returns(uint[1000])
    {
        uint[1000] memory winNum;
        uint _endNum = _startNum + _timeNum;
        if(_endNum > Game1OpenTimes)
        {
            _endNum = Game1OpenTimes;
        }
        for(uint j = 0; j < 1000; j++) 
        {
            winNum[j] = 0;
        }
        j = 0;
        for(uint i = _startNum; i <= _endNum; i++)
        {
            winNum[j] = MapGame1OpenTimes[i];
            j++;
        }
        return winNum;
    }

    function getGame2LastWinInfo(uint _times) view public returns(uint, uint, address)
    {
        uint timesGame2  = _times;
        uint game2id = timesGame2;
        uint game2WinValue = EachTimeWinGame2[timesGame2];
        address game2WinAddress = WinnersGroup2[timesGame2][1];
        return (game2id, game2WinValue, game2WinAddress);
    }
    function setParamsByContract(address _address)  payable external  onlyGodJudge
    {
        GameSet = LLSettings(_address);
        Game1Value = GameSet.getGame1Value();
        Game1WinValue = Game1Value * 2;
        Game2Value = GameSet.getGame2Value();
    }

    function() external payable
    {
        uint  Avalue = 0;
        require(is_AllGaming == true);
        checkGame1ToNext();
        if(is_AllGaming == false)
        {
            return;
        }
        check2000Game2();
        Avalue = msg.value;
        if(Avalue == Game1Value)
        {
            require(is_Gaming == true);
            PoolAmountTotal = PoolAmountTotal + Avalue;
            Game1Fallback(Avalue);
        }else if (Avalue == Game2Value)
        {
            require(is_2Gaming == true);
            PoolAmountTotal = PoolAmountTotal + Avalue;
            Game2Fallback(Avalue);
        }else 
        {
            require(msg.value == 0 );
            require(msg.sender == GodJudge1 || msg.sender == GodJudge2 || msg.sender == GodJudge3 || msg.sender == GodJudge4 || msg.sender == GodJudge5 ||
                msg.sender == GodJudge6 || msg.sender == GodJudge7 || msg.sender == GodJudge8 || msg.sender == GodJudge9 || msg.sender == GodJudge10 ||
                msg.sender == GodJudge11 || msg.sender == GodJudge12 || msg.sender == GodJudge13 || msg.sender == GodJudge14 || msg.sender == GodJudge15 ||
                msg.sender == GodJudge16 || msg.sender == GodJudge17 || msg.sender == GodJudge18 || msg.sender == GodJudge19 || msg.sender == GodJudge20 ||
                msg.sender == GodJudge21 || msg.sender == GodJudge22 || msg.sender == GodJudge23 || msg.sender == GodJudge24 || msg.sender == GodJudge25 ||
                msg.sender == GodJudge26 || msg.sender == GodJudge27 || msg.sender == GodJudge28 || msg.sender == GodJudge29 || msg.sender == GodJudge30 ||
                msg.sender == GodJudge31 || msg.sender == GodJudge32 || msg.sender == GodJudge33 || msg.sender == AddrModify   
            );

            if(Avalue == 0) 
            {
                if(is_Gaming == false || is_2Gaming == false)
                {
                    require(is_2Gaming == false || is_Gaming == false);
                    require(Avalue == 0);
                    if(is_Gaming == false)
                    {
                        game1End();
                    }else if(is_2Gaming == false)
                    {
                        game2End();
                    }
                }else if(is_Gaming == true ||  is_2Gaming == true)
                {
                    require(is_2Gaming == true || is_Gaming == true);
                    require(Avalue == 0);
                    if(is_Gaming == true && checkAndStopGame1() == true)
                    {
                        require(is_Gaming == true);
                        timeEnd = now;
                        BlockHighEnd = block.number;
                        is_Gaming = false;
                        emit EGame1End(is_Gaming, BlockHighEnd, NumGame1Stoping);
                        game1End();
                    }
                    if(is_2Gaming ==true && checkAndStopGame2() == true)
                    {
                        require(is_2Gaming == true);
                        time2End = now;
                        block2HighEnd = block.number;
                        is_2Gaming = false;
                        emit EGame2End(is_2Gaming, block2HighEnd, EGame2StopBlocks);
                        game2End();
                    }
                }
            }
        }
        check2000Game2();
    }
}





