---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139495"
---
# <span data-ttu-id="32bd6-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="32bd6-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="32bd6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="32bd6-103">**AzRecoveryServicesBackupContainer** Cmdlet 會針對特定 WorkloadType 註冊 AzureWorkloads 的 Azure VM。</span><span class="sxs-lookup"><span data-stu-id="32bd6-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="32bd6-104">句法</span><span class="sxs-lookup"><span data-stu-id="32bd6-104">SYNTAX</span></span>

### <span data-ttu-id="32bd6-105">註冊 (預設) </span><span class="sxs-lookup"><span data-stu-id="32bd6-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bd6-106">于</span><span class="sxs-lookup"><span data-stu-id="32bd6-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32bd6-107">說明</span><span class="sxs-lookup"><span data-stu-id="32bd6-107">DESCRIPTION</span></span>
<span data-ttu-id="32bd6-108">這個命令可讓 Azure Backup 將資源轉換成備份容器，然後再將登錄到指定的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="32bd6-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="32bd6-109">然後，Azure 備份服務就可以在此容器中發現指定工作負荷類型的工作負荷，以備日後受到保護。</span><span class="sxs-lookup"><span data-stu-id="32bd6-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="32bd6-110">示例</span><span class="sxs-lookup"><span data-stu-id="32bd6-110">EXAMPLES</span></span>

### <span data-ttu-id="32bd6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="32bd6-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="32bd6-112">此 Cmdlet 會將 azure VM 註冊為工作負荷 MSSQL 的容器。</span><span class="sxs-lookup"><span data-stu-id="32bd6-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="32bd6-113">參數</span><span class="sxs-lookup"><span data-stu-id="32bd6-113">PARAMETERS</span></span>

### <span data-ttu-id="32bd6-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="32bd6-114">-BackupManagementType</span></span>
<span data-ttu-id="32bd6-115">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="32bd6-115">The class of resources being protected.</span></span> <span data-ttu-id="32bd6-116">目前這個 Cmdlet 支援的值為 AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="32bd6-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="32bd6-117">-容器</span><span class="sxs-lookup"><span data-stu-id="32bd6-117">-Container</span></span>
<span data-ttu-id="32bd6-118">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="32bd6-118">Container where the item resides</span></span>

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

### <span data-ttu-id="32bd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bd6-119">-DefaultProfile</span></span>
<span data-ttu-id="32bd6-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32bd6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32bd6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="32bd6-121">-Force</span></span>
<span data-ttu-id="32bd6-122">強制註冊容器 (會防止確認對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="32bd6-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="32bd6-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="32bd6-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="32bd6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32bd6-124">-ResourceId</span></span>
<span data-ttu-id="32bd6-125">需要檢查其代表代表的 Azure 資源（如果訂閱中的某些 RecoveryServices 保存庫已受到保護）的 ID。</span><span class="sxs-lookup"><span data-stu-id="32bd6-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="32bd6-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="32bd6-126">-VaultId</span></span>
<span data-ttu-id="32bd6-127">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="32bd6-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="32bd6-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="32bd6-128">-WorkloadType</span></span>
<span data-ttu-id="32bd6-129">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="32bd6-129">Workload type of the resource.</span></span> <span data-ttu-id="32bd6-130">目前支援的值為 Add-azurevm、WindowsServer、AzureFiles、MSSQL</span><span class="sxs-lookup"><span data-stu-id="32bd6-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="32bd6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="32bd6-131">-Confirm</span></span>
<span data-ttu-id="32bd6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32bd6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32bd6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bd6-133">-WhatIf</span></span>
<span data-ttu-id="32bd6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32bd6-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="32bd6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bd6-135">CommonParameters</span></span>
<span data-ttu-id="32bd6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32bd6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bd6-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32bd6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bd6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="32bd6-138">INPUTS</span></span>

### <span data-ttu-id="32bd6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="32bd6-139">System.String</span></span>

## <span data-ttu-id="32bd6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="32bd6-140">OUTPUTS</span></span>

### <span data-ttu-id="32bd6-141">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="32bd6-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="32bd6-142">筆記</span><span class="sxs-lookup"><span data-stu-id="32bd6-142">NOTES</span></span>

## <span data-ttu-id="32bd6-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="32bd6-143">RELATED LINKS</span></span>
