---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448052"
---
# <span data-ttu-id="5170d-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="5170d-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="5170d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5170d-102">SYNOPSIS</span></span>
<span data-ttu-id="5170d-103">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="5170d-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5170d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5170d-104">SYNTAX</span></span>

### <span data-ttu-id="5170d-105">AzureVMComputeEnableProtection (預設) </span><span class="sxs-lookup"><span data-stu-id="5170d-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5170d-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="5170d-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5170d-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="5170d-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5170d-108">說明</span><span class="sxs-lookup"><span data-stu-id="5170d-108">DESCRIPTION</span></span>
<span data-ttu-id="5170d-109">**Enable-AzureRmRecoveryServicesBackupProtection** Cmdlet 會針對專案設定 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5170d-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="5170d-110">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5170d-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5170d-111">示例</span><span class="sxs-lookup"><span data-stu-id="5170d-111">EXAMPLES</span></span>

### <span data-ttu-id="5170d-112">範例1：為專案啟用備份保護</span><span class="sxs-lookup"><span data-stu-id="5170d-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="5170d-113">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="5170d-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="5170d-114">第二個 Cmdlet 會使用 $Pol 中的原則，為名為 V2VM 的 ARM 虛擬機器設定備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="5170d-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="5170d-115">參數</span><span class="sxs-lookup"><span data-stu-id="5170d-115">PARAMETERS</span></span>

### <span data-ttu-id="5170d-116">-專案</span><span class="sxs-lookup"><span data-stu-id="5170d-116">-Item</span></span>
<span data-ttu-id="5170d-117">指定此 Cmdlet 針對其啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="5170d-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="5170d-118">若要取得 **AzureRmRecoveryServicesBackupItem** ，請使用 Get-AzureRmRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5170d-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5170d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5170d-119">-Name</span></span>
<span data-ttu-id="5170d-120">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="5170d-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5170d-121">-原則</span><span class="sxs-lookup"><span data-stu-id="5170d-121">-Policy</span></span>
<span data-ttu-id="5170d-122">指定此 Cmdlet 與專案相關聯的保護原則。</span><span class="sxs-lookup"><span data-stu-id="5170d-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="5170d-123">若要取得 **AzureRmRecoveryServicesBackupProtectionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5170d-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5170d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5170d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5170d-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5170d-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="5170d-126">請僅針對 ARM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="5170d-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5170d-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5170d-127">-ServiceName</span></span>
<span data-ttu-id="5170d-128">指定服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5170d-128">Specifies the service name.</span></span>
<span data-ttu-id="5170d-129">僅針對 ASM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="5170d-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5170d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5170d-130">-DefaultProfile</span></span>
<span data-ttu-id="5170d-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5170d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5170d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5170d-132">CommonParameters</span></span>
<span data-ttu-id="5170d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5170d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5170d-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5170d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5170d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5170d-135">INPUTS</span></span>

### <span data-ttu-id="5170d-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="5170d-136">ItemBase</span></span>
<span data-ttu-id="5170d-137">形參 "Item" 接受管線中 "ItemBase" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5170d-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="5170d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5170d-138">OUTPUTS</span></span>

### <span data-ttu-id="5170d-139">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="5170d-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5170d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5170d-140">NOTES</span></span>

## <span data-ttu-id="5170d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5170d-141">RELATED LINKS</span></span>

[<span data-ttu-id="5170d-142">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="5170d-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="5170d-143">AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5170d-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

