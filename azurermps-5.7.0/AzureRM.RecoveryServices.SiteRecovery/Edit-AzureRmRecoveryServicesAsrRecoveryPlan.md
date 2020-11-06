---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 289804771010a586b73621ec5df81805ed30ae55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452108"
---
# <span data-ttu-id="17834-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="17834-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="17834-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17834-102">SYNOPSIS</span></span>
<span data-ttu-id="17834-103">編輯網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="17834-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17834-104">句法</span><span class="sxs-lookup"><span data-stu-id="17834-104">SYNTAX</span></span>

### <span data-ttu-id="17834-105">AppendGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="17834-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17834-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="17834-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17834-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="17834-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17834-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="17834-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17834-109">說明</span><span class="sxs-lookup"><span data-stu-id="17834-109">DESCRIPTION</span></span>
<span data-ttu-id="17834-110">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 編輯 Azure 網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="17834-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="17834-111">示例</span><span class="sxs-lookup"><span data-stu-id="17834-111">EXAMPLES</span></span>

### <span data-ttu-id="17834-112">範例1</span><span class="sxs-lookup"><span data-stu-id="17834-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="17834-113">將群組附加至現有的 Azure 網站復原復原方案，並傳回記憶體更新的復原方案。</span><span class="sxs-lookup"><span data-stu-id="17834-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="17834-114">參數</span><span class="sxs-lookup"><span data-stu-id="17834-114">PARAMETERS</span></span>

### <span data-ttu-id="17834-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="17834-115">-AddProtectedItem</span></span>
<span data-ttu-id="17834-116">要新增到復原方案物件之復原方案群組的 ASR 複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="17834-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="17834-117">-AppendGroup</span></span>
<span data-ttu-id="17834-118">[切換參數]，將復原方案群組附加到復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="17834-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-119">-確認</span><span class="sxs-lookup"><span data-stu-id="17834-119">-Confirm</span></span>
<span data-ttu-id="17834-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17834-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17834-121">-DefaultProfile</span></span>
<span data-ttu-id="17834-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17834-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-123">-群組</span><span class="sxs-lookup"><span data-stu-id="17834-123">-Group</span></span>
<span data-ttu-id="17834-124">指定復原方案群組。</span><span class="sxs-lookup"><span data-stu-id="17834-124">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17834-125">-InputObject</span></span>
<span data-ttu-id="17834-126">要在記憶體作業中 (編輯的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="17834-126">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="17834-127">若要更新復原方案，請執行 Update-AzureRmASRRecoveryPlan 與已編輯的復原方案物件。 ) </span><span class="sxs-lookup"><span data-stu-id="17834-127">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17834-128">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="17834-128">-RemoveGroup</span></span>
<span data-ttu-id="17834-129">從復原方案物件中移除指定的群組。</span><span class="sxs-lookup"><span data-stu-id="17834-129">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-130">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="17834-130">-RemoveProtectedItem</span></span>
<span data-ttu-id="17834-131">要從復原方案物件的復原方案群組中移除的 ASR 複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="17834-131">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17834-132">-WhatIf</span></span>
<span data-ttu-id="17834-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17834-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17834-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17834-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17834-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17834-135">CommonParameters</span></span>
<span data-ttu-id="17834-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17834-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17834-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17834-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17834-138">輸入</span><span class="sxs-lookup"><span data-stu-id="17834-138">INPUTS</span></span>

### <span data-ttu-id="17834-139">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="17834-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="17834-140">輸出</span><span class="sxs-lookup"><span data-stu-id="17834-140">OUTPUTS</span></span>

### <span data-ttu-id="17834-141">System.object</span><span class="sxs-lookup"><span data-stu-id="17834-141">System.Object</span></span>

## <span data-ttu-id="17834-142">筆記</span><span class="sxs-lookup"><span data-stu-id="17834-142">NOTES</span></span>

## <span data-ttu-id="17834-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="17834-143">RELATED LINKS</span></span>

[<span data-ttu-id="17834-144">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="17834-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="17834-145">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="17834-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
