---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956729"
---
# <span data-ttu-id="dfb67-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="dfb67-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="dfb67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfb67-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb67-103">取得訂閱的使用量配額。</span><span class="sxs-lookup"><span data-stu-id="dfb67-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="dfb67-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfb67-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfb67-105">說明</span><span class="sxs-lookup"><span data-stu-id="dfb67-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb67-106">取得訂閱的使用量配額。</span><span class="sxs-lookup"><span data-stu-id="dfb67-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="dfb67-107">示例</span><span class="sxs-lookup"><span data-stu-id="dfb67-107">EXAMPLES</span></span>

### <span data-ttu-id="dfb67-108">透過輸入位置來取得使用量配額</span><span class="sxs-lookup"><span data-stu-id="dfb67-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="dfb67-109">參數</span><span class="sxs-lookup"><span data-stu-id="dfb67-109">PARAMETERS</span></span>

### <span data-ttu-id="dfb67-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb67-110">-DefaultProfile</span></span>
<span data-ttu-id="dfb67-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfb67-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb67-112">-位置</span><span class="sxs-lookup"><span data-stu-id="dfb67-112">-Location</span></span>
<span data-ttu-id="dfb67-113">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="dfb67-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb67-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb67-114">CommonParameters</span></span>
<span data-ttu-id="dfb67-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfb67-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb67-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfb67-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb67-117">輸入</span><span class="sxs-lookup"><span data-stu-id="dfb67-117">INPUTS</span></span>

### <span data-ttu-id="dfb67-118">所有</span><span class="sxs-lookup"><span data-stu-id="dfb67-118">None</span></span>

## <span data-ttu-id="dfb67-119">輸出</span><span class="sxs-lookup"><span data-stu-id="dfb67-119">OUTPUTS</span></span>

### <span data-ttu-id="dfb67-120">PSSignalRUsage 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="dfb67-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="dfb67-121">筆記</span><span class="sxs-lookup"><span data-stu-id="dfb67-121">NOTES</span></span>

## <span data-ttu-id="dfb67-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfb67-122">RELATED LINKS</span></span>