---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2020
ms.locfileid: "93966835"
---
# <span data-ttu-id="17c6d-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="17c6d-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="17c6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17c6d-102">SYNOPSIS</span></span>


## <span data-ttu-id="17c6d-103">句法</span><span class="sxs-lookup"><span data-stu-id="17c6d-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17c6d-104">說明</span><span class="sxs-lookup"><span data-stu-id="17c6d-104">DESCRIPTION</span></span>


## <span data-ttu-id="17c6d-105">示例</span><span class="sxs-lookup"><span data-stu-id="17c6d-105">EXAMPLES</span></span>

### <span data-ttu-id="17c6d-106">範例1：</span><span class="sxs-lookup"><span data-stu-id="17c6d-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="17c6d-107">更新儲存設定。</span><span class="sxs-lookup"><span data-stu-id="17c6d-107">Update the storage settings.</span></span>

## <span data-ttu-id="17c6d-108">參數</span><span class="sxs-lookup"><span data-stu-id="17c6d-108">PARAMETERS</span></span>

### <span data-ttu-id="17c6d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c6d-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="17c6d-110">-Force</span><span class="sxs-lookup"><span data-stu-id="17c6d-110">-Force</span></span>


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

### <span data-ttu-id="17c6d-111">-位置</span><span class="sxs-lookup"><span data-stu-id="17c6d-111">-Location</span></span>


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

### <span data-ttu-id="17c6d-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="17c6d-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17c6d-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17c6d-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="17c6d-114">-確認</span><span class="sxs-lookup"><span data-stu-id="17c6d-114">-Confirm</span></span>
<span data-ttu-id="17c6d-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17c6d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17c6d-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17c6d-116">-WhatIf</span></span>
<span data-ttu-id="17c6d-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17c6d-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17c6d-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17c6d-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17c6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c6d-119">CommonParameters</span></span>
<span data-ttu-id="17c6d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17c6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c6d-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17c6d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c6d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="17c6d-122">INPUTS</span></span>

## <span data-ttu-id="17c6d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="17c6d-123">OUTPUTS</span></span>

### <span data-ttu-id="17c6d-124">ISettings （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="17c6d-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="17c6d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="17c6d-125">NOTES</span></span>

## <span data-ttu-id="17c6d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="17c6d-126">RELATED LINKS</span></span>

