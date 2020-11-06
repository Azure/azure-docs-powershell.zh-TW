---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bd8a06eb85658fe2ec06d65c0663550be78d1552
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445571"
---
# <span data-ttu-id="dbc4b-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbc4b-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="dbc4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc4b-103">停止/停用 Azure Site Recovery 複製受保護的專案的複製。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbc4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbc4b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbc4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbc4b-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc4b-106">**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會停用對指定的 Azure 網站復原複製受保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="dbc4b-107">這個操作會導致複製停止受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="dbc4b-108">示例</span><span class="sxs-lookup"><span data-stu-id="dbc4b-108">EXAMPLES</span></span>

### <span data-ttu-id="dbc4b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="dbc4b-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="dbc4b-110">針對指定的複製受保護專案啟動 [停用複製] 作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dbc4b-111">參數</span><span class="sxs-lookup"><span data-stu-id="dbc4b-111">PARAMETERS</span></span>

### <span data-ttu-id="dbc4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc4b-112">-DefaultProfile</span></span>
<span data-ttu-id="dbc4b-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dbc4b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dbc4b-114">-Force</span></span>
<span data-ttu-id="dbc4b-115">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="dbc4b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbc4b-116">-InputObject</span></span>
<span data-ttu-id="dbc4b-117">Cmdlet 的輸入物件：對應到要停用複製之受複製受保護專案的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="dbc4b-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="dbc4b-118">-WaitForCompletion</span></span>
<span data-ttu-id="dbc4b-119">指示在傳回前，該指令必須等待操作完成。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="dbc4b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="dbc4b-120">-Confirm</span></span>
<span data-ttu-id="dbc4b-121">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-121">Specify if confirmation is required.</span></span> <span data-ttu-id="dbc4b-122">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="dbc4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc4b-123">-WhatIf</span></span>
<span data-ttu-id="dbc4b-124">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="dbc4b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc4b-125">CommonParameters</span></span>
<span data-ttu-id="dbc4b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc4b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dbc4b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc4b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="dbc4b-128">INPUTS</span></span>

### <span data-ttu-id="dbc4b-129">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbc4b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="dbc4b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dbc4b-130">OUTPUTS</span></span>

### <span data-ttu-id="dbc4b-131">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dbc4b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dbc4b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dbc4b-132">NOTES</span></span>

## <span data-ttu-id="dbc4b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbc4b-133">RELATED LINKS</span></span>

[<span data-ttu-id="dbc4b-134">AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbc4b-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="dbc4b-135">新-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbc4b-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="dbc4b-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbc4b-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
