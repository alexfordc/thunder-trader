Includes=-I../../CommonFiles \
 -I../../CommonFiles/CompreTradeSystemHeaders \
 -I../../CommonFiles/CTPForLinux32 \
 -I../../QFCompreTradeSystem/AtmMarketDataPlugins \
 -I../../QFCompreTradeSystem/AtmTradePlugins \
 -I../../CommonFiles/Tick\
 -I/root/boost_1_58_0

Libs=-ldl -lboost_system -lboost_filesystem -lpthread -lboost_thread -lboost_date_time -lboost_serialization -lboost_log_setup -lboost_log

Configs=-g -std=c++0x -fexceptions -Wall -Wl,-Bsymbolic -DBOOST_SPIRIT_THREADSAFE -DBOOST_ALL_DYN_LINK

TradeCheckStrategy.so:TradeCheckStrategy.cpp
	g++ -fPIC -shared -L . $(Includes) $(Libs) $(Configs) TradeCheckStrategy.cpp -o TradeCheckStrategy.so

.PHONY : clean
clean:
	rm TradeCheckStrategy.so
