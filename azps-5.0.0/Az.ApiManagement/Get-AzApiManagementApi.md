---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285712"
---
# <span data-ttu-id="bafbd-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bafbd-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="bafbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bafbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bafbd-103">取得 API。</span><span class="sxs-lookup"><span data-stu-id="bafbd-103">Gets an API.</span></span>

## <span data-ttu-id="bafbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="bafbd-104">SYNTAX</span></span>

### <span data-ttu-id="bafbd-105">GetAllApis (預設) </span><span class="sxs-lookup"><span data-stu-id="bafbd-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bafbd-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="bafbd-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bafbd-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="bafbd-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bafbd-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="bafbd-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bafbd-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="bafbd-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bafbd-110">說明</span><span class="sxs-lookup"><span data-stu-id="bafbd-110">DESCRIPTION</span></span>
<span data-ttu-id="bafbd-111">**AzApiManagementApi** Cmdlet 會取得一或多個 Azure API 管理 api。</span><span class="sxs-lookup"><span data-stu-id="bafbd-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="bafbd-112">示例</span><span class="sxs-lookup"><span data-stu-id="bafbd-112">EXAMPLES</span></span>

### <span data-ttu-id="bafbd-113">範例1：取得所有管理 Api</span><span class="sxs-lookup"><span data-stu-id="bafbd-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="bafbd-114">這個命令會取得指定內容的所有 Api。</span><span class="sxs-lookup"><span data-stu-id="bafbd-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="bafbd-115">範例2：依識別碼取得管理 API</span><span class="sxs-lookup"><span data-stu-id="bafbd-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="bafbd-116">這個命令會取得具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="bafbd-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="bafbd-117">範例3：依名稱取得管理 API</span><span class="sxs-lookup"><span data-stu-id="bafbd-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="bafbd-118">這個命令會取得具有指定名稱的 API。</span><span class="sxs-lookup"><span data-stu-id="bafbd-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="bafbd-119">範例4：透過 GatewayId 取得管理 API</span><span class="sxs-lookup"><span data-stu-id="bafbd-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="bafbd-120">這個命令會取得指定 GatewayId 的 API。</span><span class="sxs-lookup"><span data-stu-id="bafbd-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="bafbd-121">參數</span><span class="sxs-lookup"><span data-stu-id="bafbd-121">PARAMETERS</span></span>

### <span data-ttu-id="bafbd-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bafbd-122">-ApiId</span></span>
<span data-ttu-id="bafbd-123">指定要取得的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bafbd-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="bafbd-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bafbd-124">-ApiRevision</span></span>
<span data-ttu-id="bafbd-125">特定 Api 修訂的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="bafbd-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="bafbd-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="bafbd-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="bafbd-127">-內容</span><span class="sxs-lookup"><span data-stu-id="bafbd-127">-Context</span></span>
<span data-ttu-id="bafbd-128">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="bafbd-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bafbd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafbd-129">-DefaultProfile</span></span>
<span data-ttu-id="bafbd-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bafbd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bafbd-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="bafbd-131">-GatewayId</span></span>
<span data-ttu-id="bafbd-132">如果已指定，將會嘗試取得所有閘道 Api。</span><span class="sxs-lookup"><span data-stu-id="bafbd-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="bafbd-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="bafbd-133">-Name</span></span>
<span data-ttu-id="bafbd-134">指定要取得的 API 名稱。</span><span class="sxs-lookup"><span data-stu-id="bafbd-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="bafbd-135">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="bafbd-135">-ProductId</span></span>
<span data-ttu-id="bafbd-136">指定要取得 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="bafbd-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="bafbd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafbd-137">CommonParameters</span></span>
<span data-ttu-id="bafbd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bafbd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafbd-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bafbd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafbd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="bafbd-140">INPUTS</span></span>

### <span data-ttu-id="bafbd-141">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bafbd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bafbd-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bafbd-142">System.String</span></span>

## <span data-ttu-id="bafbd-143">輸出</span><span class="sxs-lookup"><span data-stu-id="bafbd-143">OUTPUTS</span></span>

### <span data-ttu-id="bafbd-144">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bafbd-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="bafbd-145">筆記</span><span class="sxs-lookup"><span data-stu-id="bafbd-145">NOTES</span></span>

## <span data-ttu-id="bafbd-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="bafbd-146">RELATED LINKS</span></span>

[<span data-ttu-id="bafbd-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bafbd-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="bafbd-148">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bafbd-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="bafbd-149">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bafbd-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="bafbd-150">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bafbd-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="bafbd-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bafbd-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


