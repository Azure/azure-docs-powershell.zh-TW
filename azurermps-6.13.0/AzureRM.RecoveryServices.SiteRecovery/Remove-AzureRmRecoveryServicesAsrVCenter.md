---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454568"
---
# <span data-ttu-id="066db-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="066db-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="066db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="066db-102">SYNOPSIS</span></span>
<span data-ttu-id="066db-103">從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="066db-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="066db-104">句法</span><span class="sxs-lookup"><span data-stu-id="066db-104">SYNTAX</span></span>

### <span data-ttu-id="066db-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="066db-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066db-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="066db-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066db-107">ByName</span><span class="sxs-lookup"><span data-stu-id="066db-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="066db-108">說明</span><span class="sxs-lookup"><span data-stu-id="066db-108">DESCRIPTION</span></span>
<span data-ttu-id="066db-109">**AzureRmRecoveryServicesAsrvCenter** Cmdlet 會從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="066db-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="066db-110">示例</span><span class="sxs-lookup"><span data-stu-id="066db-110">EXAMPLES</span></span>

### <span data-ttu-id="066db-111">範例1</span><span class="sxs-lookup"><span data-stu-id="066db-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="066db-112">從 ASR 結構中移除 vCenter 伺服器。</span><span class="sxs-lookup"><span data-stu-id="066db-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="066db-113">參數</span><span class="sxs-lookup"><span data-stu-id="066db-113">PARAMETERS</span></span>

### <span data-ttu-id="066db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066db-114">-DefaultProfile</span></span>
<span data-ttu-id="066db-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="066db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="066db-116">-結構</span><span class="sxs-lookup"><span data-stu-id="066db-116">-Fabric</span></span>
<span data-ttu-id="066db-117">代表佈建服務器的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="066db-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="066db-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="066db-118">-InputObject</span></span>
<span data-ttu-id="066db-119">要移除的 vCenter 伺服器所代表的 ASR vCenter 物件。</span><span class="sxs-lookup"><span data-stu-id="066db-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="066db-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="066db-120">-Name</span></span>
<span data-ttu-id="066db-121">VCenter 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="066db-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066db-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="066db-122">-ResourceId</span></span>
<span data-ttu-id="066db-123">指定要移除的 vCenter resourceId。</span><span class="sxs-lookup"><span data-stu-id="066db-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066db-124">-確認</span><span class="sxs-lookup"><span data-stu-id="066db-124">-Confirm</span></span>
<span data-ttu-id="066db-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="066db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066db-126">-WhatIf</span></span>
<span data-ttu-id="066db-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="066db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="066db-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="066db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066db-129">CommonParameters</span></span>
<span data-ttu-id="066db-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="066db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066db-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="066db-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066db-132">輸入</span><span class="sxs-lookup"><span data-stu-id="066db-132">INPUTS</span></span>

### <span data-ttu-id="066db-133">RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="066db-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="066db-134">輸出</span><span class="sxs-lookup"><span data-stu-id="066db-134">OUTPUTS</span></span>

### <span data-ttu-id="066db-135">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 0.1.1.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="066db-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="066db-136">筆記</span><span class="sxs-lookup"><span data-stu-id="066db-136">NOTES</span></span>

## <span data-ttu-id="066db-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="066db-137">RELATED LINKS</span></span>
