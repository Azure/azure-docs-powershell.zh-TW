---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: 97ebacf9f5c51778122bfb8e8157692b7f1dfd03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453999"
---
# <span data-ttu-id="9cad9-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9cad9-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="9cad9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cad9-102">SYNOPSIS</span></span>
<span data-ttu-id="9cad9-103">在提交容錯移轉作業之前，變更失敗的受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="9cad9-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cad9-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cad9-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cad9-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cad9-105">DESCRIPTION</span></span>
<span data-ttu-id="9cad9-106">在提交容錯移轉作業之前， **AzureRmSiteRecoveryApplyRecoveryPoint** 會變更受保護的專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="9cad9-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="9cad9-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cad9-107">EXAMPLES</span></span>

## <span data-ttu-id="9cad9-108">參數</span><span class="sxs-lookup"><span data-stu-id="9cad9-108">PARAMETERS</span></span>

### <span data-ttu-id="9cad9-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9cad9-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="9cad9-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9cad9-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="9cad9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cad9-111">-DefaultProfile</span></span>
<span data-ttu-id="9cad9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cad9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cad9-113">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9cad9-113">-RecoveryPoint</span></span>
<span data-ttu-id="9cad9-114">指定此 Cmdlet 變更的復原點物件。</span><span class="sxs-lookup"><span data-stu-id="9cad9-114">Specifies the recovery point object that this cmdlet changes.</span></span>

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

### <span data-ttu-id="9cad9-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9cad9-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9cad9-116">指定複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="9cad9-116">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="9cad9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cad9-117">CommonParameters</span></span>
<span data-ttu-id="9cad9-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cad9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cad9-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cad9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cad9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9cad9-120">INPUTS</span></span>

### <span data-ttu-id="9cad9-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9cad9-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="9cad9-122">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9cad9-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="9cad9-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9cad9-123">OUTPUTS</span></span>

### <span data-ttu-id="9cad9-124">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9cad9-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9cad9-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9cad9-125">NOTES</span></span>

## <span data-ttu-id="9cad9-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cad9-126">RELATED LINKS</span></span>

[<span data-ttu-id="9cad9-127">Azure Site Recovery Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9cad9-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
