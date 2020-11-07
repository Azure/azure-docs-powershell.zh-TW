---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623849"
---
# <span data-ttu-id="9c026-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c026-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="9c026-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c026-102">SYNOPSIS</span></span>
<span data-ttu-id="9c026-103">編輯網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="9c026-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c026-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c026-104">SYNTAX</span></span>

### <span data-ttu-id="9c026-105">AppendGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="9c026-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c026-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="9c026-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c026-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="9c026-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c026-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="9c026-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c026-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9c026-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c026-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9c026-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c026-111">說明</span><span class="sxs-lookup"><span data-stu-id="9c026-111">DESCRIPTION</span></span>
<span data-ttu-id="9c026-112">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet 編輯 Azure 網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="9c026-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="9c026-113">示例</span><span class="sxs-lookup"><span data-stu-id="9c026-113">EXAMPLES</span></span>

## <span data-ttu-id="9c026-114">參數</span><span class="sxs-lookup"><span data-stu-id="9c026-114">PARAMETERS</span></span>

### <span data-ttu-id="9c026-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="9c026-115">-AddProtectedEntities</span></span>
<span data-ttu-id="9c026-116">指定要新增的受保護實體陣列。</span><span class="sxs-lookup"><span data-stu-id="9c026-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9c026-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="9c026-118">-AppendGroup</span></span>
<span data-ttu-id="9c026-119">表示此操作會將群組附加到復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="9c026-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-120">-群組</span><span class="sxs-lookup"><span data-stu-id="9c026-120">-Group</span></span>
<span data-ttu-id="9c026-121">指定 [網站復原方案] 群組。</span><span class="sxs-lookup"><span data-stu-id="9c026-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c026-122">-RecoveryPlan</span></span>
<span data-ttu-id="9c026-123">指定復原方案。</span><span class="sxs-lookup"><span data-stu-id="9c026-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="9c026-124">-RemoveGroup</span></span>
<span data-ttu-id="9c026-125">移除指定的網站復原復原方案群組。</span><span class="sxs-lookup"><span data-stu-id="9c026-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="9c026-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="9c026-127">指定受保護實體的陣列。</span><span class="sxs-lookup"><span data-stu-id="9c026-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9c026-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c026-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c026-129">-DefaultProfile</span></span>
<span data-ttu-id="9c026-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c026-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c026-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c026-131">CommonParameters</span></span>
<span data-ttu-id="9c026-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c026-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c026-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c026-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c026-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9c026-134">INPUTS</span></span>

### <span data-ttu-id="9c026-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c026-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="9c026-136">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9c026-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="9c026-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9c026-137">OUTPUTS</span></span>

## <span data-ttu-id="9c026-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9c026-138">NOTES</span></span>

## <span data-ttu-id="9c026-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c026-139">RELATED LINKS</span></span>

[<span data-ttu-id="9c026-140">AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c026-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="9c026-141">新-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9c026-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
