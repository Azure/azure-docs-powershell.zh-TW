---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623551"
---
# <span data-ttu-id="b2710-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="b2710-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="b2710-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2710-102">SYNOPSIS</span></span>
<span data-ttu-id="b2710-103">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。</span><span class="sxs-lookup"><span data-stu-id="b2710-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2710-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2710-104">SYNTAX</span></span>

### <span data-ttu-id="b2710-105">AzureToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="b2710-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2710-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b2710-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2710-107">說明</span><span class="sxs-lookup"><span data-stu-id="b2710-107">DESCRIPTION</span></span>
<span data-ttu-id="b2710-108">建立磁片對應物件，該物件會將 Azure 虛擬機器磁片對應至快取儲存空間帳戶，並將目標儲存空間帳戶 (復原區域) ，以用於複製磁片。</span><span class="sxs-lookup"><span data-stu-id="b2710-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="b2710-109">示例</span><span class="sxs-lookup"><span data-stu-id="b2710-109">EXAMPLES</span></span>

### <span data-ttu-id="b2710-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b2710-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="b2710-111">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。在 Azure to Azure EnableDr 和重新保護作業期間使用。</span><span class="sxs-lookup"><span data-stu-id="b2710-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="b2710-112">參數</span><span class="sxs-lookup"><span data-stu-id="b2710-112">PARAMETERS</span></span>

### <span data-ttu-id="b2710-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2710-113">-DefaultProfile</span></span>
<span data-ttu-id="b2710-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2710-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2710-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="b2710-115">-DiskId</span></span>
<span data-ttu-id="b2710-116">指定受管理磁片的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2710-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b2710-117">-LogStorageAccountId</span></span>
<span data-ttu-id="b2710-118">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2710-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b2710-119">-ManagedDisk</span></span>
<span data-ttu-id="b2710-120">指定所管理磁片的輸入。</span><span class="sxs-lookup"><span data-stu-id="b2710-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b2710-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b2710-122">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="b2710-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="b2710-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="b2710-124">指定複製的受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="b2710-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b2710-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="b2710-126">為已複製的受管理磁片指定復原資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2710-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="b2710-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="b2710-128">指定複製的受管理磁片的復原目標磁片。</span><span class="sxs-lookup"><span data-stu-id="b2710-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b2710-129">-VhdUri</span></span>
<span data-ttu-id="b2710-130">指定此對應對應之磁片的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="b2710-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2710-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b2710-131">-Confirm</span></span>
<span data-ttu-id="b2710-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2710-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2710-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2710-133">-WhatIf</span></span>
<span data-ttu-id="b2710-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2710-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2710-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2710-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2710-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2710-136">CommonParameters</span></span>
<span data-ttu-id="b2710-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2710-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2710-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2710-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2710-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b2710-139">INPUTS</span></span>

### <span data-ttu-id="b2710-140">所有</span><span class="sxs-lookup"><span data-stu-id="b2710-140">None</span></span>

## <span data-ttu-id="b2710-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b2710-141">OUTPUTS</span></span>

### <span data-ttu-id="b2710-142">RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="b2710-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="b2710-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b2710-143">NOTES</span></span>

## <span data-ttu-id="b2710-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2710-144">RELATED LINKS</span></span>
