---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450129"
---
# <span data-ttu-id="e448b-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e448b-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e448b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e448b-102">SYNOPSIS</span></span>
<span data-ttu-id="e448b-103">取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="e448b-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e448b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e448b-104">SYNTAX</span></span>

### <span data-ttu-id="e448b-105">取得所有 producst (預設) </span><span class="sxs-lookup"><span data-stu-id="e448b-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e448b-106">依識別碼取得</span><span class="sxs-lookup"><span data-stu-id="e448b-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e448b-107">依標題取得</span><span class="sxs-lookup"><span data-stu-id="e448b-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e448b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e448b-108">DESCRIPTION</span></span>
<span data-ttu-id="e448b-109">**AzureRmApiManagementProduct** Cmdlet 會取得清單或特定產品。</span><span class="sxs-lookup"><span data-stu-id="e448b-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="e448b-110">示例</span><span class="sxs-lookup"><span data-stu-id="e448b-110">EXAMPLES</span></span>

### <span data-ttu-id="e448b-111">範例1：取得所有產品</span><span class="sxs-lookup"><span data-stu-id="e448b-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="e448b-112">這個命令會取得所有 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="e448b-112">This command get all API Management products.</span></span>

### <span data-ttu-id="e448b-113">範例2：依識別碼取得產品</span><span class="sxs-lookup"><span data-stu-id="e448b-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="e448b-114">這個命令會透過識別碼取得 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="e448b-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="e448b-115">參數</span><span class="sxs-lookup"><span data-stu-id="e448b-115">PARAMETERS</span></span>

### <span data-ttu-id="e448b-116">-內容</span><span class="sxs-lookup"><span data-stu-id="e448b-116">-Context</span></span>
<span data-ttu-id="e448b-117">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e448b-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e448b-118">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="e448b-118">-ProductId</span></span>
<span data-ttu-id="e448b-119">指定要搜尋的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="e448b-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e448b-120">-標題</span><span class="sxs-lookup"><span data-stu-id="e448b-120">-Title</span></span>
<span data-ttu-id="e448b-121">指定要尋找之產品的標題。</span><span class="sxs-lookup"><span data-stu-id="e448b-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="e448b-122">如果已指定，此 Cmdlet 會嘗試透過標題取得產品。</span><span class="sxs-lookup"><span data-stu-id="e448b-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e448b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e448b-123">-DefaultProfile</span></span>
<span data-ttu-id="e448b-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e448b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e448b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e448b-125">CommonParameters</span></span>
<span data-ttu-id="e448b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e448b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e448b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e448b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e448b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e448b-128">INPUTS</span></span>

## <span data-ttu-id="e448b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e448b-129">OUTPUTS</span></span>

### <span data-ttu-id="e448b-130">IList<ApiManagement. ServiceManagement. PsApiManagementProduct]></span><span class="sxs-lookup"><span data-stu-id="e448b-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="e448b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e448b-131">NOTES</span></span>

## <span data-ttu-id="e448b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e448b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e448b-133">新-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e448b-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e448b-134">移除-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e448b-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e448b-135">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e448b-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


