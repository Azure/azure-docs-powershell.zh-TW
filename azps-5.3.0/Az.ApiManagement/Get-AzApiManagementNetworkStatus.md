---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447575"
---
# <span data-ttu-id="09780-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="09780-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="09780-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09780-102">SYNOPSIS</span></span>
<span data-ttu-id="09780-103">取得 Api 管理服務在雲端服務內所依賴之外部資源的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="09780-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="09780-104">這也會傳回 CloudService 所顯示的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="09780-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="09780-105">句法</span><span class="sxs-lookup"><span data-stu-id="09780-105">SYNTAX</span></span>

### <span data-ttu-id="09780-106">ByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="09780-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09780-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="09780-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09780-108">說明</span><span class="sxs-lookup"><span data-stu-id="09780-108">DESCRIPTION</span></span>
<span data-ttu-id="09780-109">取得 Api 管理服務的網路狀態</span><span class="sxs-lookup"><span data-stu-id="09780-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="09780-110">示例</span><span class="sxs-lookup"><span data-stu-id="09780-110">EXAMPLES</span></span>

### <span data-ttu-id="09780-111">範例1</span><span class="sxs-lookup"><span data-stu-id="09780-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="09780-112">取得 ApiManagement 服務所依據之不同資源的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="09780-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="09780-113">參數</span><span class="sxs-lookup"><span data-stu-id="09780-113">PARAMETERS</span></span>

### <span data-ttu-id="09780-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="09780-114">-ApiManagementObject</span></span>
<span data-ttu-id="09780-115">PsApiManagement 的實例。</span><span class="sxs-lookup"><span data-stu-id="09780-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="09780-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="09780-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09780-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09780-117">-DefaultProfile</span></span>
<span data-ttu-id="09780-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09780-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09780-119">-位置</span><span class="sxs-lookup"><span data-stu-id="09780-119">-Location</span></span>
<span data-ttu-id="09780-120">API 管理服務的位置。</span><span class="sxs-lookup"><span data-stu-id="09780-120">Location of the API Management Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09780-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="09780-121">-Name</span></span>
<span data-ttu-id="09780-122">API 管理的名稱。</span><span class="sxs-lookup"><span data-stu-id="09780-122">Name of API Management.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09780-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09780-123">-ResourceGroupName</span></span>
<span data-ttu-id="09780-124">API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09780-124">Name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09780-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09780-125">CommonParameters</span></span>
<span data-ttu-id="09780-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09780-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09780-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09780-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09780-128">輸入</span><span class="sxs-lookup"><span data-stu-id="09780-128">INPUTS</span></span>

### <span data-ttu-id="09780-129">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="09780-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="09780-130">System.object</span><span class="sxs-lookup"><span data-stu-id="09780-130">System.String</span></span>

## <span data-ttu-id="09780-131">輸出</span><span class="sxs-lookup"><span data-stu-id="09780-131">OUTPUTS</span></span>

### <span data-ttu-id="09780-132">PsApiManagementNetworkStatus 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="09780-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="09780-133">筆記</span><span class="sxs-lookup"><span data-stu-id="09780-133">NOTES</span></span>

## <span data-ttu-id="09780-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="09780-134">RELATED LINKS</span></span>
