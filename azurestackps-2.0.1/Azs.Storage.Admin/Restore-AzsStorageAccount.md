---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2020
ms.locfileid: "93966833"
---
# <span data-ttu-id="3dc1f-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3dc1f-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="3dc1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dc1f-102">SYNOPSIS</span></span>


## <span data-ttu-id="3dc1f-103">句法</span><span class="sxs-lookup"><span data-stu-id="3dc1f-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3dc1f-104">說明</span><span class="sxs-lookup"><span data-stu-id="3dc1f-104">DESCRIPTION</span></span>


## <span data-ttu-id="3dc1f-105">示例</span><span class="sxs-lookup"><span data-stu-id="3dc1f-105">EXAMPLES</span></span>

### <span data-ttu-id="3dc1f-106">範例1：</span><span class="sxs-lookup"><span data-stu-id="3dc1f-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="3dc1f-107">取消刪除已刪除的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="3dc1f-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="3dc1f-108">參數</span><span class="sxs-lookup"><span data-stu-id="3dc1f-108">PARAMETERS</span></span>

### <span data-ttu-id="3dc1f-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dc1f-109">-AsJob</span></span>


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

### <span data-ttu-id="3dc1f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc1f-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="3dc1f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3dc1f-111">-Force</span></span>


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

### <span data-ttu-id="3dc1f-112">-位置</span><span class="sxs-lookup"><span data-stu-id="3dc1f-112">-Location</span></span>


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

### <span data-ttu-id="3dc1f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3dc1f-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3dc1f-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="3dc1f-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3dc1f-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3dc1f-115">-NoWait</span></span>


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

### <span data-ttu-id="3dc1f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dc1f-116">-PassThru</span></span>


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

### <span data-ttu-id="3dc1f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3dc1f-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="3dc1f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="3dc1f-118">-Confirm</span></span>
<span data-ttu-id="3dc1f-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3dc1f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc1f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc1f-120">-WhatIf</span></span>
<span data-ttu-id="3dc1f-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dc1f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc1f-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dc1f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc1f-123">CommonParameters</span></span>
<span data-ttu-id="3dc1f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dc1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc1f-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3dc1f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc1f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3dc1f-126">INPUTS</span></span>

## <span data-ttu-id="3dc1f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3dc1f-127">OUTPUTS</span></span>

### <span data-ttu-id="3dc1f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="3dc1f-128">System.Boolean</span></span>



## <span data-ttu-id="3dc1f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3dc1f-129">NOTES</span></span>

## <span data-ttu-id="3dc1f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dc1f-130">RELATED LINKS</span></span>

