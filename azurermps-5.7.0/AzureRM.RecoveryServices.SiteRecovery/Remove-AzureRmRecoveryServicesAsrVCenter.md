---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448611"
---
# <span data-ttu-id="00cd1-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="00cd1-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="00cd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="00cd1-103">從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="00cd1-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00cd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="00cd1-104">SYNTAX</span></span>

### <span data-ttu-id="00cd1-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="00cd1-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00cd1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00cd1-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00cd1-107">ByName</span><span class="sxs-lookup"><span data-stu-id="00cd1-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00cd1-108">說明</span><span class="sxs-lookup"><span data-stu-id="00cd1-108">DESCRIPTION</span></span>
<span data-ttu-id="00cd1-109">**AzureRmRecoveryServicesAsrvCenter** Cmdlet 會從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="00cd1-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="00cd1-110">示例</span><span class="sxs-lookup"><span data-stu-id="00cd1-110">EXAMPLES</span></span>

### <span data-ttu-id="00cd1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="00cd1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="00cd1-112">從 ASR 結構中移除 vCenter 伺服器。</span><span class="sxs-lookup"><span data-stu-id="00cd1-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="00cd1-113">參數</span><span class="sxs-lookup"><span data-stu-id="00cd1-113">PARAMETERS</span></span>

### <span data-ttu-id="00cd1-114">-確認</span><span class="sxs-lookup"><span data-stu-id="00cd1-114">-Confirm</span></span>
<span data-ttu-id="00cd1-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00cd1-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00cd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00cd1-116">-DefaultProfile</span></span>
<span data-ttu-id="00cd1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00cd1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00cd1-118">-結構</span><span class="sxs-lookup"><span data-stu-id="00cd1-118">-Fabric</span></span>
<span data-ttu-id="00cd1-119">代表佈建服務器的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="00cd1-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00cd1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00cd1-120">-InputObject</span></span>
<span data-ttu-id="00cd1-121">要移除的 vCenter 伺服器所代表的 ASR vCenter 物件。</span><span class="sxs-lookup"><span data-stu-id="00cd1-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00cd1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="00cd1-122">-Name</span></span>
<span data-ttu-id="00cd1-123">VCenter 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="00cd1-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00cd1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00cd1-124">-ResourceId</span></span>
<span data-ttu-id="00cd1-125">指定要移除的 vCenter resourceId。</span><span class="sxs-lookup"><span data-stu-id="00cd1-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00cd1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00cd1-126">-WhatIf</span></span>
<span data-ttu-id="00cd1-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00cd1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00cd1-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00cd1-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00cd1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00cd1-129">CommonParameters</span></span>
<span data-ttu-id="00cd1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00cd1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00cd1-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00cd1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00cd1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="00cd1-132">INPUTS</span></span>

### <span data-ttu-id="00cd1-133">RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="00cd1-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="00cd1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="00cd1-134">OUTPUTS</span></span>

### <span data-ttu-id="00cd1-135">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 0.1.1.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="00cd1-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="00cd1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="00cd1-136">NOTES</span></span>

## <span data-ttu-id="00cd1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="00cd1-137">RELATED LINKS</span></span>
