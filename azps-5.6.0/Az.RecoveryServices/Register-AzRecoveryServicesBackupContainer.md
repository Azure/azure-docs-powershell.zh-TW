---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 83a0e4edd82bd77358df1d95b53e388bb35a9e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902246"
---
# <span data-ttu-id="80c8d-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="80c8d-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="80c8d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="80c8d-103">**Register-AzRecoveryServicesBackupContainer Cmdlet** 會針對特定工作負載類型之 AzureWorkloads 註冊 Azure VM。</span><span class="sxs-lookup"><span data-stu-id="80c8d-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="80c8d-104">語法</span><span class="sxs-lookup"><span data-stu-id="80c8d-104">SYNTAX</span></span>

### <span data-ttu-id="80c8d-105">註冊 (預設) </span><span class="sxs-lookup"><span data-stu-id="80c8d-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c8d-106">ReRegister</span><span class="sxs-lookup"><span data-stu-id="80c8d-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c8d-107">描述</span><span class="sxs-lookup"><span data-stu-id="80c8d-107">DESCRIPTION</span></span>
<span data-ttu-id="80c8d-108">此命令可讓 Azure 備份將資源轉換為備份容器，該容器接著會註冊到給定修復服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="80c8d-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="80c8d-109">接著，Azure 備份服務就可以探索此容器內之給定工作負載類型的工作負載，以稍後受到保護。</span><span class="sxs-lookup"><span data-stu-id="80c8d-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="80c8d-110">例子</span><span class="sxs-lookup"><span data-stu-id="80c8d-110">EXAMPLES</span></span>

### <span data-ttu-id="80c8d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="80c8d-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="80c8d-112">Cmdlet 會登錄 azure VM 做為工作負載 MSSQL 的容器。</span><span class="sxs-lookup"><span data-stu-id="80c8d-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="80c8d-113">參數</span><span class="sxs-lookup"><span data-stu-id="80c8d-113">PARAMETERS</span></span>

### <span data-ttu-id="80c8d-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="80c8d-114">-BackupManagementType</span></span>
<span data-ttu-id="80c8d-115">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="80c8d-115">The class of resources being protected.</span></span> <span data-ttu-id="80c8d-116">此 Cmdlet 目前支援的值為 AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="80c8d-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="80c8d-117">-Container</span><span class="sxs-lookup"><span data-stu-id="80c8d-117">-Container</span></span>
<span data-ttu-id="80c8d-118">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="80c8d-118">Container where the item resides</span></span>

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

### <span data-ttu-id="80c8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c8d-119">-DefaultProfile</span></span>
<span data-ttu-id="80c8d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="80c8d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c8d-121">-強制</span><span class="sxs-lookup"><span data-stu-id="80c8d-121">-Force</span></span>
<span data-ttu-id="80c8d-122">強制登錄容器 (確認對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="80c8d-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="80c8d-123">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="80c8d-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="80c8d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80c8d-124">-ResourceId</span></span>
<span data-ttu-id="80c8d-125">Azure 資源識別碼，其代表專案若已受訂閱中的某些 RecoveryServices Vault 保護，則必須檢查該專案。</span><span class="sxs-lookup"><span data-stu-id="80c8d-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="80c8d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="80c8d-126">-VaultId</span></span>
<span data-ttu-id="80c8d-127">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="80c8d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="80c8d-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="80c8d-128">-WorkloadType</span></span>
<span data-ttu-id="80c8d-129">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="80c8d-129">Workload type of the resource.</span></span> <span data-ttu-id="80c8d-130">目前支援的值為 AzureMS、WindowsServer、AzureFiles、MSSQL</span><span class="sxs-lookup"><span data-stu-id="80c8d-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="80c8d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="80c8d-131">-Confirm</span></span>
<span data-ttu-id="80c8d-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="80c8d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c8d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c8d-133">-WhatIf</span></span>
<span data-ttu-id="80c8d-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80c8d-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="80c8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c8d-135">CommonParameters</span></span>
<span data-ttu-id="80c8d-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80c8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c8d-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c8d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c8d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="80c8d-138">INPUTS</span></span>

### <span data-ttu-id="80c8d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="80c8d-139">System.String</span></span>

## <span data-ttu-id="80c8d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="80c8d-140">OUTPUTS</span></span>

### <span data-ttu-id="80c8d-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="80c8d-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="80c8d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="80c8d-142">NOTES</span></span>

## <span data-ttu-id="80c8d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="80c8d-143">RELATED LINKS</span></span>
