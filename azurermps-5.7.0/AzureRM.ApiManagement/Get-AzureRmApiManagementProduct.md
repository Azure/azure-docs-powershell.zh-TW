---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448806"
---
# <span data-ttu-id="5174b-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5174b-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="5174b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5174b-102">SYNOPSIS</span></span>
<span data-ttu-id="5174b-103">取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="5174b-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5174b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5174b-104">SYNTAX</span></span>

### <span data-ttu-id="5174b-105">GetAllProducts (預設) </span><span class="sxs-lookup"><span data-stu-id="5174b-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5174b-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5174b-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5174b-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="5174b-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5174b-108">說明</span><span class="sxs-lookup"><span data-stu-id="5174b-108">DESCRIPTION</span></span>
<span data-ttu-id="5174b-109">**AzureRmApiManagementProduct** Cmdlet 會取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="5174b-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="5174b-110">示例</span><span class="sxs-lookup"><span data-stu-id="5174b-110">EXAMPLES</span></span>

### <span data-ttu-id="5174b-111">範例1：取得所有產品</span><span class="sxs-lookup"><span data-stu-id="5174b-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="5174b-112">這個命令會取得所有 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="5174b-112">This command get all API Management products.</span></span>

### <span data-ttu-id="5174b-113">範例2：依識別碼取得產品</span><span class="sxs-lookup"><span data-stu-id="5174b-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="5174b-114">這個命令會透過識別碼取得 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="5174b-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="5174b-115">參數</span><span class="sxs-lookup"><span data-stu-id="5174b-115">PARAMETERS</span></span>

### <span data-ttu-id="5174b-116">-內容</span><span class="sxs-lookup"><span data-stu-id="5174b-116">-Context</span></span>
<span data-ttu-id="5174b-117">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="5174b-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5174b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5174b-118">-DefaultProfile</span></span>
<span data-ttu-id="5174b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5174b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5174b-120">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="5174b-120">-ProductId</span></span>
<span data-ttu-id="5174b-121">指定要搜尋的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="5174b-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5174b-122">-標題</span><span class="sxs-lookup"><span data-stu-id="5174b-122">-Title</span></span>
<span data-ttu-id="5174b-123">指定要尋找之產品的標題。</span><span class="sxs-lookup"><span data-stu-id="5174b-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="5174b-124">如果已指定，此 Cmdlet 會嘗試透過標題取得產品。</span><span class="sxs-lookup"><span data-stu-id="5174b-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5174b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5174b-125">CommonParameters</span></span>
<span data-ttu-id="5174b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5174b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5174b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5174b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5174b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5174b-128">INPUTS</span></span>

### <span data-ttu-id="5174b-129">所有</span><span class="sxs-lookup"><span data-stu-id="5174b-129">None</span></span>
<span data-ttu-id="5174b-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5174b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5174b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5174b-131">OUTPUTS</span></span>

### <span data-ttu-id="5174b-132">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5174b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="5174b-133">API 管理服務中產品的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5174b-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="5174b-134">IList<ApiManagement. ServiceManagement. PsApiManagementProduct]></span><span class="sxs-lookup"><span data-stu-id="5174b-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="5174b-135">API 管理服務中的產品清單。</span><span class="sxs-lookup"><span data-stu-id="5174b-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="5174b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5174b-136">NOTES</span></span>

## <span data-ttu-id="5174b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5174b-137">RELATED LINKS</span></span>

[<span data-ttu-id="5174b-138">新-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5174b-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="5174b-139">移除-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5174b-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="5174b-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5174b-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


