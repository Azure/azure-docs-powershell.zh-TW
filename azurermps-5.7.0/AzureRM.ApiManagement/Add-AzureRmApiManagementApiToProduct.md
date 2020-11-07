---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624512"
---
# <span data-ttu-id="1bdc2-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="1bdc2-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="1bdc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bdc2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bdc2-103">在產品中加入 API。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bdc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bdc2-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bdc2-105">說明</span><span class="sxs-lookup"><span data-stu-id="1bdc2-105">DESCRIPTION</span></span>
<span data-ttu-id="1bdc2-106">**AzureRmApiManagementApiToProduct** Cmdlet 會將 Azure API 管理 API 新增至產品。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="1bdc2-107">示例</span><span class="sxs-lookup"><span data-stu-id="1bdc2-107">EXAMPLES</span></span>

### <span data-ttu-id="1bdc2-108">範例1：新增 API 至產品</span><span class="sxs-lookup"><span data-stu-id="1bdc2-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="1bdc2-109">這個命令會將指定的 API 新增至指定的產品。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="1bdc2-110">參數</span><span class="sxs-lookup"><span data-stu-id="1bdc2-110">PARAMETERS</span></span>

### <span data-ttu-id="1bdc2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1bdc2-111">-ApiId</span></span>
<span data-ttu-id="1bdc2-112">指定要新增至產品的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bdc2-113">-內容</span><span class="sxs-lookup"><span data-stu-id="1bdc2-113">-Context</span></span>
<span data-ttu-id="1bdc2-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1bdc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bdc2-115">-DefaultProfile</span></span>
<span data-ttu-id="1bdc2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bdc2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bdc2-117">-PassThru</span></span>
<span data-ttu-id="1bdc2-118">passthru</span><span class="sxs-lookup"><span data-stu-id="1bdc2-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bdc2-119">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="1bdc2-119">-ProductId</span></span>
<span data-ttu-id="1bdc2-120">指定要新增 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bdc2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bdc2-121">CommonParameters</span></span>
<span data-ttu-id="1bdc2-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bdc2-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bdc2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1bdc2-124">INPUTS</span></span>

### <span data-ttu-id="1bdc2-125">所有</span><span class="sxs-lookup"><span data-stu-id="1bdc2-125">None</span></span>
<span data-ttu-id="1bdc2-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1bdc2-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1bdc2-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1bdc2-127">OUTPUTS</span></span>

### <span data-ttu-id="1bdc2-128">布林值</span><span class="sxs-lookup"><span data-stu-id="1bdc2-128">Boolean</span></span>

## <span data-ttu-id="1bdc2-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1bdc2-129">NOTES</span></span>

## <span data-ttu-id="1bdc2-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bdc2-130">RELATED LINKS</span></span>

[<span data-ttu-id="1bdc2-131">移除-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="1bdc2-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


