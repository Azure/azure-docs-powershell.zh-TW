---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444428"
---
# <span data-ttu-id="f638c-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f638c-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="f638c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f638c-102">SYNOPSIS</span></span>
<span data-ttu-id="f638c-103">在提交容錯移轉作業之前，變更失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="f638c-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f638c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f638c-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f638c-105">說明</span><span class="sxs-lookup"><span data-stu-id="f638c-105">DESCRIPTION</span></span>
<span data-ttu-id="f638c-106">在提交容錯移轉作業之前， **AzureRmRecoveryServicesAsrApplyRecoveryPoint** 會變更已失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="f638c-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="f638c-107">示例</span><span class="sxs-lookup"><span data-stu-id="f638c-107">EXAMPLES</span></span>

### <span data-ttu-id="f638c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f638c-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="f638c-109">開始將指定的復原點套用至複製受保護的專案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f638c-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f638c-110">參數</span><span class="sxs-lookup"><span data-stu-id="f638c-110">PARAMETERS</span></span>

### <span data-ttu-id="f638c-111">-確認</span><span class="sxs-lookup"><span data-stu-id="f638c-111">-Confirm</span></span>
<span data-ttu-id="f638c-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f638c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f638c-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f638c-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f638c-114">如果正在使用資料加密，指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="f638c-114">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f638c-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f638c-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f638c-116">指定要使用資料加密的次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="f638c-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f638c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f638c-117">-DefaultProfile</span></span>
<span data-ttu-id="f638c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f638c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f638c-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f638c-119">-RecoveryPoint</span></span>
<span data-ttu-id="f638c-120">指定對應至要套用之復原點的復原點物件。</span><span class="sxs-lookup"><span data-stu-id="f638c-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f638c-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f638c-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f638c-122">指定 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="f638c-122">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f638c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f638c-123">-WhatIf</span></span>
<span data-ttu-id="f638c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f638c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f638c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f638c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f638c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f638c-126">CommonParameters</span></span>
<span data-ttu-id="f638c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f638c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f638c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f638c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f638c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f638c-129">INPUTS</span></span>

### <span data-ttu-id="f638c-130">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f638c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f638c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f638c-131">OUTPUTS</span></span>

### <span data-ttu-id="f638c-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f638c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f638c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f638c-133">NOTES</span></span>

## <span data-ttu-id="f638c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f638c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f638c-135">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f638c-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)