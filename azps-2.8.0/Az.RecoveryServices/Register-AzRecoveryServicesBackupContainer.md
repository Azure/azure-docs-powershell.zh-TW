---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: eeffbbd62a4c161b95004c6f4bd40d31fbd02517
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792358"
---
# <span data-ttu-id="7d6fd-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7d6fd-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="7d6fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6fd-103">這個命令可讓 Azure Backup 將資源轉換成備份容器，然後再將登錄到指定的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="7d6fd-104">然後，Azure 備份服務就可以在此容器中發現指定工作負荷類型的工作負荷，以備日後受到保護。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="7d6fd-105">句法</span><span class="sxs-lookup"><span data-stu-id="7d6fd-105">SYNTAX</span></span>

### <span data-ttu-id="7d6fd-106">註冊 (預設) </span><span class="sxs-lookup"><span data-stu-id="7d6fd-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6fd-107">于</span><span class="sxs-lookup"><span data-stu-id="7d6fd-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6fd-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d6fd-108">DESCRIPTION</span></span>
<span data-ttu-id="7d6fd-109">這個 Cmdlet 會使用特定 workloadType 註冊 AzureWorkloads 的 Azure VM。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="7d6fd-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d6fd-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6fd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7d6fd-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="7d6fd-112">這個 Cmdlet 會針對工作負荷 MSSQL 註冊 azure VM。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="7d6fd-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d6fd-113">PARAMETERS</span></span>

### <span data-ttu-id="7d6fd-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7d6fd-114">-BackupManagementType</span></span>
<span data-ttu-id="7d6fd-115">Azure 備份容器的備份管理類型</span><span class="sxs-lookup"><span data-stu-id="7d6fd-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6fd-116">-容器</span><span class="sxs-lookup"><span data-stu-id="7d6fd-116">-Container</span></span>
<span data-ttu-id="7d6fd-117">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="7d6fd-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6fd-118">-DefaultProfile</span></span>
<span data-ttu-id="7d6fd-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d6fd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7d6fd-120">-Force</span></span>
<span data-ttu-id="7d6fd-121">強制註冊容器 (會防止確認對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="7d6fd-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d6fd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6fd-123">-ResourceId</span></span>
<span data-ttu-id="7d6fd-124">需要檢查其代表代表的 Azure 資源（如果訂閱中的某些 RecoveryServices 保存庫已受到保護）的 ID。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6fd-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7d6fd-125">-VaultId</span></span>
<span data-ttu-id="7d6fd-126">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6fd-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7d6fd-127">-WorkloadType</span></span>
<span data-ttu-id="7d6fd-128">資源的工作量類型 (例如： Add-azurevm、WindowsServer、AzureFiles、MSSQL) 。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6fd-129">-確認</span><span class="sxs-lookup"><span data-stu-id="7d6fd-129">-Confirm</span></span>
<span data-ttu-id="7d6fd-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6fd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6fd-131">-WhatIf</span></span>
<span data-ttu-id="7d6fd-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6fd-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6fd-134">CommonParameters</span></span>
<span data-ttu-id="7d6fd-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6fd-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d6fd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6fd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7d6fd-137">INPUTS</span></span>

### <span data-ttu-id="7d6fd-138">System.object</span><span class="sxs-lookup"><span data-stu-id="7d6fd-138">System.String</span></span>

## <span data-ttu-id="7d6fd-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7d6fd-139">OUTPUTS</span></span>

### <span data-ttu-id="7d6fd-140">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="7d6fd-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="7d6fd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7d6fd-141">NOTES</span></span>

## <span data-ttu-id="7d6fd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d6fd-142">RELATED LINKS</span></span>