---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283759"
---
# <span data-ttu-id="72388-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="72388-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="72388-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72388-102">SYNOPSIS</span></span>
<span data-ttu-id="72388-103">在提交容錯移轉作業之前，變更失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="72388-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="72388-104">句法</span><span class="sxs-lookup"><span data-stu-id="72388-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72388-105">說明</span><span class="sxs-lookup"><span data-stu-id="72388-105">DESCRIPTION</span></span>
<span data-ttu-id="72388-106">在提交容錯移轉作業之前， **AzRecoveryServicesAsrApplyRecoveryPoint** 會變更已失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="72388-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="72388-107">示例</span><span class="sxs-lookup"><span data-stu-id="72388-107">EXAMPLES</span></span>

### <span data-ttu-id="72388-108">範例1</span><span class="sxs-lookup"><span data-stu-id="72388-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="72388-109">開始將指定的復原點套用至複製受保護的專案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="72388-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="72388-110">參數</span><span class="sxs-lookup"><span data-stu-id="72388-110">PARAMETERS</span></span>

### <span data-ttu-id="72388-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="72388-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="72388-112">如果正在使用資料加密，指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="72388-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72388-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="72388-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="72388-114">指定要使用資料加密的次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="72388-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72388-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72388-115">-DefaultProfile</span></span>
<span data-ttu-id="72388-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72388-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="72388-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="72388-117">-RecoveryPoint</span></span>
<span data-ttu-id="72388-118">指定對應至要套用之復原點的復原點物件。</span><span class="sxs-lookup"><span data-stu-id="72388-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72388-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72388-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="72388-120">指定 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="72388-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72388-121">-確認</span><span class="sxs-lookup"><span data-stu-id="72388-121">-Confirm</span></span>
<span data-ttu-id="72388-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72388-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72388-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72388-123">-WhatIf</span></span>
<span data-ttu-id="72388-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72388-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72388-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72388-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72388-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72388-126">CommonParameters</span></span>
<span data-ttu-id="72388-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72388-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72388-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="72388-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72388-129">輸入</span><span class="sxs-lookup"><span data-stu-id="72388-129">INPUTS</span></span>

### <span data-ttu-id="72388-130">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72388-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="72388-131">輸出</span><span class="sxs-lookup"><span data-stu-id="72388-131">OUTPUTS</span></span>

### <span data-ttu-id="72388-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="72388-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72388-133">筆記</span><span class="sxs-lookup"><span data-stu-id="72388-133">NOTES</span></span>

## <span data-ttu-id="72388-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="72388-134">RELATED LINKS</span></span>

[<span data-ttu-id="72388-135">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="72388-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
