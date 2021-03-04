---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 5e1cbec98e2b501a71f022766f7248c3209d590f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912122"
---
# <span data-ttu-id="7e69d-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="7e69d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e69d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e69d-103">獲得 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-103">Gets an API.</span></span>

## <span data-ttu-id="7e69d-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e69d-104">SYNTAX</span></span>

### <span data-ttu-id="7e69d-105">GetAllApis (預設) </span><span class="sxs-lookup"><span data-stu-id="7e69d-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e69d-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="7e69d-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e69d-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="7e69d-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e69d-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="7e69d-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e69d-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="7e69d-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e69d-110">描述</span><span class="sxs-lookup"><span data-stu-id="7e69d-110">DESCRIPTION</span></span>
<span data-ttu-id="7e69d-111">**Get-AzApiManagementApi** Cmdlet 會取得一或多個 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="7e69d-112">例子</span><span class="sxs-lookup"><span data-stu-id="7e69d-112">EXAMPLES</span></span>

### <span data-ttu-id="7e69d-113">範例 1：取得所有管理 API</span><span class="sxs-lookup"><span data-stu-id="7e69d-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="7e69d-114">此命令會獲得指定內容的所有 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="7e69d-115">範例 2：取得管理 API by ID</span><span class="sxs-lookup"><span data-stu-id="7e69d-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="7e69d-116">此命令會獲得具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="7e69d-117">範例 3：根據名稱取得管理 API</span><span class="sxs-lookup"><span data-stu-id="7e69d-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="7e69d-118">此命令會獲得具有指定名稱的 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="7e69d-119">範例 4：取得閘道Id 管理 API</span><span class="sxs-lookup"><span data-stu-id="7e69d-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="7e69d-120">此命令會獲得指定 GatewayId 的 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="7e69d-121">參數</span><span class="sxs-lookup"><span data-stu-id="7e69d-121">PARAMETERS</span></span>

### <span data-ttu-id="7e69d-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7e69d-122">-ApiId</span></span>
<span data-ttu-id="7e69d-123">指定要取得之 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e69d-123">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e69d-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7e69d-124">-ApiRevision</span></span>
<span data-ttu-id="7e69d-125">特定 Api 修訂的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e69d-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="7e69d-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e69d-126">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e69d-127">-內容</span><span class="sxs-lookup"><span data-stu-id="7e69d-127">-Context</span></span>
<span data-ttu-id="7e69d-128">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="7e69d-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e69d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e69d-129">-DefaultProfile</span></span>
<span data-ttu-id="7e69d-130">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e69d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e69d-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7e69d-131">-GatewayId</span></span>
<span data-ttu-id="7e69d-132">如果指定，會嘗試取得所有閘道 API。</span><span class="sxs-lookup"><span data-stu-id="7e69d-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e69d-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e69d-133">-Name</span></span>
<span data-ttu-id="7e69d-134">指定要取得之 API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e69d-134">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e69d-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7e69d-135">-ProductId</span></span>
<span data-ttu-id="7e69d-136">指定要取得 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e69d-136">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e69d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e69d-137">CommonParameters</span></span>
<span data-ttu-id="7e69d-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e69d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e69d-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e69d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e69d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7e69d-140">INPUTS</span></span>

### <span data-ttu-id="7e69d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="7e69d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7e69d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7e69d-142">System.String</span></span>

## <span data-ttu-id="7e69d-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7e69d-143">OUTPUTS</span></span>

### <span data-ttu-id="7e69d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7e69d-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7e69d-145">NOTES</span></span>

## <span data-ttu-id="7e69d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e69d-146">RELATED LINKS</span></span>

[<span data-ttu-id="7e69d-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="7e69d-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="7e69d-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="7e69d-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="7e69d-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7e69d-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


