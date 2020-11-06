---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621122"
---
# <span data-ttu-id="a73d3-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="a73d3-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="a73d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a73d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a73d3-103">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。</span><span class="sxs-lookup"><span data-stu-id="a73d3-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="a73d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="a73d3-104">SYNTAX</span></span>

### <span data-ttu-id="a73d3-105">AzureToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="a73d3-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a73d3-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a73d3-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a73d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="a73d3-107">DESCRIPTION</span></span>
<span data-ttu-id="a73d3-108">建立磁片對應物件，該物件會將 Azure 虛擬機器磁片對應至快取儲存空間帳戶，並將目標儲存空間帳戶 (復原區域) ，以用於複製磁片。</span><span class="sxs-lookup"><span data-stu-id="a73d3-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="a73d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="a73d3-109">EXAMPLES</span></span>

### <span data-ttu-id="a73d3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a73d3-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="a73d3-111">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。在 Azure to Azure EnableDr 和重新保護作業期間使用。</span><span class="sxs-lookup"><span data-stu-id="a73d3-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="a73d3-112">參數</span><span class="sxs-lookup"><span data-stu-id="a73d3-112">PARAMETERS</span></span>

### <span data-ttu-id="a73d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73d3-113">-DefaultProfile</span></span>
<span data-ttu-id="a73d3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a73d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a73d3-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="a73d3-115">-DiskId</span></span>
<span data-ttu-id="a73d3-116">指定受管理磁片的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="a73d3-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="a73d3-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a73d3-117">-LogStorageAccountId</span></span>
<span data-ttu-id="a73d3-118">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="a73d3-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="a73d3-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a73d3-119">-ManagedDisk</span></span>
<span data-ttu-id="a73d3-120">指定所管理磁片的輸入。</span><span class="sxs-lookup"><span data-stu-id="a73d3-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="a73d3-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a73d3-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a73d3-122">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="a73d3-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="a73d3-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="a73d3-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="a73d3-124">指定複製的受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="a73d3-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="a73d3-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a73d3-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="a73d3-126">為已複製的受管理磁片指定復原資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a73d3-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="a73d3-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="a73d3-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="a73d3-128">指定複製的受管理磁片的復原目標磁片。</span><span class="sxs-lookup"><span data-stu-id="a73d3-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="a73d3-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="a73d3-129">-VhdUri</span></span>
<span data-ttu-id="a73d3-130">指定此對應對應之磁片的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="a73d3-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="a73d3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a73d3-131">-Confirm</span></span>
<span data-ttu-id="a73d3-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a73d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a73d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73d3-133">-WhatIf</span></span>
<span data-ttu-id="a73d3-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a73d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73d3-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a73d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a73d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73d3-136">CommonParameters</span></span>
<span data-ttu-id="a73d3-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a73d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73d3-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a73d3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73d3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a73d3-139">INPUTS</span></span>

### <span data-ttu-id="a73d3-140">所有</span><span class="sxs-lookup"><span data-stu-id="a73d3-140">None</span></span>

## <span data-ttu-id="a73d3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a73d3-141">OUTPUTS</span></span>

### <span data-ttu-id="a73d3-142">RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="a73d3-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="a73d3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a73d3-143">NOTES</span></span>

## <span data-ttu-id="a73d3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a73d3-144">RELATED LINKS</span></span>
