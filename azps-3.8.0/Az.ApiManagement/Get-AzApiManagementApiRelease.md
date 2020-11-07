---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: de4f91e7d2df778952ca505f37f1d6f6874a6524
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957896"
---
# <span data-ttu-id="f03ec-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f03ec-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="f03ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f03ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f03ec-103">取得 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f03ec-103">Get the API Release.</span></span>

## <span data-ttu-id="f03ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="f03ec-104">SYNTAX</span></span>

### <span data-ttu-id="f03ec-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f03ec-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f03ec-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f03ec-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f03ec-107">說明</span><span class="sxs-lookup"><span data-stu-id="f03ec-107">DESCRIPTION</span></span>
<span data-ttu-id="f03ec-108">**AzApiManagementApiRelease** Cmdlet 會取得一或多個 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f03ec-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="f03ec-109">示例</span><span class="sxs-lookup"><span data-stu-id="f03ec-109">EXAMPLES</span></span>

### <span data-ttu-id="f03ec-110">範例1：取得 API 的所有版本</span><span class="sxs-lookup"><span data-stu-id="f03ec-110">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contoso
```

<span data-ttu-id="f03ec-111">這個命令會取得 `echo-api` 指定內容的所有 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f03ec-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="f03ec-112">範例2：取得特定 API 版本的發行資訊</span><span class="sxs-lookup"><span data-stu-id="f03ec-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f03ec-113">這個命令會以指定的 releaseId 來取得特定 API 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="f03ec-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="f03ec-114">參數</span><span class="sxs-lookup"><span data-stu-id="f03ec-114">PARAMETERS</span></span>

### <span data-ttu-id="f03ec-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f03ec-115">-ApiId</span></span>
<span data-ttu-id="f03ec-116">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f03ec-116">API identifier to look for.</span></span>
<span data-ttu-id="f03ec-117">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="f03ec-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03ec-118">-內容</span><span class="sxs-lookup"><span data-stu-id="f03ec-118">-Context</span></span>
<span data-ttu-id="f03ec-119">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f03ec-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f03ec-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f03ec-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f03ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03ec-121">-DefaultProfile</span></span>
<span data-ttu-id="f03ec-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f03ec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03ec-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="f03ec-123">-ReleaseId</span></span>
<span data-ttu-id="f03ec-124">發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f03ec-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03ec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f03ec-125">-ResourceId</span></span>
<span data-ttu-id="f03ec-126">Api 發行的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f03ec-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="f03ec-127">如果已指定，將會嘗試透過識別碼尋找 api 版本。</span><span class="sxs-lookup"><span data-stu-id="f03ec-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="f03ec-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f03ec-128">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03ec-129">CommonParameters</span></span>
<span data-ttu-id="f03ec-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f03ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03ec-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f03ec-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03ec-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f03ec-132">INPUTS</span></span>

### <span data-ttu-id="f03ec-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f03ec-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f03ec-134">System.object</span><span class="sxs-lookup"><span data-stu-id="f03ec-134">System.String</span></span>

## <span data-ttu-id="f03ec-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f03ec-135">OUTPUTS</span></span>

### <span data-ttu-id="f03ec-136">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f03ec-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f03ec-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f03ec-137">NOTES</span></span>

## <span data-ttu-id="f03ec-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f03ec-138">RELATED LINKS</span></span>

[<span data-ttu-id="f03ec-139">新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f03ec-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="f03ec-140">移除-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f03ec-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="f03ec-141">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f03ec-141">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)