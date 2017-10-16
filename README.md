# l2DN
http://www.c-sharpcorner.com/article/consuming-asp-net-web-api-rest-service-in-asp-net-mvc-using-http-client/
https://www.codeproject.com/Articles/826359/Consuming-ASP-NET-WEB-API-using-ASP-NET-MVC-and-Re
https://www.w3schools.com/howto/howto_js_filter_table.asp

http://www.codedigest.com/posts/10/creating-grid-table-with-sorting-filtering-and-paging-in-aspnet-mvc

http://www.c-sharpcorner.com/article/crud-Asp-Net-web-api-with-entity-framework-in-Asp-Net-mvc/

http://www.dotnetcurry.com/aspnet/1192/aspnet-web-api-async-calls-mvc-wpf

https://stackoverflow.com/questions/26319719/how-to-show-details-view-of-selected-car

https://my.visualstudio.com/?auth_redirect=true

https://startbootstrap.com/template-categories/all/



#include <iostream>
#include <algorithm>
#include <vector>
#include <time.h>

//using namespace std;

int main()
{
    std::vector<int> intVec;

    srand (time(NULL));
    int _number = rand() % 20 + 1;

    for (std::vector<int>::size_type i = 0; i != _number; ++i)
        intVec.push_back (rand() % 100 + 1);

    sort(intVec.begin(), intVec.end());

    std::cout << "intVec stores " << int(intVec.size()) << " numbers.\n";
    for (std::vector<int>::size_type i = 0; i != intVec.size(); ++i)
        std::cout << "intVec[" << i + 1 << "]=" << intVec[i] << " " << std::endl;


    return 0;
}



#include <iostream>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <algorithm>

int main()
{

    int vector[20], _number;

    srand (time(NULL));
    _number = rand() % 20 + 1;

    for (int i = 0; i < _number; ++i)
        vector[i] = rand() % 100 + 1;

    std::cout << "vector stores " << _number << "numbers" << "\n";

    std::sort(vector, vector + _number);
    for (int i = 0; i < _number; ++i)
       std::cout << "vector[" << i + 1 << "]=" << vector[i] << " " << std::endl;

    return 0;
}


