---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: a17c7b8addf1bf1218131e8e950185d9da6c22d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621197"
---
# <span data-ttu-id="96c74-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="96c74-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="96c74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96c74-102">SYNOPSIS</span></span>
<span data-ttu-id="96c74-103">這個命令可讓使用者自動保護所有現有未受保護的資料庫，以及稍後會以指定原則新增的任何 DB。</span><span class="sxs-lookup"><span data-stu-id="96c74-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="96c74-104">然後，Azure 備份服務會定期針對任何新的處理來掃描自動保護的容器，並自動保護它們。</span><span class="sxs-lookup"><span data-stu-id="96c74-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="96c74-105">句法</span><span class="sxs-lookup"><span data-stu-id="96c74-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96c74-106">說明</span><span class="sxs-lookup"><span data-stu-id="96c74-106">DESCRIPTION</span></span>
<span data-ttu-id="96c74-107">**Enable-AzRecoveryServicesBackupAutoProtection** Cmdlet 會在可保護的專案上設定 Azure 自動備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="96c74-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="96c74-108">示例</span><span class="sxs-lookup"><span data-stu-id="96c74-108">EXAMPLES</span></span>

### <span data-ttu-id="96c74-109">範例1</span><span class="sxs-lookup"><span data-stu-id="96c74-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="96c74-110">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="96c74-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="96c74-111">第二個 Cmdlet 會使用 $Pol 中的原則設定 AzureWorkload 的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="96c74-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="96c74-112">參數</span><span class="sxs-lookup"><span data-stu-id="96c74-112">PARAMETERS</span></span>

### <span data-ttu-id="96c74-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="96c74-113">-BackupManagementType</span></span>
<span data-ttu-id="96c74-114">資源的備份管理類型 (例如： MAB、DPM、AzureWorkload) 。</span><span class="sxs-lookup"><span data-stu-id="96c74-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="96c74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c74-115">-DefaultProfile</span></span>
<span data-ttu-id="96c74-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96c74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96c74-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="96c74-117">-InputItem</span></span>
<span data-ttu-id="96c74-118">指定可以傳送成輸入的可保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="96c74-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="96c74-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96c74-119">-PassThru</span></span>
<span data-ttu-id="96c74-120">傳回自動保護的結果。</span><span class="sxs-lookup"><span data-stu-id="96c74-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="96c74-121">-原則</span><span class="sxs-lookup"><span data-stu-id="96c74-121">-Policy</span></span>
<span data-ttu-id="96c74-122">保護原則物件。</span><span class="sxs-lookup"><span data-stu-id="96c74-122">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c74-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="96c74-123">-VaultId</span></span>
<span data-ttu-id="96c74-124">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="96c74-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="96c74-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="96c74-125">-WorkloadType</span></span>
<span data-ttu-id="96c74-126">資源的工作量類型 (例如： Add-azurevm、WindowsServer、AzureFiles、MSSQL) 。</span><span class="sxs-lookup"><span data-stu-id="96c74-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="96c74-127">-確認</span><span class="sxs-lookup"><span data-stu-id="96c74-127">-Confirm</span></span>
<span data-ttu-id="96c74-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96c74-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c74-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c74-129">-WhatIf</span></span>
<span data-ttu-id="96c74-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96c74-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c74-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96c74-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c74-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c74-132">CommonParameters</span></span>
<span data-ttu-id="96c74-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96c74-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c74-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96c74-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c74-135">輸入</span><span class="sxs-lookup"><span data-stu-id="96c74-135">INPUTS</span></span>

### <span data-ttu-id="96c74-136">System.object</span><span class="sxs-lookup"><span data-stu-id="96c74-136">System.String</span></span>

## <span data-ttu-id="96c74-137">輸出</span><span class="sxs-lookup"><span data-stu-id="96c74-137">OUTPUTS</span></span>

### <span data-ttu-id="96c74-138">System.object</span><span class="sxs-lookup"><span data-stu-id="96c74-138">System.Object</span></span>

## <span data-ttu-id="96c74-139">筆記</span><span class="sxs-lookup"><span data-stu-id="96c74-139">NOTES</span></span>

## <span data-ttu-id="96c74-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="96c74-140">RELATED LINKS</span></span>