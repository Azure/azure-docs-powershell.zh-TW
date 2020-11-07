---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: a6c47561b8fdb9e748940c917d85548d25be1ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958624"
---
# <span data-ttu-id="824ac-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="824ac-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="824ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="824ac-102">SYNOPSIS</span></span>
<span data-ttu-id="824ac-103">這個命令可讓 Azure Backup 將資源轉換成備份容器，然後再將登錄到指定的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="824ac-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="824ac-104">然後，Azure 備份服務就可以在此容器中發現指定工作負荷類型的工作負荷，以備日後受到保護。</span><span class="sxs-lookup"><span data-stu-id="824ac-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="824ac-105">句法</span><span class="sxs-lookup"><span data-stu-id="824ac-105">SYNTAX</span></span>

### <span data-ttu-id="824ac-106">註冊 (預設) </span><span class="sxs-lookup"><span data-stu-id="824ac-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824ac-107">于</span><span class="sxs-lookup"><span data-stu-id="824ac-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824ac-108">說明</span><span class="sxs-lookup"><span data-stu-id="824ac-108">DESCRIPTION</span></span>
<span data-ttu-id="824ac-109">這個 Cmdlet 會使用特定 workloadType 註冊 AzureWorkloads 的 Azure VM。</span><span class="sxs-lookup"><span data-stu-id="824ac-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="824ac-110">示例</span><span class="sxs-lookup"><span data-stu-id="824ac-110">EXAMPLES</span></span>

### <span data-ttu-id="824ac-111">範例1</span><span class="sxs-lookup"><span data-stu-id="824ac-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="824ac-112">這個 Cmdlet 會針對工作負荷 MSSQL 註冊 azure VM。</span><span class="sxs-lookup"><span data-stu-id="824ac-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="824ac-113">參數</span><span class="sxs-lookup"><span data-stu-id="824ac-113">PARAMETERS</span></span>

### <span data-ttu-id="824ac-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="824ac-114">-BackupManagementType</span></span>
<span data-ttu-id="824ac-115">Azure 備份容器的備份管理類型</span><span class="sxs-lookup"><span data-stu-id="824ac-115">The backup management type of the Azure Backup container</span></span>

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

### <span data-ttu-id="824ac-116">-容器</span><span class="sxs-lookup"><span data-stu-id="824ac-116">-Container</span></span>
<span data-ttu-id="824ac-117">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="824ac-117">Container where the item resides</span></span>

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

### <span data-ttu-id="824ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824ac-118">-DefaultProfile</span></span>
<span data-ttu-id="824ac-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="824ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="824ac-120">-Force</span><span class="sxs-lookup"><span data-stu-id="824ac-120">-Force</span></span>
<span data-ttu-id="824ac-121">強制註冊容器 (會防止確認對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="824ac-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="824ac-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="824ac-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="824ac-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="824ac-123">-ResourceId</span></span>
<span data-ttu-id="824ac-124">需要檢查其代表代表的 Azure 資源（如果訂閱中的某些 RecoveryServices 保存庫已受到保護）的 ID。</span><span class="sxs-lookup"><span data-stu-id="824ac-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="824ac-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="824ac-125">-VaultId</span></span>
<span data-ttu-id="824ac-126">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="824ac-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="824ac-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="824ac-127">-WorkloadType</span></span>
<span data-ttu-id="824ac-128">資源的工作量類型 (例如： Add-azurevm、WindowsServer、AzureFiles、MSSQL) 。</span><span class="sxs-lookup"><span data-stu-id="824ac-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="824ac-129">-確認</span><span class="sxs-lookup"><span data-stu-id="824ac-129">-Confirm</span></span>
<span data-ttu-id="824ac-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="824ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824ac-131">-WhatIf</span></span>
<span data-ttu-id="824ac-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="824ac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824ac-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="824ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824ac-134">CommonParameters</span></span>
<span data-ttu-id="824ac-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="824ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824ac-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="824ac-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824ac-137">輸入</span><span class="sxs-lookup"><span data-stu-id="824ac-137">INPUTS</span></span>

### <span data-ttu-id="824ac-138">System.object</span><span class="sxs-lookup"><span data-stu-id="824ac-138">System.String</span></span>

## <span data-ttu-id="824ac-139">輸出</span><span class="sxs-lookup"><span data-stu-id="824ac-139">OUTPUTS</span></span>

### <span data-ttu-id="824ac-140">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="824ac-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="824ac-141">筆記</span><span class="sxs-lookup"><span data-stu-id="824ac-141">NOTES</span></span>

## <span data-ttu-id="824ac-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="824ac-142">RELATED LINKS</span></span>
