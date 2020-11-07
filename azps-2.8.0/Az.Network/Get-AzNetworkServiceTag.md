---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: cbf01f50c72eef4d016754b063d0d10700553e3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790078"
---
# <span data-ttu-id="09715-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="09715-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="09715-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09715-102">SYNOPSIS</span></span>
<span data-ttu-id="09715-103">取得服務標記資訊資源的清單。</span><span class="sxs-lookup"><span data-stu-id="09715-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="09715-104">句法</span><span class="sxs-lookup"><span data-stu-id="09715-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09715-105">說明</span><span class="sxs-lookup"><span data-stu-id="09715-105">DESCRIPTION</span></span>
<span data-ttu-id="09715-106">**AzNetworkServiceTag** Cmdlet 會取得服務標記資訊資源的清單。</span><span class="sxs-lookup"><span data-stu-id="09715-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="09715-107">請注意，您指定的 Azure 區域資訊將用來做為版本 (的參照，而不是根據位置) 的篩選。</span><span class="sxs-lookup"><span data-stu-id="09715-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="09715-108">例如，即使您指定的是在 `-Location eastus2` 所有地區都要有首碼詳細資料的服務標記清單，但僅限您訂閱所屬的雲端 (（例如，上市公司、美國政府、中國或德國）) 。</span><span class="sxs-lookup"><span data-stu-id="09715-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="09715-109">示例</span><span class="sxs-lookup"><span data-stu-id="09715-109">EXAMPLES</span></span>

### <span data-ttu-id="09715-110">範例1</span><span class="sxs-lookup"><span data-stu-id="09715-110">Example 1</span></span>
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

<span data-ttu-id="09715-111">命令會取得服務標記資訊資源的清單，並將它儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="09715-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="09715-112">範例2：取得 AzureSQL 的所有位址首碼</span><span class="sxs-lookup"><span data-stu-id="09715-112">Example 2: Get all address prefixes for AzureSQL</span></span>
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

<span data-ttu-id="09715-113">第一個命令會取得服務標記資訊資源的清單，並將它儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="09715-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="09715-114">第二個命令會篩選清單以選取 Sql 的資訊資源。</span><span class="sxs-lookup"><span data-stu-id="09715-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="09715-115">範例3：取得美國西部的儲存服務標籤資訊資源</span><span class="sxs-lookup"><span data-stu-id="09715-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
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

<span data-ttu-id="09715-116">第一個命令會取得服務標記資訊資源的清單，並將它儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="09715-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="09715-117">下列命令會顯示篩選清單以選取 [西部美國] 中的儲存服務標記資訊的各種方式。</span><span class="sxs-lookup"><span data-stu-id="09715-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="09715-118">範例4：取得所有全域服務標記資訊資源</span><span class="sxs-lookup"><span data-stu-id="09715-118">Example 4: Get all global service tag information resources</span></span>
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

<span data-ttu-id="09715-119">第一個命令會取得服務標記資訊資源的清單，並將它儲存在變數中 `serviceTags` 。</span><span class="sxs-lookup"><span data-stu-id="09715-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="09715-120">第二個命令會篩選清單，以便只選取那些沒有設定區域的人。</span><span class="sxs-lookup"><span data-stu-id="09715-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="09715-121">參數</span><span class="sxs-lookup"><span data-stu-id="09715-121">PARAMETERS</span></span>

### <span data-ttu-id="09715-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09715-122">-DefaultProfile</span></span>
<span data-ttu-id="09715-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09715-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09715-124">-位置</span><span class="sxs-lookup"><span data-stu-id="09715-124">-Location</span></span>
<span data-ttu-id="09715-125">您將會在所有區域中，將會用來做為參考 (的位置，而不是根據位置來篩選，您將會收到一份服務標記，其中包含所有地區的首碼詳細資料，但僅限您訂閱所屬的雲端) 。</span><span class="sxs-lookup"><span data-stu-id="09715-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

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

### <span data-ttu-id="09715-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09715-126">CommonParameters</span></span>
<span data-ttu-id="09715-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09715-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09715-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09715-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09715-129">輸入</span><span class="sxs-lookup"><span data-stu-id="09715-129">INPUTS</span></span>

### <span data-ttu-id="09715-130">System.object</span><span class="sxs-lookup"><span data-stu-id="09715-130">System.String</span></span>

## <span data-ttu-id="09715-131">輸出</span><span class="sxs-lookup"><span data-stu-id="09715-131">OUTPUTS</span></span>

### <span data-ttu-id="09715-132">PSNetworkServiceTag 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09715-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="09715-133">筆記</span><span class="sxs-lookup"><span data-stu-id="09715-133">NOTES</span></span>

## <span data-ttu-id="09715-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="09715-134">RELATED LINKS</span></span>
