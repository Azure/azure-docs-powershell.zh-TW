---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 297b862cb9491c0659d5fd2ec5ab0da4fc071e4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903674"
---
# <span data-ttu-id="930e8-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="930e8-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="930e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="930e8-102">SYNOPSIS</span></span>
<span data-ttu-id="930e8-103">在指定位置獲得訂閱的批次服務配額。</span><span class="sxs-lookup"><span data-stu-id="930e8-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="930e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="930e8-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="930e8-105">描述</span><span class="sxs-lookup"><span data-stu-id="930e8-105">DESCRIPTION</span></span>
<span data-ttu-id="930e8-106">在指定的位置上，獲得指定訂閱的批次服務配額。</span><span class="sxs-lookup"><span data-stu-id="930e8-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="930e8-107">例子</span><span class="sxs-lookup"><span data-stu-id="930e8-107">EXAMPLES</span></span>

### <span data-ttu-id="930e8-108">範例 1：取得美國西部地區訂閱的批次服務配額</span><span class="sxs-lookup"><span data-stu-id="930e8-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="930e8-109">此命令會獲得美國西部地區目前訂閱的配額。</span><span class="sxs-lookup"><span data-stu-id="930e8-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="930e8-110">退貨值表示此訂閱只能在該地區建立一個批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="930e8-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="930e8-111">參數</span><span class="sxs-lookup"><span data-stu-id="930e8-111">PARAMETERS</span></span>

### <span data-ttu-id="930e8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930e8-112">-DefaultProfile</span></span>
<span data-ttu-id="930e8-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="930e8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930e8-114">-位置</span><span class="sxs-lookup"><span data-stu-id="930e8-114">-Location</span></span>
<span data-ttu-id="930e8-115">指定此 Cmdlet 會檢查配額的區域。</span><span class="sxs-lookup"><span data-stu-id="930e8-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="930e8-116">詳細資訊請參閱 Azure 區域 https://azure.microsoft.com/regions) (。</span><span class="sxs-lookup"><span data-stu-id="930e8-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930e8-117">CommonParameters</span></span>
<span data-ttu-id="930e8-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="930e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930e8-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="930e8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930e8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="930e8-120">INPUTS</span></span>

### <span data-ttu-id="930e8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="930e8-121">System.String</span></span>

## <span data-ttu-id="930e8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="930e8-122">OUTPUTS</span></span>

### <span data-ttu-id="930e8-123">Microsoft.Azure.Commands.Batch。Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="930e8-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="930e8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="930e8-124">NOTES</span></span>

## <span data-ttu-id="930e8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="930e8-125">RELATED LINKS</span></span>
