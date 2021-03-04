---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: 4346ec557d149d2555b136cfef15b86770b89dbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916030"
---
# <span data-ttu-id="696d9-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="696d9-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="696d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="696d9-102">SYNOPSIS</span></span>
<span data-ttu-id="696d9-103">獲得服務標記資訊資源的清單。</span><span class="sxs-lookup"><span data-stu-id="696d9-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="696d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="696d9-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696d9-105">描述</span><span class="sxs-lookup"><span data-stu-id="696d9-105">DESCRIPTION</span></span>
<span data-ttu-id="696d9-106">**Get-AzNetworkServiceTag** Cmdlet 會取得服務標記資訊資源的清單。</span><span class="sxs-lookup"><span data-stu-id="696d9-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="696d9-107">請注意，您指定的 Azure 區域資訊將做為版本 (的參照，而不是根據位置或位置做為) 。</span><span class="sxs-lookup"><span data-stu-id="696d9-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="696d9-108">例如，即使您指定，您也會在所有地區取得包含首碼詳細資料的服務標記清單，但僅限於您訂閱所屬的雲端 (例如公用、美國政府、中國或 `-Location eastus2` 德國) 。</span><span class="sxs-lookup"><span data-stu-id="696d9-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="696d9-109">例子</span><span class="sxs-lookup"><span data-stu-id="696d9-109">EXAMPLES</span></span>

### <span data-ttu-id="696d9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="696d9-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="696d9-111">該命令會獲得服務標記資訊資源的清單，並儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="696d9-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="696d9-112">範例 2：取得 AzureSQL 的所有位址首碼</span><span class="sxs-lookup"><span data-stu-id="696d9-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="696d9-113">第一個命令會獲得服務標記資訊資源的清單，並儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="696d9-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="696d9-114">第二個命令會篩選清單以選取 Sql 的資訊資源。</span><span class="sxs-lookup"><span data-stu-id="696d9-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="696d9-115">範例 3：取得 West US 2 的 Storage 的服務標記資訊資源</span><span class="sxs-lookup"><span data-stu-id="696d9-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="696d9-116">第一個命令會獲得服務標記資訊資源的清單，並儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="696d9-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="696d9-117">下列命令顯示各種篩選清單的方式，以選取美國西部 2 儲存空間的服務標記資訊。</span><span class="sxs-lookup"><span data-stu-id="696d9-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="696d9-118">範例 4：取得所有全域服務標記資訊資源</span><span class="sxs-lookup"><span data-stu-id="696d9-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="696d9-119">第一個命令會獲得服務標記資訊資源的清單，並儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="696d9-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="696d9-120">第二個命令會篩選清單，只選取沒有設定區域的清單。</span><span class="sxs-lookup"><span data-stu-id="696d9-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="696d9-121">參數</span><span class="sxs-lookup"><span data-stu-id="696d9-121">PARAMETERS</span></span>

### <span data-ttu-id="696d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696d9-122">-DefaultProfile</span></span>
<span data-ttu-id="696d9-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="696d9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696d9-124">-位置</span><span class="sxs-lookup"><span data-stu-id="696d9-124">-Location</span></span>
<span data-ttu-id="696d9-125">將用來做為版本 (參照的位置，不會根據位置做為篩選，而是在所有地區取得包含首碼詳細資料的服務標記清單，但僅限於您的訂閱所屬的雲端) 。</span><span class="sxs-lookup"><span data-stu-id="696d9-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696d9-126">CommonParameters</span></span>
<span data-ttu-id="696d9-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="696d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696d9-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="696d9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696d9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="696d9-129">INPUTS</span></span>

### <span data-ttu-id="696d9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="696d9-130">System.String</span></span>

## <span data-ttu-id="696d9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="696d9-131">OUTPUTS</span></span>

### <span data-ttu-id="696d9-132">Microsoft.Azure.Commands.Network.models.PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="696d9-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="696d9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="696d9-133">NOTES</span></span>

## <span data-ttu-id="696d9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="696d9-134">RELATED LINKS</span></span>
