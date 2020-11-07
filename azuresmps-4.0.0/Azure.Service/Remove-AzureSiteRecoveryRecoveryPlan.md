---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967557"
---
# <span data-ttu-id="4fe13-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fe13-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="4fe13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fe13-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe13-103">從網站復原中移除網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="4fe13-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="4fe13-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fe13-104">SYNTAX</span></span>

### <span data-ttu-id="4fe13-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="4fe13-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe13-106">ById</span><span class="sxs-lookup"><span data-stu-id="4fe13-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe13-107">說明</span><span class="sxs-lookup"><span data-stu-id="4fe13-107">DESCRIPTION</span></span>
<span data-ttu-id="4fe13-108">**AzureSiteRecoveryRecoveryPlan** Cmdlet 會從目前的 Azure site recovery 中移除網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="4fe13-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="4fe13-109">示例</span><span class="sxs-lookup"><span data-stu-id="4fe13-109">EXAMPLES</span></span>

### <span data-ttu-id="4fe13-110">範例1：移除恢復方案</span><span class="sxs-lookup"><span data-stu-id="4fe13-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="4fe13-111">第一個命令使用 **AzureSiteRecoveryRecoveryPlan** Cmdlet 來取得網站復原方案，然後將它儲存在 $RecoveryPlan 變數中。</span><span class="sxs-lookup"><span data-stu-id="4fe13-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="4fe13-112">第二個命令會在 $RecoveryPlan 中移除復原方案。</span><span class="sxs-lookup"><span data-stu-id="4fe13-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="4fe13-113">參數</span><span class="sxs-lookup"><span data-stu-id="4fe13-113">PARAMETERS</span></span>

### <span data-ttu-id="4fe13-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4fe13-114">-Force</span></span>
<span data-ttu-id="4fe13-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4fe13-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4fe13-116">-Id</span></span>
<span data-ttu-id="4fe13-117">指定要移除的復原方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fe13-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4fe13-118">-Profile</span></span>
<span data-ttu-id="4fe13-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4fe13-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4fe13-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4fe13-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fe13-121">-RecoveryPlan</span></span>
<span data-ttu-id="4fe13-122">指定要移除的復原方案。</span><span class="sxs-lookup"><span data-stu-id="4fe13-122">Specifies the recovery plan to remove.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4fe13-123">-WaitForCompletion</span></span>
<span data-ttu-id="4fe13-124">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="4fe13-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4fe13-125">-Confirm</span></span>
<span data-ttu-id="4fe13-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4fe13-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe13-127">-WhatIf</span></span>
<span data-ttu-id="4fe13-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fe13-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fe13-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fe13-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe13-130">CommonParameters</span></span>
<span data-ttu-id="4fe13-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fe13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe13-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fe13-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe13-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4fe13-133">INPUTS</span></span>

## <span data-ttu-id="4fe13-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4fe13-134">OUTPUTS</span></span>

## <span data-ttu-id="4fe13-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4fe13-135">NOTES</span></span>

## <span data-ttu-id="4fe13-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fe13-136">RELATED LINKS</span></span>

[<span data-ttu-id="4fe13-137">AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fe13-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4fe13-138">新-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fe13-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4fe13-139">更新-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fe13-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


