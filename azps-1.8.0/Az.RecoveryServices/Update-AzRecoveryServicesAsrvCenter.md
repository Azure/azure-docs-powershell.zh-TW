---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d6e26eb293a2b87fccc0749b6d5c53d15d7d860f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621013"
---
# <span data-ttu-id="a544d-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="a544d-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="a544d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a544d-102">SYNOPSIS</span></span>
<span data-ttu-id="a544d-103">更新已註冊 vCenter 的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a544d-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="a544d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a544d-104">SYNTAX</span></span>

### <span data-ttu-id="a544d-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a544d-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a544d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a544d-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a544d-107">說明</span><span class="sxs-lookup"><span data-stu-id="a544d-107">DESCRIPTION</span></span>
<span data-ttu-id="a544d-108">**AzRecoveryServicesAsrvCenter** Cmdlet 會更新已註冊 vCenter 的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a544d-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="a544d-109">示例</span><span class="sxs-lookup"><span data-stu-id="a544d-109">EXAMPLES</span></span>

### <span data-ttu-id="a544d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a544d-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="a544d-111">更新已註冊 vCenter 的探索詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a544d-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="a544d-112">參數</span><span class="sxs-lookup"><span data-stu-id="a544d-112">PARAMETERS</span></span>

### <span data-ttu-id="a544d-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a544d-113">-Account</span></span>
<span data-ttu-id="a544d-114">vCenter 登入認證帳戶。</span><span class="sxs-lookup"><span data-stu-id="a544d-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="a544d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a544d-115">-DefaultProfile</span></span>
<span data-ttu-id="a544d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a544d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a544d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a544d-117">-InputObject</span></span>
<span data-ttu-id="a544d-118">要更新其探索詳細資料的 vCenter 伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="a544d-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="a544d-119">-埠</span><span class="sxs-lookup"><span data-stu-id="a544d-119">-Port</span></span>
<span data-ttu-id="a544d-120">VCenter 伺服器上用來進行探索的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="a544d-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="a544d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a544d-121">-ResourceId</span></span>
<span data-ttu-id="a544d-122">指定 vCenter 的 resourceId。</span><span class="sxs-lookup"><span data-stu-id="a544d-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="a544d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a544d-123">-Confirm</span></span>
<span data-ttu-id="a544d-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a544d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a544d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a544d-125">-WhatIf</span></span>
<span data-ttu-id="a544d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a544d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a544d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a544d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a544d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a544d-128">CommonParameters</span></span>
<span data-ttu-id="a544d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a544d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a544d-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a544d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a544d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a544d-131">INPUTS</span></span>

### <span data-ttu-id="a544d-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a544d-132">System.String</span></span>

### <span data-ttu-id="a544d-133">RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="a544d-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="a544d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a544d-134">OUTPUTS</span></span>

### <span data-ttu-id="a544d-135">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a544d-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a544d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a544d-136">NOTES</span></span>

## <span data-ttu-id="a544d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a544d-137">RELATED LINKS</span></span>
