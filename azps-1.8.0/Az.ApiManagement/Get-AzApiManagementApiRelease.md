---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611641"
---
# <span data-ttu-id="92fe0-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92fe0-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="92fe0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="92fe0-103">取得 API 版本。</span><span class="sxs-lookup"><span data-stu-id="92fe0-103">Get the API Release.</span></span>

## <span data-ttu-id="92fe0-104">句法</span><span class="sxs-lookup"><span data-stu-id="92fe0-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92fe0-105">說明</span><span class="sxs-lookup"><span data-stu-id="92fe0-105">DESCRIPTION</span></span>
<span data-ttu-id="92fe0-106">**AzApiManagementApiRelease** Cmdlet 會取得一或多個 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="92fe0-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="92fe0-107">示例</span><span class="sxs-lookup"><span data-stu-id="92fe0-107">EXAMPLES</span></span>

### <span data-ttu-id="92fe0-108">範例1：取得 API 的所有版本</span><span class="sxs-lookup"><span data-stu-id="92fe0-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="92fe0-109">這個命令會取得 `echo-api` 指定內容的所有 API 版本。</span><span class="sxs-lookup"><span data-stu-id="92fe0-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="92fe0-110">範例2：取得特定 API 版本的發行資訊</span><span class="sxs-lookup"><span data-stu-id="92fe0-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="92fe0-111">這個命令會以指定的 releaseId 來取得特定 API 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="92fe0-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="92fe0-112">參數</span><span class="sxs-lookup"><span data-stu-id="92fe0-112">PARAMETERS</span></span>

### <span data-ttu-id="92fe0-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="92fe0-113">-ApiId</span></span>
<span data-ttu-id="92fe0-114">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="92fe0-114">API identifier to look for.</span></span>
<span data-ttu-id="92fe0-115">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="92fe0-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="92fe0-116">-內容</span><span class="sxs-lookup"><span data-stu-id="92fe0-116">-Context</span></span>
<span data-ttu-id="92fe0-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="92fe0-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="92fe0-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="92fe0-118">This parameter is required.</span></span>

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

### <span data-ttu-id="92fe0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fe0-119">-DefaultProfile</span></span>
<span data-ttu-id="92fe0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92fe0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92fe0-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="92fe0-121">-ReleaseId</span></span>
<span data-ttu-id="92fe0-122">發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="92fe0-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="92fe0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fe0-123">CommonParameters</span></span>
<span data-ttu-id="92fe0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92fe0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fe0-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92fe0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fe0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="92fe0-126">INPUTS</span></span>

### <span data-ttu-id="92fe0-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="92fe0-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92fe0-128">System.object</span><span class="sxs-lookup"><span data-stu-id="92fe0-128">System.String</span></span>

## <span data-ttu-id="92fe0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="92fe0-129">OUTPUTS</span></span>

### <span data-ttu-id="92fe0-130">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="92fe0-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="92fe0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="92fe0-131">NOTES</span></span>

## <span data-ttu-id="92fe0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="92fe0-132">RELATED LINKS</span></span>

[<span data-ttu-id="92fe0-133">新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92fe0-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="92fe0-134">移除-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92fe0-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="92fe0-135">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92fe0-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)