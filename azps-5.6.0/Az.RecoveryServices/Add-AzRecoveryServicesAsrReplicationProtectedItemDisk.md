---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: 1f69ba390d0cdf3184b876147984c10e79ed423a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910941"
---
# <span data-ttu-id="de245-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="de245-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="de245-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de245-102">SYNOPSIS</span></span>
<span data-ttu-id="de245-103">新增磁片來保護已受保護的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="de245-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="de245-104">語法</span><span class="sxs-lookup"><span data-stu-id="de245-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de245-105">描述</span><span class="sxs-lookup"><span data-stu-id="de245-105">DESCRIPTION</span></span>
<span data-ttu-id="de245-106">**Add-AzRecoveryServicesAsrReplicationProtecedItemAz** Cmdlet 新增磁片來保護已受保護的 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="de245-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="de245-107">例子</span><span class="sxs-lookup"><span data-stu-id="de245-107">EXAMPLES</span></span>

### <span data-ttu-id="de245-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="de245-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="de245-109">啟動作業以新增指定的磁片組配置以保護。</span><span class="sxs-lookup"><span data-stu-id="de245-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="de245-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="de245-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="de245-111">啟動作業以新增指定的磁片組配置以保護。管道輸入複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="de245-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="de245-112">參數</span><span class="sxs-lookup"><span data-stu-id="de245-112">PARAMETERS</span></span>

### <span data-ttu-id="de245-113">-AzureToAzureAzlicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="de245-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="de245-114">指定用於 Azure 到 Azure 災害復原案例之磁片保護的磁片組配置。</span><span class="sxs-lookup"><span data-stu-id="de245-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de245-115">-DefaultProfile</span></span>
<span data-ttu-id="de245-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de245-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de245-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de245-117">-InputObject</span></span>
<span data-ttu-id="de245-118">Cmdlet 的輸入物件：對應至新磁片的 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="de245-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de245-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="de245-119">-WaitForCompletion</span></span>
<span data-ttu-id="de245-120">等待完成</span><span class="sxs-lookup"><span data-stu-id="de245-120">Wait For Completion</span></span>

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

### <span data-ttu-id="de245-121">-確認</span><span class="sxs-lookup"><span data-stu-id="de245-121">-Confirm</span></span>
<span data-ttu-id="de245-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de245-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de245-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de245-123">-WhatIf</span></span>
<span data-ttu-id="de245-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de245-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de245-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de245-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de245-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de245-126">CommonParameters</span></span>
<span data-ttu-id="de245-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de245-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de245-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de245-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de245-129">輸入</span><span class="sxs-lookup"><span data-stu-id="de245-129">INPUTS</span></span>

### <span data-ttu-id="de245-130">沒有</span><span class="sxs-lookup"><span data-stu-id="de245-130">None</span></span>

## <span data-ttu-id="de245-131">輸出</span><span class="sxs-lookup"><span data-stu-id="de245-131">OUTPUTS</span></span>

### <span data-ttu-id="de245-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="de245-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="de245-133">筆記</span><span class="sxs-lookup"><span data-stu-id="de245-133">NOTES</span></span>

## <span data-ttu-id="de245-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="de245-134">RELATED LINKS</span></span>
