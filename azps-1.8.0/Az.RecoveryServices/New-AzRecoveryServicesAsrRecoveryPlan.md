---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5e0c3627616ae7310785943f73ed7c07f0f263b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621105"
---
# <span data-ttu-id="b39ad-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b39ad-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b39ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b39ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b39ad-103">建立 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="b39ad-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="b39ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="b39ad-104">SYNTAX</span></span>

### <span data-ttu-id="b39ad-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="b39ad-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b39ad-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b39ad-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b39ad-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b39ad-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b39ad-108">說明</span><span class="sxs-lookup"><span data-stu-id="b39ad-108">DESCRIPTION</span></span>
<span data-ttu-id="b39ad-109">**新的-AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會在 [復原服務] 保存庫中建立 Azure Site recovery 復原方案。</span><span class="sxs-lookup"><span data-stu-id="b39ad-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="b39ad-110">復原方案會將屬於應用程式的虛擬機器收集到單元中，讓它們能夠一起復原。</span><span class="sxs-lookup"><span data-stu-id="b39ad-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="b39ad-111">示例</span><span class="sxs-lookup"><span data-stu-id="b39ad-111">EXAMPLES</span></span>

### <span data-ttu-id="b39ad-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b39ad-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b39ad-113">使用指定的參數啟動復原方案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="b39ad-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b39ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="b39ad-114">PARAMETERS</span></span>

### <span data-ttu-id="b39ad-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="b39ad-115">-Azure</span></span>
<span data-ttu-id="b39ad-116">{{Fill Azure 說明}}</span><span class="sxs-lookup"><span data-stu-id="b39ad-116">{{Fill Azure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39ad-117">-DefaultProfile</span></span>
<span data-ttu-id="b39ad-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b39ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b39ad-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="b39ad-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="b39ad-120">指定將成為此復原方案一部分之複製受保護專案 (傳統或資源管理員) 的容錯移轉部署模型。</span><span class="sxs-lookup"><span data-stu-id="b39ad-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b39ad-121">-Name</span></span>
<span data-ttu-id="b39ad-122">修復方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="b39ad-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-123">-Path</span><span class="sxs-lookup"><span data-stu-id="b39ad-123">-Path</span></span>
<span data-ttu-id="b39ad-124">指定恢復方案定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b39ad-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="b39ad-125">復原方案定義 json 可以用來建立復原方案。</span><span class="sxs-lookup"><span data-stu-id="b39ad-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="b39ad-126">-PrimaryFabric</span></span>
<span data-ttu-id="b39ad-127">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件的初始 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="b39ad-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b39ad-128">-RecoveryFabric</span></span>
<span data-ttu-id="b39ad-129">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件來取得恢復 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="b39ad-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b39ad-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b39ad-131">要新增至第一個恢復方案群組的複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="b39ad-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b39ad-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b39ad-132">-Confirm</span></span>
<span data-ttu-id="b39ad-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b39ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b39ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b39ad-134">-WhatIf</span></span>
<span data-ttu-id="b39ad-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b39ad-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b39ad-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b39ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b39ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39ad-137">CommonParameters</span></span>
<span data-ttu-id="b39ad-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b39ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39ad-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b39ad-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39ad-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b39ad-140">INPUTS</span></span>

### <span data-ttu-id="b39ad-141">ASRReplicationProtectedItem []. RecoveryServices. SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b39ad-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="b39ad-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b39ad-142">OUTPUTS</span></span>

### <span data-ttu-id="b39ad-143">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b39ad-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b39ad-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b39ad-144">NOTES</span></span>

## <span data-ttu-id="b39ad-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b39ad-145">RELATED LINKS</span></span>

[<span data-ttu-id="b39ad-146">AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b39ad-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b39ad-147">移除-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b39ad-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b39ad-148">更新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b39ad-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


