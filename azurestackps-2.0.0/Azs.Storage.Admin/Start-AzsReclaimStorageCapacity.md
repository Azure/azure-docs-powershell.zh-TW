---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794850"
---
# <span data-ttu-id="0b5fe-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="0b5fe-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="0b5fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b5fe-102">SYNOPSIS</span></span>


## <span data-ttu-id="0b5fe-103">句法</span><span class="sxs-lookup"><span data-stu-id="0b5fe-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b5fe-104">說明</span><span class="sxs-lookup"><span data-stu-id="0b5fe-104">DESCRIPTION</span></span>


## <span data-ttu-id="0b5fe-105">示例</span><span class="sxs-lookup"><span data-stu-id="0b5fe-105">EXAMPLES</span></span>

### <span data-ttu-id="0b5fe-106">範例1：</span><span class="sxs-lookup"><span data-stu-id="0b5fe-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="0b5fe-107">啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="0b5fe-107">Start garbage collection.</span></span>

## <span data-ttu-id="0b5fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="0b5fe-108">PARAMETERS</span></span>

### <span data-ttu-id="0b5fe-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b5fe-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5fe-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0b5fe-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-112">-位置</span><span class="sxs-lookup"><span data-stu-id="0b5fe-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-113">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0b5fe-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b5fe-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b5fe-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-116">-確認</span><span class="sxs-lookup"><span data-stu-id="0b5fe-116">-Confirm</span></span>
<span data-ttu-id="0b5fe-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b5fe-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5fe-118">-WhatIf</span></span>
<span data-ttu-id="0b5fe-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b5fe-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b5fe-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b5fe-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0b5fe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5fe-121">CommonParameters</span></span>
<span data-ttu-id="0b5fe-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b5fe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5fe-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b5fe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5fe-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0b5fe-124">INPUTS</span></span>

## <span data-ttu-id="0b5fe-125">輸出</span><span class="sxs-lookup"><span data-stu-id="0b5fe-125">OUTPUTS</span></span>

### <span data-ttu-id="0b5fe-126">System.object</span><span class="sxs-lookup"><span data-stu-id="0b5fe-126">System.Boolean</span></span>



## <span data-ttu-id="0b5fe-127">筆記</span><span class="sxs-lookup"><span data-stu-id="0b5fe-127">NOTES</span></span>

## <span data-ttu-id="0b5fe-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b5fe-128">RELATED LINKS</span></span>

