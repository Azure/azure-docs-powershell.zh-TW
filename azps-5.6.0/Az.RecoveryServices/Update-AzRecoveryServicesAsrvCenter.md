---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d19455e4b467846ce38541ca3b0ec02f586cf226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906430"
---
# <span data-ttu-id="c08cb-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="c08cb-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="c08cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c08cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c08cb-103">更新已登錄 vCenter的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c08cb-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="c08cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="c08cb-104">SYNTAX</span></span>

### <span data-ttu-id="c08cb-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c08cb-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08cb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c08cb-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c08cb-107">描述</span><span class="sxs-lookup"><span data-stu-id="c08cb-107">DESCRIPTION</span></span>
<span data-ttu-id="c08cb-108">**Update-AzRecoveryServicesAsrvCenter** Cmdlet 是已登錄 vCenter的更新探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c08cb-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="c08cb-109">例子</span><span class="sxs-lookup"><span data-stu-id="c08cb-109">EXAMPLES</span></span>

### <span data-ttu-id="c08cb-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c08cb-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="c08cb-111">更新已登錄 vCenter的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c08cb-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="c08cb-112">參數</span><span class="sxs-lookup"><span data-stu-id="c08cb-112">PARAMETERS</span></span>

### <span data-ttu-id="c08cb-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c08cb-113">-Account</span></span>
<span data-ttu-id="c08cb-114">vCenter登入認證帳戶。</span><span class="sxs-lookup"><span data-stu-id="c08cb-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="c08cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08cb-115">-DefaultProfile</span></span>
<span data-ttu-id="c08cb-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c08cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c08cb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c08cb-117">-InputObject</span></span>
<span data-ttu-id="c08cb-118">要更新探索詳細資料之 vCenter 伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="c08cb-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="c08cb-119">-埠</span><span class="sxs-lookup"><span data-stu-id="c08cb-119">-Port</span></span>
<span data-ttu-id="c08cb-120">vCenter 伺服器上用於探索的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="c08cb-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="c08cb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c08cb-121">-ResourceId</span></span>
<span data-ttu-id="c08cb-122">指定 vCenter 的資源Id。</span><span class="sxs-lookup"><span data-stu-id="c08cb-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="c08cb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c08cb-123">-Confirm</span></span>
<span data-ttu-id="c08cb-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c08cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08cb-125">-WhatIf</span></span>
<span data-ttu-id="c08cb-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c08cb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c08cb-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c08cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08cb-128">CommonParameters</span></span>
<span data-ttu-id="c08cb-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c08cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08cb-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c08cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08cb-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c08cb-131">INPUTS</span></span>

### <span data-ttu-id="c08cb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c08cb-132">System.String</span></span>

### <span data-ttu-id="c08cb-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="c08cb-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="c08cb-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c08cb-134">OUTPUTS</span></span>

### <span data-ttu-id="c08cb-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c08cb-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c08cb-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c08cb-136">NOTES</span></span>

## <span data-ttu-id="c08cb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c08cb-137">RELATED LINKS</span></span>
