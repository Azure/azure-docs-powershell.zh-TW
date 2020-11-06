---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448964"
---
# <span data-ttu-id="6c5a3-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c5a3-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6c5a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5a3-103">取得保存庫的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c5a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c5a3-104">SYNTAX</span></span>

### <span data-ttu-id="6c5a3-105">NoParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c5a3-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c5a3-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="6c5a3-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c5a3-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="6c5a3-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c5a3-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="6c5a3-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c5a3-109">說明</span><span class="sxs-lookup"><span data-stu-id="6c5a3-109">DESCRIPTION</span></span>
<span data-ttu-id="6c5a3-110">**AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 會取得保存庫的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="6c5a3-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6c5a3-112">示例</span><span class="sxs-lookup"><span data-stu-id="6c5a3-112">EXAMPLES</span></span>

### <span data-ttu-id="6c5a3-113">範例1：取得保存庫中的所有原則</span><span class="sxs-lookup"><span data-stu-id="6c5a3-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="6c5a3-114">這個命令會取得在保存庫中建立的所有保護原則。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="6c5a3-115">範例2：取得特定原則</span><span class="sxs-lookup"><span data-stu-id="6c5a3-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="6c5a3-116">這個命令會取得名為 DefaultPolicy 的保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="6c5a3-117">參數</span><span class="sxs-lookup"><span data-stu-id="6c5a3-117">PARAMETERS</span></span>

### <span data-ttu-id="6c5a3-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6c5a3-118">-BackupManagementType</span></span>
<span data-ttu-id="6c5a3-119">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="6c5a3-120">目前僅支援 Add-azurevm、AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5a3-121">-DefaultProfile</span></span>
<span data-ttu-id="6c5a3-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c5a3-123">-Name</span></span>
<span data-ttu-id="6c5a3-124">指定原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="6c5a3-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6c5a3-125">-VaultId</span></span>
<span data-ttu-id="6c5a3-126">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6c5a3-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6c5a3-127">-WorkloadType</span></span>
<span data-ttu-id="6c5a3-128">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-128">Specifies the workload type.</span></span>
<span data-ttu-id="6c5a3-129">目前僅支援 Add-azurevm、AzureFiles。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5a3-130">CommonParameters</span></span>
<span data-ttu-id="6c5a3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5a3-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c5a3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5a3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6c5a3-133">INPUTS</span></span>

### <span data-ttu-id="6c5a3-134">System.object</span><span class="sxs-lookup"><span data-stu-id="6c5a3-134">System.String</span></span>
<span data-ttu-id="6c5a3-135">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6c5a3-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="6c5a3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6c5a3-136">OUTPUTS</span></span>

### <span data-ttu-id="6c5a3-137">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="6c5a3-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="6c5a3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6c5a3-138">NOTES</span></span>

## <span data-ttu-id="6c5a3-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c5a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="6c5a3-140">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c5a3-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6c5a3-141">移除-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c5a3-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6c5a3-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c5a3-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


