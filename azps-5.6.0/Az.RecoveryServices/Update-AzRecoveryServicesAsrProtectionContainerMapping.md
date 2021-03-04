---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 29c996036705e3fc71f1c6a04ead16c24b1b3bca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901673"
---
# <span data-ttu-id="d498f-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d498f-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d498f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d498f-102">SYNOPSIS</span></span>
<span data-ttu-id="d498f-103">更新 Azure 網站復原保護容器的映射。</span><span class="sxs-lookup"><span data-stu-id="d498f-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="d498f-104">語法</span><span class="sxs-lookup"><span data-stu-id="d498f-104">SYNTAX</span></span>

### <span data-ttu-id="d498f-105">AzureToAzureEnableAutoUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="d498f-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d498f-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="d498f-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d498f-107">描述</span><span class="sxs-lookup"><span data-stu-id="d498f-107">DESCRIPTION</span></span>
<span data-ttu-id="d498f-108">**Update-AzRecoveryServicesAsrProtectionContainerMadlet** 會更新指定的 Azure 網站復原保護容器地圖。</span><span class="sxs-lookup"><span data-stu-id="d498f-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="d498f-109">例子</span><span class="sxs-lookup"><span data-stu-id="d498f-109">EXAMPLES</span></span>

### <span data-ttu-id="d498f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d498f-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="d498f-111">啟動作業以停用容器的自動更新。</span><span class="sxs-lookup"><span data-stu-id="d498f-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="d498f-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d498f-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="d498f-113">啟動作業以停用容器的啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="d498f-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="d498f-114">參數</span><span class="sxs-lookup"><span data-stu-id="d498f-114">PARAMETERS</span></span>

### <span data-ttu-id="d498f-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="d498f-115">-AutomationAccountId</span></span>
<span data-ttu-id="d498f-116">指定用於自動 udpate 的自動化 accountId。</span><span class="sxs-lookup"><span data-stu-id="d498f-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d498f-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d498f-117">-AzureToAzure</span></span>
<span data-ttu-id="d498f-118">指定 Azure 到 Azure 保護容器。</span><span class="sxs-lookup"><span data-stu-id="d498f-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d498f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d498f-119">-DefaultProfile</span></span>
<span data-ttu-id="d498f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d498f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d498f-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="d498f-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="d498f-122">切換參數以停用自動更新。</span><span class="sxs-lookup"><span data-stu-id="d498f-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d498f-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="d498f-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="d498f-124">切換參數以啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="d498f-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d498f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d498f-125">-InputObject</span></span>
<span data-ttu-id="d498f-126">用於保護容器地圖的物件。</span><span class="sxs-lookup"><span data-stu-id="d498f-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d498f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d498f-127">-Confirm</span></span>
<span data-ttu-id="d498f-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d498f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d498f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d498f-129">-WhatIf</span></span>
<span data-ttu-id="d498f-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d498f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d498f-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d498f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d498f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d498f-132">CommonParameters</span></span>
<span data-ttu-id="d498f-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d498f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d498f-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d498f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d498f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d498f-135">INPUTS</span></span>

### <span data-ttu-id="d498f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d498f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="d498f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d498f-137">OUTPUTS</span></span>

### <span data-ttu-id="d498f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d498f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d498f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d498f-139">NOTES</span></span>

## <span data-ttu-id="d498f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d498f-140">RELATED LINKS</span></span>
