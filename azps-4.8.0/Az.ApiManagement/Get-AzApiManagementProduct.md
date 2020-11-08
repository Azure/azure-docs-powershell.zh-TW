---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969459"
---
# <span data-ttu-id="1748c-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1748c-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="1748c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1748c-102">SYNOPSIS</span></span>
<span data-ttu-id="1748c-103">取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="1748c-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="1748c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1748c-104">SYNTAX</span></span>

### <span data-ttu-id="1748c-105">GetAllProducts (預設) </span><span class="sxs-lookup"><span data-stu-id="1748c-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1748c-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="1748c-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1748c-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="1748c-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1748c-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="1748c-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1748c-109">說明</span><span class="sxs-lookup"><span data-stu-id="1748c-109">DESCRIPTION</span></span>
<span data-ttu-id="1748c-110">**AzApiManagementProduct** Cmdlet 會取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="1748c-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="1748c-111">示例</span><span class="sxs-lookup"><span data-stu-id="1748c-111">EXAMPLES</span></span>

### <span data-ttu-id="1748c-112">範例1：取得所有產品</span><span class="sxs-lookup"><span data-stu-id="1748c-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="1748c-113">這個命令會取得所有 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="1748c-113">This command get all API Management products.</span></span>

### <span data-ttu-id="1748c-114">範例2：依識別碼取得產品</span><span class="sxs-lookup"><span data-stu-id="1748c-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="1748c-115">這個命令會透過識別碼取得 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="1748c-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="1748c-116">參數</span><span class="sxs-lookup"><span data-stu-id="1748c-116">PARAMETERS</span></span>

### <span data-ttu-id="1748c-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1748c-117">-ApiId</span></span>
<span data-ttu-id="1748c-118">Api 的 ApiId，以尋找相關產品。</span><span class="sxs-lookup"><span data-stu-id="1748c-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="1748c-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1748c-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="1748c-120">-內容</span><span class="sxs-lookup"><span data-stu-id="1748c-120">-Context</span></span>
<span data-ttu-id="1748c-121">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="1748c-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1748c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1748c-122">-DefaultProfile</span></span>
<span data-ttu-id="1748c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1748c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1748c-124">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="1748c-124">-ProductId</span></span>
<span data-ttu-id="1748c-125">指定要搜尋的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="1748c-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="1748c-126">-標題</span><span class="sxs-lookup"><span data-stu-id="1748c-126">-Title</span></span>
<span data-ttu-id="1748c-127">指定要尋找之產品的標題。</span><span class="sxs-lookup"><span data-stu-id="1748c-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="1748c-128">如果已指定，此 Cmdlet 會嘗試透過標題取得產品。</span><span class="sxs-lookup"><span data-stu-id="1748c-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="1748c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1748c-129">CommonParameters</span></span>
<span data-ttu-id="1748c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1748c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1748c-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1748c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1748c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1748c-132">INPUTS</span></span>

### <span data-ttu-id="1748c-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1748c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1748c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1748c-134">System.String</span></span>

## <span data-ttu-id="1748c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1748c-135">OUTPUTS</span></span>

### <span data-ttu-id="1748c-136">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1748c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="1748c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1748c-137">NOTES</span></span>

## <span data-ttu-id="1748c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1748c-138">RELATED LINKS</span></span>

[<span data-ttu-id="1748c-139">新-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1748c-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="1748c-140">移除-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1748c-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="1748c-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1748c-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


