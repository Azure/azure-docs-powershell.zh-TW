---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287107"
---
# <span data-ttu-id="daf24-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="daf24-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="daf24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daf24-102">SYNOPSIS</span></span>
<span data-ttu-id="daf24-103">取得 API 版本。</span><span class="sxs-lookup"><span data-stu-id="daf24-103">Get the API Release.</span></span>

## <span data-ttu-id="daf24-104">句法</span><span class="sxs-lookup"><span data-stu-id="daf24-104">SYNTAX</span></span>

### <span data-ttu-id="daf24-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="daf24-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daf24-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="daf24-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="daf24-107">說明</span><span class="sxs-lookup"><span data-stu-id="daf24-107">DESCRIPTION</span></span>
<span data-ttu-id="daf24-108">**AzApiManagementApiRelease** Cmdlet 會取得一或多個 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="daf24-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="daf24-109">示例</span><span class="sxs-lookup"><span data-stu-id="daf24-109">EXAMPLES</span></span>

### <span data-ttu-id="daf24-110">範例1：取得 API 的所有版本</span><span class="sxs-lookup"><span data-stu-id="daf24-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="daf24-111">這個命令會取得 `echo-api` 指定內容的所有 API 版本。</span><span class="sxs-lookup"><span data-stu-id="daf24-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="daf24-112">範例2：取得特定 API 版本的發行資訊</span><span class="sxs-lookup"><span data-stu-id="daf24-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="daf24-113">這個命令會以指定的 releaseId 來取得特定 API 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="daf24-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="daf24-114">參數</span><span class="sxs-lookup"><span data-stu-id="daf24-114">PARAMETERS</span></span>

### <span data-ttu-id="daf24-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="daf24-115">-ApiId</span></span>
<span data-ttu-id="daf24-116">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="daf24-116">API identifier to look for.</span></span>
<span data-ttu-id="daf24-117">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="daf24-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="daf24-118">-內容</span><span class="sxs-lookup"><span data-stu-id="daf24-118">-Context</span></span>
<span data-ttu-id="daf24-119">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="daf24-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="daf24-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="daf24-120">This parameter is required.</span></span>

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

### <span data-ttu-id="daf24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf24-121">-DefaultProfile</span></span>
<span data-ttu-id="daf24-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="daf24-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daf24-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="daf24-123">-ReleaseId</span></span>
<span data-ttu-id="daf24-124">發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="daf24-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="daf24-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daf24-125">-ResourceId</span></span>
<span data-ttu-id="daf24-126">Api 發行的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="daf24-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="daf24-127">如果已指定，將會嘗試透過識別碼尋找 api 版本。</span><span class="sxs-lookup"><span data-stu-id="daf24-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="daf24-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="daf24-128">This parameter is required.</span></span>

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

### <span data-ttu-id="daf24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf24-129">CommonParameters</span></span>
<span data-ttu-id="daf24-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daf24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf24-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="daf24-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf24-132">輸入</span><span class="sxs-lookup"><span data-stu-id="daf24-132">INPUTS</span></span>

### <span data-ttu-id="daf24-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="daf24-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="daf24-134">System.object</span><span class="sxs-lookup"><span data-stu-id="daf24-134">System.String</span></span>

## <span data-ttu-id="daf24-135">輸出</span><span class="sxs-lookup"><span data-stu-id="daf24-135">OUTPUTS</span></span>

### <span data-ttu-id="daf24-136">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="daf24-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="daf24-137">筆記</span><span class="sxs-lookup"><span data-stu-id="daf24-137">NOTES</span></span>

## <span data-ttu-id="daf24-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="daf24-138">RELATED LINKS</span></span>

[<span data-ttu-id="daf24-139">新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="daf24-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="daf24-140">移除-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="daf24-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="daf24-141">更新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="daf24-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)