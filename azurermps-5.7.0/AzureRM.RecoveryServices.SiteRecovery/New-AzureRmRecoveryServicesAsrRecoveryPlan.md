---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: e9edfb1654e623b023a075cb462fedfbd9442756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447703"
---
# <span data-ttu-id="6ae78-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ae78-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6ae78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ae78-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae78-103">建立 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="6ae78-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ae78-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ae78-104">SYNTAX</span></span>

### <span data-ttu-id="6ae78-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="6ae78-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ae78-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6ae78-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ae78-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6ae78-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ae78-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ae78-108">DESCRIPTION</span></span>
<span data-ttu-id="6ae78-109">**新的-AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 會在 [復原服務] 保存庫中建立 Azure Site recovery 復原方案。</span><span class="sxs-lookup"><span data-stu-id="6ae78-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="6ae78-110">復原方案會將屬於應用程式的虛擬機器收集到單元中，讓它們能夠一起復原。</span><span class="sxs-lookup"><span data-stu-id="6ae78-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="6ae78-111">示例</span><span class="sxs-lookup"><span data-stu-id="6ae78-111">EXAMPLES</span></span>

### <span data-ttu-id="6ae78-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6ae78-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="6ae78-113">使用指定的參數啟動復原方案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="6ae78-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6ae78-114">參數</span><span class="sxs-lookup"><span data-stu-id="6ae78-114">PARAMETERS</span></span>

### <span data-ttu-id="6ae78-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="6ae78-115">-Azure</span></span>
<span data-ttu-id="6ae78-116">切換參數，以指定修復方案的復原位置是 Azure。</span><span class="sxs-lookup"><span data-stu-id="6ae78-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

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

### <span data-ttu-id="6ae78-117">-確認</span><span class="sxs-lookup"><span data-stu-id="6ae78-117">-Confirm</span></span>
<span data-ttu-id="6ae78-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ae78-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ae78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae78-119">-DefaultProfile</span></span>
<span data-ttu-id="6ae78-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ae78-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="6ae78-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="6ae78-121">-FailoverDeploymentModel</span></span>
<span data-ttu-id="6ae78-122">指定將成為此復原方案一部分之複製受保護專案 (傳統或資源管理員) 的容錯移轉部署模型。</span><span class="sxs-lookup"><span data-stu-id="6ae78-122">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="6ae78-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ae78-123">-Name</span></span>
<span data-ttu-id="6ae78-124">修復方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ae78-124">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="6ae78-125">-Path</span><span class="sxs-lookup"><span data-stu-id="6ae78-125">-Path</span></span>
<span data-ttu-id="6ae78-126">指定恢復方案定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6ae78-126">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="6ae78-127">復原方案定義 json 可以用來建立復原方案。</span><span class="sxs-lookup"><span data-stu-id="6ae78-127">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="6ae78-128">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="6ae78-128">-PrimaryFabric</span></span>
<span data-ttu-id="6ae78-129">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件的初始 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="6ae78-129">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="6ae78-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6ae78-130">-RecoveryFabric</span></span>
<span data-ttu-id="6ae78-131">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件來取得恢復 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="6ae78-131">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="6ae78-132">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6ae78-132">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6ae78-133">要新增至第一個恢復方案群組的複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="6ae78-133">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="6ae78-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae78-134">-WhatIf</span></span>
<span data-ttu-id="6ae78-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ae78-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ae78-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ae78-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ae78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae78-137">CommonParameters</span></span>
<span data-ttu-id="6ae78-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ae78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae78-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ae78-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae78-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6ae78-140">INPUTS</span></span>

### <span data-ttu-id="6ae78-141">ASRReplicationProtectedItem []. RecoveryServices. SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6ae78-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="6ae78-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6ae78-142">OUTPUTS</span></span>

### <span data-ttu-id="6ae78-143">System.object</span><span class="sxs-lookup"><span data-stu-id="6ae78-143">System.Object</span></span>

## <span data-ttu-id="6ae78-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6ae78-144">NOTES</span></span>

## <span data-ttu-id="6ae78-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ae78-145">RELATED LINKS</span></span>

[<span data-ttu-id="6ae78-146">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ae78-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6ae78-147">移除-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ae78-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6ae78-148">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ae78-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


