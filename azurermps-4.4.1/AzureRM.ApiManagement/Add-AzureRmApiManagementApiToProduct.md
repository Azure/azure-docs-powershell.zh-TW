---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: d5c9061921f6ab345a027eeec69b4d6cd7230211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624861"
---
# <span data-ttu-id="ccf53-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="ccf53-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="ccf53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccf53-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf53-103">在產品中加入 API。</span><span class="sxs-lookup"><span data-stu-id="ccf53-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccf53-104">句法</span><span class="sxs-lookup"><span data-stu-id="ccf53-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf53-105">說明</span><span class="sxs-lookup"><span data-stu-id="ccf53-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf53-106">**AzureRmApiManagementApiToProduct** Cmdlet 會將 Azure API 管理 API 新增至產品。</span><span class="sxs-lookup"><span data-stu-id="ccf53-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="ccf53-107">示例</span><span class="sxs-lookup"><span data-stu-id="ccf53-107">EXAMPLES</span></span>

### <span data-ttu-id="ccf53-108">範例1：新增 API 至產品</span><span class="sxs-lookup"><span data-stu-id="ccf53-108">Example 1: Add an API to a product</span></span>
```
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="ccf53-109">這個命令會將指定的 API 新增至指定的產品。</span><span class="sxs-lookup"><span data-stu-id="ccf53-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="ccf53-110">參數</span><span class="sxs-lookup"><span data-stu-id="ccf53-110">PARAMETERS</span></span>

### <span data-ttu-id="ccf53-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ccf53-111">-ApiId</span></span>
<span data-ttu-id="ccf53-112">指定要新增至產品的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccf53-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf53-113">-內容</span><span class="sxs-lookup"><span data-stu-id="ccf53-113">-Context</span></span>
<span data-ttu-id="ccf53-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="ccf53-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ccf53-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccf53-115">-PassThru</span></span>
<span data-ttu-id="ccf53-116">passthru</span><span class="sxs-lookup"><span data-stu-id="ccf53-116">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf53-117">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="ccf53-117">-ProductId</span></span>
<span data-ttu-id="ccf53-118">指定要新增 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccf53-118">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf53-119">-DefaultProfile</span></span>
<span data-ttu-id="ccf53-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccf53-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccf53-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf53-121">CommonParameters</span></span>
<span data-ttu-id="ccf53-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccf53-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf53-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ccf53-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf53-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ccf53-124">INPUTS</span></span>

## <span data-ttu-id="ccf53-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ccf53-125">OUTPUTS</span></span>

### <span data-ttu-id="ccf53-126">布林值</span><span class="sxs-lookup"><span data-stu-id="ccf53-126">Boolean</span></span>

## <span data-ttu-id="ccf53-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ccf53-127">NOTES</span></span>

## <span data-ttu-id="ccf53-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccf53-128">RELATED LINKS</span></span>

[<span data-ttu-id="ccf53-129">移除-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="ccf53-129">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


