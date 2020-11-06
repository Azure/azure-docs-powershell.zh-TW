---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455875"
---
# <span data-ttu-id="f954b-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="f954b-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="f954b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f954b-102">SYNOPSIS</span></span>
<span data-ttu-id="f954b-103">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="f954b-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f954b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f954b-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f954b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f954b-105">DESCRIPTION</span></span>
<span data-ttu-id="f954b-106">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="f954b-106">List all compute resource Skus</span></span>

## <span data-ttu-id="f954b-107">示例</span><span class="sxs-lookup"><span data-stu-id="f954b-107">EXAMPLES</span></span>

### <span data-ttu-id="f954b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f954b-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="f954b-109">列出西部美國地區的所有計算資源 sku</span><span class="sxs-lookup"><span data-stu-id="f954b-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="f954b-110">參數</span><span class="sxs-lookup"><span data-stu-id="f954b-110">PARAMETERS</span></span>

### <span data-ttu-id="f954b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f954b-111">-DefaultProfile</span></span>
<span data-ttu-id="f954b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f954b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f954b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f954b-113">CommonParameters</span></span>
<span data-ttu-id="f954b-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f954b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f954b-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f954b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f954b-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f954b-116">INPUTS</span></span>

### <span data-ttu-id="f954b-117">所有</span><span class="sxs-lookup"><span data-stu-id="f954b-117">None</span></span>

## <span data-ttu-id="f954b-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f954b-118">OUTPUTS</span></span>

### <span data-ttu-id="f954b-119">System.object</span><span class="sxs-lookup"><span data-stu-id="f954b-119">System.Object</span></span>

## <span data-ttu-id="f954b-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f954b-120">NOTES</span></span>

## <span data-ttu-id="f954b-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f954b-121">RELATED LINKS</span></span>

