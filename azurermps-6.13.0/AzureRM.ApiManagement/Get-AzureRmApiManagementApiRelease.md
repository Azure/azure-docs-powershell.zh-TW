---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623574"
---
# <span data-ttu-id="c5fe7-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c5fe7-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="c5fe7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fe7-103">取得 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5fe7-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5fe7-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5fe7-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="c5fe7-106">**AzureRmApiManagementApiRelease** Cmdlet 會取得一或多個 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="c5fe7-107">示例</span><span class="sxs-lookup"><span data-stu-id="c5fe7-107">EXAMPLES</span></span>

### <span data-ttu-id="c5fe7-108">範例1：取得 API 的所有版本</span><span class="sxs-lookup"><span data-stu-id="c5fe7-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="c5fe7-109">這個命令會取得 `echo-api` 指定內容的所有 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="c5fe7-110">範例2：取得特定 API 版本的發行資訊</span><span class="sxs-lookup"><span data-stu-id="c5fe7-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="c5fe7-111">這個命令會以指定的 releaseId 來取得特定 API 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="c5fe7-112">參數</span><span class="sxs-lookup"><span data-stu-id="c5fe7-112">PARAMETERS</span></span>

### <span data-ttu-id="c5fe7-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c5fe7-113">-ApiId</span></span>
<span data-ttu-id="c5fe7-114">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-114">API identifier to look for.</span></span>
<span data-ttu-id="c5fe7-115">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c5fe7-116">-內容</span><span class="sxs-lookup"><span data-stu-id="c5fe7-116">-Context</span></span>
<span data-ttu-id="c5fe7-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c5fe7-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5fe7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fe7-119">-DefaultProfile</span></span>
<span data-ttu-id="c5fe7-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fe7-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c5fe7-121">-ReleaseId</span></span>
<span data-ttu-id="c5fe7-122">發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="c5fe7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fe7-123">CommonParameters</span></span>
<span data-ttu-id="c5fe7-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fe7-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5fe7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fe7-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c5fe7-126">INPUTS</span></span>

### <span data-ttu-id="c5fe7-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c5fe7-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c5fe7-128">System.object</span><span class="sxs-lookup"><span data-stu-id="c5fe7-128">System.String</span></span>

## <span data-ttu-id="c5fe7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c5fe7-129">OUTPUTS</span></span>

### <span data-ttu-id="c5fe7-130">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c5fe7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c5fe7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c5fe7-131">NOTES</span></span>

## <span data-ttu-id="c5fe7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5fe7-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5fe7-133">新-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c5fe7-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="c5fe7-134">移除-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c5fe7-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="c5fe7-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c5fe7-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
