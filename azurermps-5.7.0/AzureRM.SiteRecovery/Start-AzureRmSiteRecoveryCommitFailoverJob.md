---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverycommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 839855b9b56e4ecc73552af310af7221c9b7b2d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453995"
---
# <span data-ttu-id="434e3-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="434e3-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="434e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="434e3-102">SYNOPSIS</span></span>
<span data-ttu-id="434e3-103">啟動針對網站復原物件的 [確認容錯移轉] 動作。</span><span class="sxs-lookup"><span data-stu-id="434e3-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="434e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="434e3-104">SYNTAX</span></span>

### <span data-ttu-id="434e3-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="434e3-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434e3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="434e3-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434e3-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="434e3-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="434e3-108">說明</span><span class="sxs-lookup"><span data-stu-id="434e3-108">DESCRIPTION</span></span>
<span data-ttu-id="434e3-109">在容錯移轉作業之後， **Start AzureRmSiteRecoveryCommitFailoverJob** Cmdlet 會啟動 Azure Site Recovery 物件的 commit 容錯移轉進程。</span><span class="sxs-lookup"><span data-stu-id="434e3-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="434e3-110">示例</span><span class="sxs-lookup"><span data-stu-id="434e3-110">EXAMPLES</span></span>

## <span data-ttu-id="434e3-111">參數</span><span class="sxs-lookup"><span data-stu-id="434e3-111">PARAMETERS</span></span>

### <span data-ttu-id="434e3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434e3-112">-DefaultProfile</span></span>
<span data-ttu-id="434e3-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="434e3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="434e3-114">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="434e3-114">-ProtectionEntity</span></span>
<span data-ttu-id="434e3-115">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="434e3-115">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="434e3-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="434e3-116">-RecoveryPlan</span></span>
<span data-ttu-id="434e3-117">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="434e3-117">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="434e3-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="434e3-118">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="434e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434e3-119">CommonParameters</span></span>
<span data-ttu-id="434e3-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="434e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434e3-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="434e3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434e3-122">輸入</span><span class="sxs-lookup"><span data-stu-id="434e3-122">INPUTS</span></span>

### <span data-ttu-id="434e3-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="434e3-123">ASRProtectionEntity</span></span>
<span data-ttu-id="434e3-124">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="434e3-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="434e3-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="434e3-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="434e3-126">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="434e3-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="434e3-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="434e3-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="434e3-128">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="434e3-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="434e3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="434e3-129">OUTPUTS</span></span>

### <span data-ttu-id="434e3-130">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="434e3-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="434e3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="434e3-131">NOTES</span></span>

## <span data-ttu-id="434e3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="434e3-132">RELATED LINKS</span></span>

