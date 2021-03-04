---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 589338afde60e069646cb677205da11e322ba7da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917138"
---
# <span data-ttu-id="a4fa1-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a4fa1-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="a4fa1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a4fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fa1-103">獲得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="a4fa1-104">語法</span><span class="sxs-lookup"><span data-stu-id="a4fa1-104">SYNTAX</span></span>

### <span data-ttu-id="a4fa1-105">GetAllProducts (預設) </span><span class="sxs-lookup"><span data-stu-id="a4fa1-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4fa1-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="a4fa1-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4fa1-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="a4fa1-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4fa1-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="a4fa1-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4fa1-109">描述</span><span class="sxs-lookup"><span data-stu-id="a4fa1-109">DESCRIPTION</span></span>
<span data-ttu-id="a4fa1-110">**Get-AzApiManagementProduct** Cmdlet 會取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="a4fa1-111">例子</span><span class="sxs-lookup"><span data-stu-id="a4fa1-111">EXAMPLES</span></span>

### <span data-ttu-id="a4fa1-112">範例 1：取得所有產品</span><span class="sxs-lookup"><span data-stu-id="a4fa1-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="a4fa1-113">此命令會取得所有 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-113">This command get all API Management products.</span></span>

### <span data-ttu-id="a4fa1-114">範例 2：取得產品識別碼</span><span class="sxs-lookup"><span data-stu-id="a4fa1-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="a4fa1-115">此命令會以識別碼取得 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="a4fa1-116">參數</span><span class="sxs-lookup"><span data-stu-id="a4fa1-116">PARAMETERS</span></span>

### <span data-ttu-id="a4fa1-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a4fa1-117">-ApiId</span></span>
<span data-ttu-id="a4fa1-118">Api 的 ApiId，以尋找相關產品。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="a4fa1-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4fa1-120">-內容</span><span class="sxs-lookup"><span data-stu-id="a4fa1-120">-Context</span></span>
<span data-ttu-id="a4fa1-121">指定 **PsApiManagementCoNtext 物件的** 實例。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a4fa1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fa1-122">-DefaultProfile</span></span>
<span data-ttu-id="a4fa1-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4fa1-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a4fa1-124">-ProductId</span></span>
<span data-ttu-id="a4fa1-125">指定要搜尋的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="a4fa1-126">-標題</span><span class="sxs-lookup"><span data-stu-id="a4fa1-126">-Title</span></span>
<span data-ttu-id="a4fa1-127">指定要尋找的產品標題。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="a4fa1-128">如果指定，Cmdlet 會嘗試按標題取得產品。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fa1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fa1-129">CommonParameters</span></span>
<span data-ttu-id="a4fa1-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a4fa1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fa1-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4fa1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fa1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a4fa1-132">INPUTS</span></span>

### <span data-ttu-id="a4fa1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="a4fa1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4fa1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a4fa1-134">System.String</span></span>

## <span data-ttu-id="a4fa1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a4fa1-135">OUTPUTS</span></span>

### <span data-ttu-id="a4fa1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a4fa1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="a4fa1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a4fa1-137">NOTES</span></span>

## <span data-ttu-id="a4fa1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4fa1-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4fa1-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a4fa1-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="a4fa1-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a4fa1-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="a4fa1-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a4fa1-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


