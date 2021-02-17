---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 4f9e917f17037e5f47b52501007da5556bde1187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401074"
---
# <span data-ttu-id="f84f2-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f84f2-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="f84f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f84f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f84f2-103">取得 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f84f2-103">Get the API Release.</span></span>

## <span data-ttu-id="f84f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="f84f2-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f84f2-105">描述</span><span class="sxs-lookup"><span data-stu-id="f84f2-105">DESCRIPTION</span></span>
<span data-ttu-id="f84f2-106">**Get-AzApiManagementApiRelease** Cmdlet 會取得 Azure API 管理 API 的一或多個版本。</span><span class="sxs-lookup"><span data-stu-id="f84f2-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="f84f2-107">例子</span><span class="sxs-lookup"><span data-stu-id="f84f2-107">EXAMPLES</span></span>

### <span data-ttu-id="f84f2-108">範例 1：取得 API 的所有版本</span><span class="sxs-lookup"><span data-stu-id="f84f2-108">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="f84f2-109">此命令會針對指定的上下文獲得 `echo-api` API 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="f84f2-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="f84f2-110">範例 2：取得特定 API 發行版本的發行資訊</span><span class="sxs-lookup"><span data-stu-id="f84f2-110">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="f84f2-111">此命令會使用指定的 releaseId，獲得特定 API 的發行資訊。</span><span class="sxs-lookup"><span data-stu-id="f84f2-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="f84f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="f84f2-112">PARAMETERS</span></span>

### <span data-ttu-id="f84f2-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f84f2-113">-ApiId</span></span>
<span data-ttu-id="f84f2-114">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f84f2-114">API identifier to look for.</span></span>
<span data-ttu-id="f84f2-115">如果指定，會嘗試使用識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="f84f2-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="f84f2-116">-內容</span><span class="sxs-lookup"><span data-stu-id="f84f2-116">-Context</span></span>
<span data-ttu-id="f84f2-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f84f2-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f84f2-118">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="f84f2-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f84f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84f2-119">-DefaultProfile</span></span>
<span data-ttu-id="f84f2-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f84f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f84f2-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="f84f2-121">-ReleaseId</span></span>
<span data-ttu-id="f84f2-122">發行識別碼。</span><span class="sxs-lookup"><span data-stu-id="f84f2-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="f84f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84f2-123">CommonParameters</span></span>
<span data-ttu-id="f84f2-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f84f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84f2-125">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f84f2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84f2-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f84f2-126">INPUTS</span></span>

### <span data-ttu-id="f84f2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="f84f2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f84f2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f84f2-128">System.String</span></span>

## <span data-ttu-id="f84f2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f84f2-129">OUTPUTS</span></span>

### <span data-ttu-id="f84f2-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f84f2-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f84f2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f84f2-131">NOTES</span></span>

## <span data-ttu-id="f84f2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f84f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="f84f2-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f84f2-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="f84f2-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f84f2-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="f84f2-135">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f84f2-135">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)