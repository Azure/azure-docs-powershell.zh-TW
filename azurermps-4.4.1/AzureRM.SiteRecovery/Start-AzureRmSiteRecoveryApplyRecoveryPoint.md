---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447947"
---
# <span data-ttu-id="528e6-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="528e6-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="528e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="528e6-102">SYNOPSIS</span></span>
<span data-ttu-id="528e6-103">在提交容錯移轉作業之前，變更失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="528e6-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="528e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="528e6-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="528e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="528e6-105">DESCRIPTION</span></span>
<span data-ttu-id="528e6-106">在提交容錯移轉作業之前， **AzureRmSiteRecoveryApplyRecoveryPoint** 會變更受保護的專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="528e6-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="528e6-107">示例</span><span class="sxs-lookup"><span data-stu-id="528e6-107">EXAMPLES</span></span>

## <span data-ttu-id="528e6-108">參數</span><span class="sxs-lookup"><span data-stu-id="528e6-108">PARAMETERS</span></span>

### <span data-ttu-id="528e6-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="528e6-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="528e6-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="528e6-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="528e6-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="528e6-111">-RecoveryPoint</span></span>
<span data-ttu-id="528e6-112">指定此 Cmdlet 變更的復原點物件。</span><span class="sxs-lookup"><span data-stu-id="528e6-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="528e6-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="528e6-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="528e6-114">指定複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="528e6-114">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="528e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528e6-115">-DefaultProfile</span></span>
<span data-ttu-id="528e6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="528e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="528e6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528e6-117">CommonParameters</span></span>
<span data-ttu-id="528e6-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="528e6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528e6-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="528e6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528e6-120">輸入</span><span class="sxs-lookup"><span data-stu-id="528e6-120">INPUTS</span></span>

### <span data-ttu-id="528e6-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="528e6-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="528e6-122">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="528e6-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="528e6-123">輸出</span><span class="sxs-lookup"><span data-stu-id="528e6-123">OUTPUTS</span></span>

### <span data-ttu-id="528e6-124">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="528e6-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="528e6-125">筆記</span><span class="sxs-lookup"><span data-stu-id="528e6-125">NOTES</span></span>

## <span data-ttu-id="528e6-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="528e6-126">RELATED LINKS</span></span>

[<span data-ttu-id="528e6-127">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="528e6-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
