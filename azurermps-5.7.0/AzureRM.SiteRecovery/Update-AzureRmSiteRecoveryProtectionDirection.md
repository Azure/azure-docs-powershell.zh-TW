---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: f7d8efcde5f60ed9cf6eb3aff7f86c9ea3171ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444307"
---
# <span data-ttu-id="1a6b7-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="1a6b7-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="1a6b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6b7-103">更新來源和目標伺服器，以保護網站恢復物件。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a6b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a6b7-104">SYNTAX</span></span>

### <span data-ttu-id="1a6b7-105">ByPEObject (預設) </span><span class="sxs-lookup"><span data-stu-id="1a6b7-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a6b7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1a6b7-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a6b7-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="1a6b7-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a6b7-108">說明</span><span class="sxs-lookup"><span data-stu-id="1a6b7-108">DESCRIPTION</span></span>
<span data-ttu-id="1a6b7-109">**更新-AzureRmSiteRecoveryProtectionDirection** Cmdlet 會更新來源和目標伺服器，以在完成認可式容錯移轉作業之後，保護 Azure Site Recovery 物件。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="1a6b7-110">示例</span><span class="sxs-lookup"><span data-stu-id="1a6b7-110">EXAMPLES</span></span>

## <span data-ttu-id="1a6b7-111">參數</span><span class="sxs-lookup"><span data-stu-id="1a6b7-111">PARAMETERS</span></span>

### <span data-ttu-id="1a6b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6b7-112">-DefaultProfile</span></span>
<span data-ttu-id="1a6b7-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a6b7-114">方向</span><span class="sxs-lookup"><span data-stu-id="1a6b7-114">-Direction</span></span>
<span data-ttu-id="1a6b7-115">指定認可的方向。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-115">Specifies the direction of the commit.</span></span>
<span data-ttu-id="1a6b7-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1a6b7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a6b7-117">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1a6b7-117">PrimaryToRecovery</span></span>
- <span data-ttu-id="1a6b7-118">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1a6b7-118">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a6b7-119">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1a6b7-119">-ProtectionEntity</span></span>
<span data-ttu-id="1a6b7-120">指定保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-120">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="1a6b7-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6b7-121">-RecoveryPlan</span></span>
<span data-ttu-id="1a6b7-122">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-122">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="1a6b7-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1a6b7-123">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="1a6b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6b7-124">CommonParameters</span></span>
<span data-ttu-id="1a6b7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6b7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a6b7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6b7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1a6b7-127">INPUTS</span></span>

### <span data-ttu-id="1a6b7-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1a6b7-128">ASRProtectionEntity</span></span>
<span data-ttu-id="1a6b7-129">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1a6b7-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="1a6b7-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6b7-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="1a6b7-131">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1a6b7-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="1a6b7-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1a6b7-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="1a6b7-133">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1a6b7-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="1a6b7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1a6b7-134">OUTPUTS</span></span>

### <span data-ttu-id="1a6b7-135">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1a6b7-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a6b7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1a6b7-136">NOTES</span></span>

## <span data-ttu-id="1a6b7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a6b7-137">RELATED LINKS</span></span>

