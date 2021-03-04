---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 16d528497532f026961941963049c61a470ad188
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902794"
---
# <span data-ttu-id="5850c-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="5850c-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="5850c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5850c-102">SYNOPSIS</span></span>
<span data-ttu-id="5850c-103">取得訂閱的使用配額。</span><span class="sxs-lookup"><span data-stu-id="5850c-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="5850c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5850c-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5850c-105">描述</span><span class="sxs-lookup"><span data-stu-id="5850c-105">DESCRIPTION</span></span>
<span data-ttu-id="5850c-106">取得訂閱的使用配額。</span><span class="sxs-lookup"><span data-stu-id="5850c-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="5850c-107">例子</span><span class="sxs-lookup"><span data-stu-id="5850c-107">EXAMPLES</span></span>

### <span data-ttu-id="5850c-108">輸入位置以取得使用量配額</span><span class="sxs-lookup"><span data-stu-id="5850c-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="5850c-109">參數</span><span class="sxs-lookup"><span data-stu-id="5850c-109">PARAMETERS</span></span>

### <span data-ttu-id="5850c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5850c-110">-DefaultProfile</span></span>
<span data-ttu-id="5850c-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5850c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5850c-112">-位置</span><span class="sxs-lookup"><span data-stu-id="5850c-112">-Location</span></span>
<span data-ttu-id="5850c-113">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="5850c-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="5850c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5850c-114">CommonParameters</span></span>
<span data-ttu-id="5850c-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5850c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5850c-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5850c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5850c-117">輸入</span><span class="sxs-lookup"><span data-stu-id="5850c-117">INPUTS</span></span>

### <span data-ttu-id="5850c-118">沒有</span><span class="sxs-lookup"><span data-stu-id="5850c-118">None</span></span>

## <span data-ttu-id="5850c-119">輸出</span><span class="sxs-lookup"><span data-stu-id="5850c-119">OUTPUTS</span></span>

### <span data-ttu-id="5850c-120">Microsoft.Azure.Commands.SignalR.models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="5850c-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="5850c-121">筆記</span><span class="sxs-lookup"><span data-stu-id="5850c-121">NOTES</span></span>

## <span data-ttu-id="5850c-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5850c-122">RELATED LINKS</span></span>
