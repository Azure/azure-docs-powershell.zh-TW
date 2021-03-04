---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c29ff9d1fbe4a34f17a491dd1cb3c86c16f3ce75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903438"
---
# <span data-ttu-id="92b34-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92b34-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="92b34-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92b34-102">SYNOPSIS</span></span>
<span data-ttu-id="92b34-103">為儲存庫獲取備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="92b34-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="92b34-104">語法</span><span class="sxs-lookup"><span data-stu-id="92b34-104">SYNTAX</span></span>

### <span data-ttu-id="92b34-105">NoParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="92b34-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92b34-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="92b34-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92b34-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="92b34-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92b34-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="92b34-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92b34-109">描述</span><span class="sxs-lookup"><span data-stu-id="92b34-109">DESCRIPTION</span></span>
<span data-ttu-id="92b34-110">**Get-AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會取得適用于儲存庫的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="92b34-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="92b34-111">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="92b34-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="92b34-112">例子</span><span class="sxs-lookup"><span data-stu-id="92b34-112">EXAMPLES</span></span>

### <span data-ttu-id="92b34-113">範例 1：取得資料庫中的所有策略</span><span class="sxs-lookup"><span data-stu-id="92b34-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="92b34-114">此命令會獲得在儲存庫中建立的所有保護原則。</span><span class="sxs-lookup"><span data-stu-id="92b34-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="92b34-115">範例 2：取得特定政策</span><span class="sxs-lookup"><span data-stu-id="92b34-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="92b34-116">此命令會獲得名為 DefaultPolicy 的保護原則，然後將它儲存在$Pol變數中。</span><span class="sxs-lookup"><span data-stu-id="92b34-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="92b34-117">參數</span><span class="sxs-lookup"><span data-stu-id="92b34-117">PARAMETERS</span></span>

### <span data-ttu-id="92b34-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="92b34-118">-BackupManagementType</span></span>
<span data-ttu-id="92b34-119">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="92b34-119">The class of resources being protected.</span></span> <span data-ttu-id="92b34-120">此 Cmdlet 目前支援的值為 AzureCM、AzureStorage、AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="92b34-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b34-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b34-121">-DefaultProfile</span></span>
<span data-ttu-id="92b34-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92b34-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b34-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="92b34-123">-Name</span></span>
<span data-ttu-id="92b34-124">指定該策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="92b34-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b34-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="92b34-125">-VaultId</span></span>
<span data-ttu-id="92b34-126">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="92b34-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="92b34-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="92b34-127">-WorkloadType</span></span>
<span data-ttu-id="92b34-128">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="92b34-128">Workload type of the resource.</span></span> <span data-ttu-id="92b34-129">目前支援的值為 AzureMS、AzureFiles、MSSQL</span><span class="sxs-lookup"><span data-stu-id="92b34-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b34-130">CommonParameters</span></span>
<span data-ttu-id="92b34-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92b34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b34-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92b34-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b34-133">輸入</span><span class="sxs-lookup"><span data-stu-id="92b34-133">INPUTS</span></span>

### <span data-ttu-id="92b34-134">System.String</span><span class="sxs-lookup"><span data-stu-id="92b34-134">System.String</span></span>

## <span data-ttu-id="92b34-135">輸出</span><span class="sxs-lookup"><span data-stu-id="92b34-135">OUTPUTS</span></span>

### <span data-ttu-id="92b34-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="92b34-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="92b34-137">筆記</span><span class="sxs-lookup"><span data-stu-id="92b34-137">NOTES</span></span>

## <span data-ttu-id="92b34-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="92b34-138">RELATED LINKS</span></span>

[<span data-ttu-id="92b34-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92b34-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="92b34-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92b34-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="92b34-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92b34-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


