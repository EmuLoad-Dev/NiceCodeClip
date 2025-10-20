// ex: 251020
int get_date_YYMMdd() {
    time_t t = time(NULL);
    struct tm *tm_info = localtime(&t);
    
    int year = tm_info->tm_year % 100;
    int month = tm_info->tm_mon + 1;
    int day = tm_info->tm_mday;
    
    return year * 10000 + month * 100 + day;
}
