---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798781"
---
# <span data-ttu-id="acaa9-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="acaa9-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="acaa9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="acaa9-103">針對可保護的專案停用自動備份。</span><span class="sxs-lookup"><span data-stu-id="acaa9-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="acaa9-104">句法</span><span class="sxs-lookup"><span data-stu-id="acaa9-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acaa9-105">說明</span><span class="sxs-lookup"><span data-stu-id="acaa9-105">DESCRIPTION</span></span>
<span data-ttu-id="acaa9-106">**Disable AzRecoveryServicesBackupAutoProtection** Cmdlet 會在能保護的專案上停用保護。</span><span class="sxs-lookup"><span data-stu-id="acaa9-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="acaa9-107">示例</span><span class="sxs-lookup"><span data-stu-id="acaa9-107">EXAMPLES</span></span>

### <span data-ttu-id="acaa9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="acaa9-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="acaa9-109">第一個 Cmdlet 會停用備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="acaa9-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="acaa9-110">參數</span><span class="sxs-lookup"><span data-stu-id="acaa9-110">PARAMETERS</span></span>

### <span data-ttu-id="acaa9-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="acaa9-111">-BackupManagementType</span></span>
<span data-ttu-id="acaa9-112">資源的備份管理類型 (例如： MAB、DPM) 。</span><span class="sxs-lookup"><span data-stu-id="acaa9-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acaa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acaa9-113">-DefaultProfile</span></span>
<span data-ttu-id="acaa9-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acaa9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acaa9-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="acaa9-115">-InputItem</span></span>
<span data-ttu-id="acaa9-116">專案識別碼</span><span class="sxs-lookup"><span data-stu-id="acaa9-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acaa9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acaa9-117">-PassThru</span></span>
<span data-ttu-id="acaa9-118">傳回自動保護的結果。</span><span class="sxs-lookup"><span data-stu-id="acaa9-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="acaa9-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="acaa9-119">-VaultId</span></span>
<span data-ttu-id="acaa9-120">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="acaa9-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="acaa9-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="acaa9-121">-WorkloadType</span></span>
<span data-ttu-id="acaa9-122">資源的工作量類型 (例如： Add-azurevm、WindowsServer、AzureFiles) 。</span><span class="sxs-lookup"><span data-stu-id="acaa9-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

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

### <span data-ttu-id="acaa9-123">-確認</span><span class="sxs-lookup"><span data-stu-id="acaa9-123">-Confirm</span></span>
<span data-ttu-id="acaa9-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acaa9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acaa9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acaa9-125">-WhatIf</span></span>
<span data-ttu-id="acaa9-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acaa9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acaa9-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acaa9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acaa9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acaa9-128">CommonParameters</span></span>
<span data-ttu-id="acaa9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acaa9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acaa9-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="acaa9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acaa9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="acaa9-131">INPUTS</span></span>

### <span data-ttu-id="acaa9-132">System.object</span><span class="sxs-lookup"><span data-stu-id="acaa9-132">System.String</span></span>

## <span data-ttu-id="acaa9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="acaa9-133">OUTPUTS</span></span>

### <span data-ttu-id="acaa9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="acaa9-134">System.Boolean</span></span>

## <span data-ttu-id="acaa9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="acaa9-135">NOTES</span></span>

## <span data-ttu-id="acaa9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="acaa9-136">RELATED LINKS</span></span>
