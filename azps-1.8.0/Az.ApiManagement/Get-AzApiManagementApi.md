---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: a87c75058e3ebfb1ae7d14e729fdc9280cdccb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611643"
---
# <span data-ttu-id="00b38-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00b38-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="00b38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00b38-102">SYNOPSIS</span></span>
<span data-ttu-id="00b38-103">取得 API。</span><span class="sxs-lookup"><span data-stu-id="00b38-103">Gets an API.</span></span>

## <span data-ttu-id="00b38-104">句法</span><span class="sxs-lookup"><span data-stu-id="00b38-104">SYNTAX</span></span>

### <span data-ttu-id="00b38-105">GetAllApis (預設) </span><span class="sxs-lookup"><span data-stu-id="00b38-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00b38-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="00b38-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00b38-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="00b38-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00b38-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="00b38-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00b38-109">說明</span><span class="sxs-lookup"><span data-stu-id="00b38-109">DESCRIPTION</span></span>
<span data-ttu-id="00b38-110">**AzApiManagementApi** Cmdlet 會取得一或多個 Azure API 管理 api。</span><span class="sxs-lookup"><span data-stu-id="00b38-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="00b38-111">示例</span><span class="sxs-lookup"><span data-stu-id="00b38-111">EXAMPLES</span></span>

### <span data-ttu-id="00b38-112">範例1：取得所有管理 Api</span><span class="sxs-lookup"><span data-stu-id="00b38-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="00b38-113">這個命令會取得指定內容的所有 Api。</span><span class="sxs-lookup"><span data-stu-id="00b38-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="00b38-114">範例2：依識別碼取得管理 API</span><span class="sxs-lookup"><span data-stu-id="00b38-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="00b38-115">這個命令會取得具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="00b38-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="00b38-116">範例3：依名稱取得管理 API</span><span class="sxs-lookup"><span data-stu-id="00b38-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="00b38-117">這個命令會取得具有指定名稱的 API。</span><span class="sxs-lookup"><span data-stu-id="00b38-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="00b38-118">參數</span><span class="sxs-lookup"><span data-stu-id="00b38-118">PARAMETERS</span></span>

### <span data-ttu-id="00b38-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00b38-119">-ApiId</span></span>
<span data-ttu-id="00b38-120">指定要取得的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="00b38-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="00b38-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="00b38-121">-ApiRevision</span></span>
<span data-ttu-id="00b38-122">特定 Api 修訂的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="00b38-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="00b38-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="00b38-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="00b38-124">-內容</span><span class="sxs-lookup"><span data-stu-id="00b38-124">-Context</span></span>
<span data-ttu-id="00b38-125">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="00b38-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="00b38-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b38-126">-DefaultProfile</span></span>
<span data-ttu-id="00b38-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00b38-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b38-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="00b38-128">-Name</span></span>
<span data-ttu-id="00b38-129">指定要取得的 API 名稱。</span><span class="sxs-lookup"><span data-stu-id="00b38-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="00b38-130">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="00b38-130">-ProductId</span></span>
<span data-ttu-id="00b38-131">指定要取得 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="00b38-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="00b38-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b38-132">CommonParameters</span></span>
<span data-ttu-id="00b38-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00b38-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b38-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00b38-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b38-135">輸入</span><span class="sxs-lookup"><span data-stu-id="00b38-135">INPUTS</span></span>

### <span data-ttu-id="00b38-136">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="00b38-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00b38-137">System.object</span><span class="sxs-lookup"><span data-stu-id="00b38-137">System.String</span></span>

## <span data-ttu-id="00b38-138">輸出</span><span class="sxs-lookup"><span data-stu-id="00b38-138">OUTPUTS</span></span>

### <span data-ttu-id="00b38-139">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="00b38-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="00b38-140">筆記</span><span class="sxs-lookup"><span data-stu-id="00b38-140">NOTES</span></span>

## <span data-ttu-id="00b38-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="00b38-141">RELATED LINKS</span></span>

[<span data-ttu-id="00b38-142">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00b38-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="00b38-143">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00b38-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="00b38-144">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00b38-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="00b38-145">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00b38-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="00b38-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00b38-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


