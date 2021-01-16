---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283760"
---
# <span data-ttu-id="b770f-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b770f-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b770f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b770f-102">SYNOPSIS</span></span>
<span data-ttu-id="b770f-103">取得保存庫的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="b770f-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="b770f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b770f-104">SYNTAX</span></span>

### <span data-ttu-id="b770f-105">NoParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b770f-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b770f-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="b770f-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b770f-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="b770f-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b770f-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="b770f-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b770f-109">說明</span><span class="sxs-lookup"><span data-stu-id="b770f-109">DESCRIPTION</span></span>
<span data-ttu-id="b770f-110">**AzRecoveryServicesBackupProtectionPolicy** Cmdlet 會取得保存庫的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="b770f-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="b770f-111">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b770f-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b770f-112">示例</span><span class="sxs-lookup"><span data-stu-id="b770f-112">EXAMPLES</span></span>

### <span data-ttu-id="b770f-113">範例1：取得保存庫中的所有原則</span><span class="sxs-lookup"><span data-stu-id="b770f-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="b770f-114">這個命令會取得在保存庫中建立的所有保護原則。</span><span class="sxs-lookup"><span data-stu-id="b770f-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="b770f-115">範例2：取得特定原則</span><span class="sxs-lookup"><span data-stu-id="b770f-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="b770f-116">這個命令會取得名為 DefaultPolicy 的保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="b770f-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="b770f-117">參數</span><span class="sxs-lookup"><span data-stu-id="b770f-117">PARAMETERS</span></span>

### <span data-ttu-id="b770f-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b770f-118">-BackupManagementType</span></span>
<span data-ttu-id="b770f-119">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="b770f-119">The class of resources being protected.</span></span> <span data-ttu-id="b770f-120">這個 Cmdlet 支援的值目前是 AzureStorage、AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="b770f-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

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

### <span data-ttu-id="b770f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b770f-121">-DefaultProfile</span></span>
<span data-ttu-id="b770f-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b770f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b770f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b770f-123">-Name</span></span>
<span data-ttu-id="b770f-124">指定原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b770f-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="b770f-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b770f-125">-VaultId</span></span>
<span data-ttu-id="b770f-126">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="b770f-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b770f-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b770f-127">-WorkloadType</span></span>
<span data-ttu-id="b770f-128">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="b770f-128">Workload type of the resource.</span></span> <span data-ttu-id="b770f-129">目前支援的值為 Add-azurevm、AzureFiles、MSSQL</span><span class="sxs-lookup"><span data-stu-id="b770f-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="b770f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b770f-130">CommonParameters</span></span>
<span data-ttu-id="b770f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b770f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b770f-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b770f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b770f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b770f-133">INPUTS</span></span>

### <span data-ttu-id="b770f-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b770f-134">System.String</span></span>

## <span data-ttu-id="b770f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b770f-135">OUTPUTS</span></span>

### <span data-ttu-id="b770f-136">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="b770f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="b770f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b770f-137">NOTES</span></span>

## <span data-ttu-id="b770f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b770f-138">RELATED LINKS</span></span>

[<span data-ttu-id="b770f-139">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b770f-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b770f-140">移除-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b770f-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b770f-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b770f-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


