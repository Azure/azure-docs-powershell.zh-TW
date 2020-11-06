---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 856a316104e0e660f170de8f519dbcb66c55bd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455088"
---
# <span data-ttu-id="69bc8-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="69bc8-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="69bc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="69bc8-103">更新已註冊 vCenter 的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="69bc8-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69bc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="69bc8-104">SYNTAX</span></span>

### <span data-ttu-id="69bc8-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="69bc8-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69bc8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="69bc8-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69bc8-107">說明</span><span class="sxs-lookup"><span data-stu-id="69bc8-107">DESCRIPTION</span></span>
<span data-ttu-id="69bc8-108">**AzureRmRecoveryServicesAsrvCenter** Cmdlet 會更新已註冊 vCenter 的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="69bc8-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="69bc8-109">示例</span><span class="sxs-lookup"><span data-stu-id="69bc8-109">EXAMPLES</span></span>

### <span data-ttu-id="69bc8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="69bc8-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="69bc8-111">更新已註冊 vCenter 的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="69bc8-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="69bc8-112">參數</span><span class="sxs-lookup"><span data-stu-id="69bc8-112">PARAMETERS</span></span>

### <span data-ttu-id="69bc8-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="69bc8-113">-Account</span></span>
<span data-ttu-id="69bc8-114">vCenter 登入認證帳戶。</span><span class="sxs-lookup"><span data-stu-id="69bc8-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bc8-115">-DefaultProfile</span></span>
<span data-ttu-id="69bc8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69bc8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69bc8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69bc8-117">-InputObject</span></span>
<span data-ttu-id="69bc8-118">要更新其探索詳細資料的 vCenter 伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="69bc8-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="69bc8-119">-埠</span><span class="sxs-lookup"><span data-stu-id="69bc8-119">-Port</span></span>
<span data-ttu-id="69bc8-120">VCenter 伺服器上用來進行探索的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="69bc8-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bc8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69bc8-121">-ResourceId</span></span>
<span data-ttu-id="69bc8-122">指定 vCenter 的 resourceId。</span><span class="sxs-lookup"><span data-stu-id="69bc8-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="69bc8-123">-確認</span><span class="sxs-lookup"><span data-stu-id="69bc8-123">-Confirm</span></span>
<span data-ttu-id="69bc8-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69bc8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bc8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bc8-125">-WhatIf</span></span>
<span data-ttu-id="69bc8-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69bc8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bc8-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69bc8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bc8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bc8-128">CommonParameters</span></span>
<span data-ttu-id="69bc8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69bc8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bc8-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69bc8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bc8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="69bc8-131">INPUTS</span></span>

### <span data-ttu-id="69bc8-132">RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="69bc8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="69bc8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="69bc8-133">OUTPUTS</span></span>

### <span data-ttu-id="69bc8-134">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 0.1.1.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="69bc8-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="69bc8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="69bc8-135">NOTES</span></span>

## <span data-ttu-id="69bc8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="69bc8-136">RELATED LINKS</span></span>
