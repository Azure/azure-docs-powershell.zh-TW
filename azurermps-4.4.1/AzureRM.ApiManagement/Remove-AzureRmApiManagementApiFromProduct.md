---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 957a2fbecc588f9b04400571e587c6ba56e16df5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445207"
---
# <span data-ttu-id="1da64-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="1da64-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="1da64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1da64-102">SYNOPSIS</span></span>
<span data-ttu-id="1da64-103">從產品移除 API。</span><span class="sxs-lookup"><span data-stu-id="1da64-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da64-104">句法</span><span class="sxs-lookup"><span data-stu-id="1da64-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da64-105">說明</span><span class="sxs-lookup"><span data-stu-id="1da64-105">DESCRIPTION</span></span>
<span data-ttu-id="1da64-106">**AzureRmApiManagementApiFromProduct** Cmdlet 會從產品中移除 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="1da64-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="1da64-107">示例</span><span class="sxs-lookup"><span data-stu-id="1da64-107">EXAMPLES</span></span>

### <span data-ttu-id="1da64-108">範例1：從產品移除 API</span><span class="sxs-lookup"><span data-stu-id="1da64-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="1da64-109">此 commnd 會從產品中移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="1da64-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="1da64-110">參數</span><span class="sxs-lookup"><span data-stu-id="1da64-110">PARAMETERS</span></span>

### <span data-ttu-id="1da64-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1da64-111">-ApiId</span></span>
<span data-ttu-id="1da64-112">指定要從產品中移除的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1da64-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="1da64-113">-內容</span><span class="sxs-lookup"><span data-stu-id="1da64-113">-Context</span></span>
<span data-ttu-id="1da64-114">指定 **PsApiManagementCoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="1da64-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1da64-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1da64-115">-PassThru</span></span>
<span data-ttu-id="1da64-116">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="1da64-116">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="1da64-117">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="1da64-117">-ProductId</span></span>
<span data-ttu-id="1da64-118">指定要從中移除 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="1da64-118">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="1da64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da64-119">-DefaultProfile</span></span>
<span data-ttu-id="1da64-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1da64-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da64-121">CommonParameters</span></span>
<span data-ttu-id="1da64-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1da64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da64-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1da64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da64-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1da64-124">INPUTS</span></span>

## <span data-ttu-id="1da64-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1da64-125">OUTPUTS</span></span>

### <span data-ttu-id="1da64-126">bool</span><span class="sxs-lookup"><span data-stu-id="1da64-126">bool</span></span>

## <span data-ttu-id="1da64-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1da64-127">NOTES</span></span>

## <span data-ttu-id="1da64-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="1da64-128">RELATED LINKS</span></span>

[<span data-ttu-id="1da64-129">附加 AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="1da64-129">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


