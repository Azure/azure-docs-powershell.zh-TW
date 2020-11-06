---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447936"
---
# <span data-ttu-id="42619-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="42619-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="42619-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42619-102">SYNOPSIS</span></span>
<span data-ttu-id="42619-103">更新來源和目標伺服器，以保護網站恢復物件。</span><span class="sxs-lookup"><span data-stu-id="42619-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42619-104">句法</span><span class="sxs-lookup"><span data-stu-id="42619-104">SYNTAX</span></span>

### <span data-ttu-id="42619-105">ByPEObject (預設) </span><span class="sxs-lookup"><span data-stu-id="42619-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42619-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="42619-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42619-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="42619-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42619-108">說明</span><span class="sxs-lookup"><span data-stu-id="42619-108">DESCRIPTION</span></span>
<span data-ttu-id="42619-109">**更新-AzureRmSiteRecoveryProtectionDirection** Cmdlet 會更新來源和目標伺服器，以在完成認可式容錯移轉作業之後，保護 Azure Site Recovery 物件。</span><span class="sxs-lookup"><span data-stu-id="42619-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="42619-110">示例</span><span class="sxs-lookup"><span data-stu-id="42619-110">EXAMPLES</span></span>

## <span data-ttu-id="42619-111">參數</span><span class="sxs-lookup"><span data-stu-id="42619-111">PARAMETERS</span></span>

### <span data-ttu-id="42619-112">方向</span><span class="sxs-lookup"><span data-stu-id="42619-112">-Direction</span></span>
<span data-ttu-id="42619-113">指定認可的方向。</span><span class="sxs-lookup"><span data-stu-id="42619-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="42619-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="42619-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42619-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="42619-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="42619-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="42619-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42619-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="42619-117">-ProtectionEntity</span></span>
<span data-ttu-id="42619-118">指定保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="42619-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42619-119">-RecoveryPlan</span></span>
<span data-ttu-id="42619-120">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="42619-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="42619-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42619-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42619-122">-DefaultProfile</span></span>
<span data-ttu-id="42619-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42619-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42619-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42619-124">CommonParameters</span></span>
<span data-ttu-id="42619-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42619-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42619-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42619-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42619-127">輸入</span><span class="sxs-lookup"><span data-stu-id="42619-127">INPUTS</span></span>

### <span data-ttu-id="42619-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="42619-128">ASRProtectionEntity</span></span>
<span data-ttu-id="42619-129">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="42619-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="42619-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42619-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="42619-131">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="42619-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="42619-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="42619-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="42619-133">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="42619-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="42619-134">輸出</span><span class="sxs-lookup"><span data-stu-id="42619-134">OUTPUTS</span></span>

### <span data-ttu-id="42619-135">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="42619-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42619-136">筆記</span><span class="sxs-lookup"><span data-stu-id="42619-136">NOTES</span></span>

## <span data-ttu-id="42619-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="42619-137">RELATED LINKS</span></span>

