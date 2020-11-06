---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453035"
---
# <span data-ttu-id="fbf67-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbf67-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="fbf67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbf67-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf67-103">編輯網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="fbf67-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbf67-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbf67-104">SYNTAX</span></span>

### <span data-ttu-id="fbf67-105">AppendGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="fbf67-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbf67-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="fbf67-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbf67-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="fbf67-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbf67-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="fbf67-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbf67-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="fbf67-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbf67-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="fbf67-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbf67-111">說明</span><span class="sxs-lookup"><span data-stu-id="fbf67-111">DESCRIPTION</span></span>
<span data-ttu-id="fbf67-112">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 編輯 Azure 網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="fbf67-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="fbf67-113">示例</span><span class="sxs-lookup"><span data-stu-id="fbf67-113">EXAMPLES</span></span>

## <span data-ttu-id="fbf67-114">參數</span><span class="sxs-lookup"><span data-stu-id="fbf67-114">PARAMETERS</span></span>

### <span data-ttu-id="fbf67-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="fbf67-115">-AddProtectedEntities</span></span>
<span data-ttu-id="fbf67-116">指定要新增的受保護實體陣列。</span><span class="sxs-lookup"><span data-stu-id="fbf67-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="fbf67-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="fbf67-118">-AppendGroup</span></span>
<span data-ttu-id="fbf67-119">表示此操作會將群組附加到復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="fbf67-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf67-120">-DefaultProfile</span></span>
<span data-ttu-id="fbf67-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fbf67-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbf67-122">-群組</span><span class="sxs-lookup"><span data-stu-id="fbf67-122">-Group</span></span>
<span data-ttu-id="fbf67-123">指定 [網站復原方案] 群組。</span><span class="sxs-lookup"><span data-stu-id="fbf67-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbf67-124">-RecoveryPlan</span></span>
<span data-ttu-id="fbf67-125">指定復原方案。</span><span class="sxs-lookup"><span data-stu-id="fbf67-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="fbf67-126">-RemoveGroup</span></span>
<span data-ttu-id="fbf67-127">移除指定的網站復原復原方案群組。</span><span class="sxs-lookup"><span data-stu-id="fbf67-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="fbf67-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="fbf67-129">指定受保護實體的陣列。</span><span class="sxs-lookup"><span data-stu-id="fbf67-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="fbf67-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf67-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf67-131">CommonParameters</span></span>
<span data-ttu-id="fbf67-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbf67-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf67-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbf67-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf67-134">輸入</span><span class="sxs-lookup"><span data-stu-id="fbf67-134">INPUTS</span></span>

### <span data-ttu-id="fbf67-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbf67-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="fbf67-136">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fbf67-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="fbf67-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fbf67-137">OUTPUTS</span></span>

## <span data-ttu-id="fbf67-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fbf67-138">NOTES</span></span>

## <span data-ttu-id="fbf67-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbf67-139">RELATED LINKS</span></span>

[<span data-ttu-id="fbf67-140">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbf67-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fbf67-141">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fbf67-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
