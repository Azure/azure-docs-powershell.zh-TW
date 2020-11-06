---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448040"
---
# <span data-ttu-id="12114-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12114-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="12114-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12114-102">SYNOPSIS</span></span>
<span data-ttu-id="12114-103">透過建立複製受保護的專案，為 ASR 可保護的專案啟用複製</span><span class="sxs-lookup"><span data-stu-id="12114-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12114-104">句法</span><span class="sxs-lookup"><span data-stu-id="12114-104">SYNTAX</span></span>

### <span data-ttu-id="12114-105">DisableDR (預設) </span><span class="sxs-lookup"><span data-stu-id="12114-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12114-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="12114-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12114-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="12114-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12114-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="12114-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12114-109">說明</span><span class="sxs-lookup"><span data-stu-id="12114-109">DESCRIPTION</span></span>
<span data-ttu-id="12114-110">**新的-AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會建立新的受保護的複製專案。</span><span class="sxs-lookup"><span data-stu-id="12114-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="12114-111">使用此 Cmdlet 來啟用 ASR 可保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="12114-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="12114-112">示例</span><span class="sxs-lookup"><span data-stu-id="12114-112">EXAMPLES</span></span>

### <span data-ttu-id="12114-113">範例1</span><span class="sxs-lookup"><span data-stu-id="12114-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="12114-114">針對指定的 ASR 可保護專案啟動複製受保護的專案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="12114-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="12114-115">參數</span><span class="sxs-lookup"><span data-stu-id="12114-115">PARAMETERS</span></span>

### <span data-ttu-id="12114-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="12114-116">-Name</span></span>
<span data-ttu-id="12114-117">指定 ASR 複製受保護的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="12114-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-118">-OS</span><span class="sxs-lookup"><span data-stu-id="12114-118">-OS</span></span>
<span data-ttu-id="12114-119">指定作業系統系列。</span><span class="sxs-lookup"><span data-stu-id="12114-119">Specifies the operating system family.</span></span>
<span data-ttu-id="12114-120">此參數可接受的值為： Windows 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="12114-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="12114-121">-OSDiskName</span></span>
<span data-ttu-id="12114-122">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="12114-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="12114-123">-ProtectableItem</span></span>
<span data-ttu-id="12114-124">指定要啟用複製的 ASR 可保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="12114-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12114-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="12114-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="12114-126">指定要用於複製之複製原則對應的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="12114-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="12114-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="12114-128">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="12114-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="12114-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="12114-130">指定在容錯移轉事件中，將建立虛擬機器之資源群組的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="12114-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="12114-131">-WaitForCompletion</span></span>
<span data-ttu-id="12114-132">指定在傳回前，該指令應等待完成操作。</span><span class="sxs-lookup"><span data-stu-id="12114-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-133">-確認</span><span class="sxs-lookup"><span data-stu-id="12114-133">-Confirm</span></span>
<span data-ttu-id="12114-134">啟動作業前提示您確認。</span><span class="sxs-lookup"><span data-stu-id="12114-134">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12114-135">-WhatIf</span></span>
<span data-ttu-id="12114-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12114-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12114-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12114-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12114-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12114-138">CommonParameters</span></span>
<span data-ttu-id="12114-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12114-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12114-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12114-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12114-141">輸入</span><span class="sxs-lookup"><span data-stu-id="12114-141">INPUTS</span></span>

### <span data-ttu-id="12114-142">RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="12114-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="12114-143">輸出</span><span class="sxs-lookup"><span data-stu-id="12114-143">OUTPUTS</span></span>

### <span data-ttu-id="12114-144">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="12114-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="12114-145">筆記</span><span class="sxs-lookup"><span data-stu-id="12114-145">NOTES</span></span>

## <span data-ttu-id="12114-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="12114-146">RELATED LINKS</span></span>

[<span data-ttu-id="12114-147">AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12114-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="12114-148">移除-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12114-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="12114-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12114-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
