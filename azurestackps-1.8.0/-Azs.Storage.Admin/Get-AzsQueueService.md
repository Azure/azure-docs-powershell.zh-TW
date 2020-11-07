---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793741"
---
# <span data-ttu-id="f3142-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="f3142-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="f3142-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3142-102">SYNOPSIS</span></span>
<span data-ttu-id="f3142-103">傳回佇列服務。</span><span class="sxs-lookup"><span data-stu-id="f3142-103">Returns the queue service.</span></span>

## <span data-ttu-id="f3142-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3142-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3142-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3142-105">DESCRIPTION</span></span>
<span data-ttu-id="f3142-106">傳回佇列服務。</span><span class="sxs-lookup"><span data-stu-id="f3142-106">Returns the queue service.</span></span>

## <span data-ttu-id="f3142-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3142-107">EXAMPLES</span></span>

### <span data-ttu-id="f3142-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3142-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="f3142-109">取得佇列服務。</span><span class="sxs-lookup"><span data-stu-id="f3142-109">Get the queue service.</span></span>

## <span data-ttu-id="f3142-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3142-110">PARAMETERS</span></span>

### <span data-ttu-id="f3142-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="f3142-111">-FarmName</span></span>
<span data-ttu-id="f3142-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="f3142-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3142-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3142-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3142-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f3142-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3142-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3142-115">CommonParameters</span></span>
<span data-ttu-id="f3142-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3142-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3142-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3142-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3142-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f3142-118">INPUTS</span></span>

## <span data-ttu-id="f3142-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f3142-119">OUTPUTS</span></span>

### <span data-ttu-id="f3142-120">AzureStack （QueueService）的</span><span class="sxs-lookup"><span data-stu-id="f3142-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="f3142-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f3142-121">NOTES</span></span>

## <span data-ttu-id="f3142-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3142-122">RELATED LINKS</span></span>

