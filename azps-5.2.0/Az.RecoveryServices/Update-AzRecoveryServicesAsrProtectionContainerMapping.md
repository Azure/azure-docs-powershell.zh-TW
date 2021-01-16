---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276207"
---
# <span data-ttu-id="14ec4-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="14ec4-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="14ec4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="14ec4-103">更新 Azure site recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="14ec4-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="14ec4-104">句法</span><span class="sxs-lookup"><span data-stu-id="14ec4-104">SYNTAX</span></span>

### <span data-ttu-id="14ec4-105">AzureToAzureEnableAutoUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="14ec4-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14ec4-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="14ec4-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14ec4-107">說明</span><span class="sxs-lookup"><span data-stu-id="14ec4-107">DESCRIPTION</span></span>
<span data-ttu-id="14ec4-108">**更新-AzRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會更新指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="14ec4-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="14ec4-109">示例</span><span class="sxs-lookup"><span data-stu-id="14ec4-109">EXAMPLES</span></span>

### <span data-ttu-id="14ec4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="14ec4-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="14ec4-111">啟動操作以停用容器的自動更新。</span><span class="sxs-lookup"><span data-stu-id="14ec4-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="14ec4-112">範例2</span><span class="sxs-lookup"><span data-stu-id="14ec4-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="14ec4-113">啟動作業來停用 [啟用容器的自動更新]。</span><span class="sxs-lookup"><span data-stu-id="14ec4-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="14ec4-114">參數</span><span class="sxs-lookup"><span data-stu-id="14ec4-114">PARAMETERS</span></span>

### <span data-ttu-id="14ec4-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="14ec4-115">-AutomationAccountId</span></span>
<span data-ttu-id="14ec4-116">指定用於自動 udpate 的自動化 accountId。</span><span class="sxs-lookup"><span data-stu-id="14ec4-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="14ec4-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="14ec4-117">-AzureToAzure</span></span>
<span data-ttu-id="14ec4-118">指定 Azure 到 Azure 保護容器。</span><span class="sxs-lookup"><span data-stu-id="14ec4-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="14ec4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ec4-119">-DefaultProfile</span></span>
<span data-ttu-id="14ec4-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14ec4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14ec4-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="14ec4-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="14ec4-122">切換參數以停用自動更新。</span><span class="sxs-lookup"><span data-stu-id="14ec4-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="14ec4-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="14ec4-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="14ec4-124">[切換參數] 可啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="14ec4-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="14ec4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14ec4-125">-InputObject</span></span>
<span data-ttu-id="14ec4-126">[保護容器對應的物件]。</span><span class="sxs-lookup"><span data-stu-id="14ec4-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="14ec4-127">-確認</span><span class="sxs-lookup"><span data-stu-id="14ec4-127">-Confirm</span></span>
<span data-ttu-id="14ec4-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14ec4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14ec4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14ec4-129">-WhatIf</span></span>
<span data-ttu-id="14ec4-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14ec4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14ec4-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14ec4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14ec4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ec4-132">CommonParameters</span></span>
<span data-ttu-id="14ec4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14ec4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ec4-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14ec4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ec4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="14ec4-135">INPUTS</span></span>

### <span data-ttu-id="14ec4-136">RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="14ec4-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="14ec4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="14ec4-137">OUTPUTS</span></span>

### <span data-ttu-id="14ec4-138">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="14ec4-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="14ec4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="14ec4-139">NOTES</span></span>

## <span data-ttu-id="14ec4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="14ec4-140">RELATED LINKS</span></span>
