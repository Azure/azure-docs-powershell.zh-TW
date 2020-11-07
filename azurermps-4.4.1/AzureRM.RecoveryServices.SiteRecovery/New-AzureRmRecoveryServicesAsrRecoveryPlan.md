---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623870"
---
# <span data-ttu-id="35083-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35083-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="35083-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35083-102">SYNOPSIS</span></span>
<span data-ttu-id="35083-103">建立 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="35083-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35083-104">句法</span><span class="sxs-lookup"><span data-stu-id="35083-104">SYNTAX</span></span>

### <span data-ttu-id="35083-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="35083-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35083-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="35083-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35083-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="35083-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35083-108">說明</span><span class="sxs-lookup"><span data-stu-id="35083-108">DESCRIPTION</span></span>
<span data-ttu-id="35083-109">**新的-AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 會在 [復原服務] 保存庫中建立 Azure Site recovery 復原方案。</span><span class="sxs-lookup"><span data-stu-id="35083-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="35083-110">復原方案會將屬於應用程式的虛擬機器收集到單元中，讓它們能夠一起復原。</span><span class="sxs-lookup"><span data-stu-id="35083-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="35083-111">示例</span><span class="sxs-lookup"><span data-stu-id="35083-111">EXAMPLES</span></span>

### <span data-ttu-id="35083-112">範例1</span><span class="sxs-lookup"><span data-stu-id="35083-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="35083-113">使用指定的參數啟動復原方案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="35083-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="35083-114">參數</span><span class="sxs-lookup"><span data-stu-id="35083-114">PARAMETERS</span></span>

### <span data-ttu-id="35083-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="35083-115">-Azure</span></span>
<span data-ttu-id="35083-116">切換參數，以指定修復方案的復原位置是 Azure。</span><span class="sxs-lookup"><span data-stu-id="35083-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35083-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="35083-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="35083-118">指定將成為此復原方案一部分之複製受保護專案 (傳統或資源管理員) 的容錯移轉部署模型。</span><span class="sxs-lookup"><span data-stu-id="35083-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35083-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="35083-119">-Name</span></span>
<span data-ttu-id="35083-120">修復方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="35083-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35083-121">-Path</span><span class="sxs-lookup"><span data-stu-id="35083-121">-Path</span></span>
<span data-ttu-id="35083-122">指定恢復方案定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="35083-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="35083-123">復原方案定義 json 可以用來建立復原方案。</span><span class="sxs-lookup"><span data-stu-id="35083-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35083-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="35083-124">-PrimaryFabric</span></span>
<span data-ttu-id="35083-125">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件的初始 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="35083-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35083-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="35083-126">-RecoveryFabric</span></span>
<span data-ttu-id="35083-127">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件來取得恢復 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="35083-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35083-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="35083-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="35083-129">要新增至第一個恢復方案群組的複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="35083-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35083-130">-確認</span><span class="sxs-lookup"><span data-stu-id="35083-130">-Confirm</span></span>
<span data-ttu-id="35083-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35083-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35083-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35083-132">-WhatIf</span></span>
<span data-ttu-id="35083-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35083-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35083-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35083-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35083-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35083-135">CommonParameters</span></span>
<span data-ttu-id="35083-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35083-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35083-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35083-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35083-138">輸入</span><span class="sxs-lookup"><span data-stu-id="35083-138">INPUTS</span></span>

### <span data-ttu-id="35083-139">ASRReplicationProtectedItem []. RecoveryServices. SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="35083-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="35083-140">輸出</span><span class="sxs-lookup"><span data-stu-id="35083-140">OUTPUTS</span></span>

### <span data-ttu-id="35083-141">System.object</span><span class="sxs-lookup"><span data-stu-id="35083-141">System.Object</span></span>

## <span data-ttu-id="35083-142">筆記</span><span class="sxs-lookup"><span data-stu-id="35083-142">NOTES</span></span>

## <span data-ttu-id="35083-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="35083-143">RELATED LINKS</span></span>

[<span data-ttu-id="35083-144">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35083-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="35083-145">移除-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35083-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="35083-146">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35083-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


