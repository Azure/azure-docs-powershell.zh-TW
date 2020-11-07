---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623594"
---
# <span data-ttu-id="79efa-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="79efa-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="79efa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79efa-102">SYNOPSIS</span></span>
<span data-ttu-id="79efa-103">取得保存庫的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="79efa-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79efa-104">句法</span><span class="sxs-lookup"><span data-stu-id="79efa-104">SYNTAX</span></span>

### <span data-ttu-id="79efa-105">NoParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79efa-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79efa-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="79efa-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79efa-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="79efa-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79efa-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="79efa-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79efa-109">說明</span><span class="sxs-lookup"><span data-stu-id="79efa-109">DESCRIPTION</span></span>
<span data-ttu-id="79efa-110">**AzureRmRecoveryServicesBackupProtectionPolicy** Cmdlet 會取得保存庫的 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="79efa-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="79efa-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79efa-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="79efa-112">示例</span><span class="sxs-lookup"><span data-stu-id="79efa-112">EXAMPLES</span></span>

### <span data-ttu-id="79efa-113">範例1：取得保存庫中的所有原則</span><span class="sxs-lookup"><span data-stu-id="79efa-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="79efa-114">這個命令會取得在保存庫中建立的所有保護原則。</span><span class="sxs-lookup"><span data-stu-id="79efa-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="79efa-115">範例2：取得特定原則</span><span class="sxs-lookup"><span data-stu-id="79efa-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="79efa-116">這個命令會取得名為 DefaultPolicy 的保護原則，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="79efa-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="79efa-117">參數</span><span class="sxs-lookup"><span data-stu-id="79efa-117">PARAMETERS</span></span>

### <span data-ttu-id="79efa-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="79efa-118">-BackupManagementType</span></span>
<span data-ttu-id="79efa-119">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="79efa-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="79efa-120">目前僅支援 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="79efa-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79efa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79efa-121">-DefaultProfile</span></span>
<span data-ttu-id="79efa-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79efa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79efa-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="79efa-123">-Name</span></span>
<span data-ttu-id="79efa-124">指定原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="79efa-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79efa-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="79efa-125">-WorkloadType</span></span>
<span data-ttu-id="79efa-126">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="79efa-126">Specifies the workload type.</span></span>
<span data-ttu-id="79efa-127">目前僅支援 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="79efa-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79efa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79efa-128">CommonParameters</span></span>
<span data-ttu-id="79efa-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79efa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79efa-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79efa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79efa-131">輸入</span><span class="sxs-lookup"><span data-stu-id="79efa-131">INPUTS</span></span>

### <span data-ttu-id="79efa-132">所有</span><span class="sxs-lookup"><span data-stu-id="79efa-132">None</span></span>
<span data-ttu-id="79efa-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="79efa-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79efa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="79efa-134">OUTPUTS</span></span>

### <span data-ttu-id="79efa-135">PolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="79efa-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="79efa-136">[System.object]. RecoveryServices [PolicyBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="79efa-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="79efa-137">筆記</span><span class="sxs-lookup"><span data-stu-id="79efa-137">NOTES</span></span>

## <span data-ttu-id="79efa-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="79efa-138">RELATED LINKS</span></span>

[<span data-ttu-id="79efa-139">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="79efa-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="79efa-140">移除-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="79efa-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="79efa-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="79efa-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


