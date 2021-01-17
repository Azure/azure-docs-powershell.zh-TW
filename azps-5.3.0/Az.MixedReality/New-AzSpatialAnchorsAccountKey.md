---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438664"
---
# <span data-ttu-id="2bfff-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="2bfff-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="2bfff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bfff-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfff-103">[重新產生空間錨點] 帳戶的金鑰</span><span class="sxs-lookup"><span data-stu-id="2bfff-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="2bfff-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bfff-104">SYNTAX</span></span>

### <span data-ttu-id="2bfff-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bfff-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bfff-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bfff-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bfff-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bfff-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bfff-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bfff-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bfff-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bfff-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bfff-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bfff-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bfff-111">說明</span><span class="sxs-lookup"><span data-stu-id="2bfff-111">DESCRIPTION</span></span>
<span data-ttu-id="2bfff-112">重新產生 [空間錨點] 帳戶的主鍵或輔助索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2bfff-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="2bfff-113">示例</span><span class="sxs-lookup"><span data-stu-id="2bfff-113">EXAMPLES</span></span>

### <span data-ttu-id="2bfff-114">範例1</span><span class="sxs-lookup"><span data-stu-id="2bfff-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="2bfff-115">在資源群組 "rg1" 中，重新產生空間錨點的次要金鑰 [範例]。</span><span class="sxs-lookup"><span data-stu-id="2bfff-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="2bfff-116">範例2</span><span class="sxs-lookup"><span data-stu-id="2bfff-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="2bfff-117">使用管道從目前訂閱和資源群組 "rg1" 重新產生空間錨點 "範例" 的次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="2bfff-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="2bfff-118">參數</span><span class="sxs-lookup"><span data-stu-id="2bfff-118">PARAMETERS</span></span>

### <span data-ttu-id="2bfff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bfff-119">-DefaultProfile</span></span>
<span data-ttu-id="2bfff-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bfff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2bfff-121">-Force</span></span>
<span data-ttu-id="2bfff-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2bfff-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bfff-123">-InputObject</span></span>
<span data-ttu-id="2bfff-124">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="2bfff-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bfff-125">-Name</span></span>
<span data-ttu-id="2bfff-126">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfff-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-127">-主要</span><span class="sxs-lookup"><span data-stu-id="2bfff-127">-Primary</span></span>
<span data-ttu-id="2bfff-128">重新產生空間錨點帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="2bfff-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfff-129">-ResourceGroupName</span></span>
<span data-ttu-id="2bfff-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfff-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bfff-131">-ResourceId</span></span>
<span data-ttu-id="2bfff-132">空間錨定帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bfff-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-133">-副</span><span class="sxs-lookup"><span data-stu-id="2bfff-133">-Secondary</span></span>
<span data-ttu-id="2bfff-134">重新產生空間錨點帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="2bfff-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfff-135">-確認</span><span class="sxs-lookup"><span data-stu-id="2bfff-135">-Confirm</span></span>
<span data-ttu-id="2bfff-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bfff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bfff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bfff-137">-WhatIf</span></span>
<span data-ttu-id="2bfff-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bfff-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bfff-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bfff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bfff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfff-140">CommonParameters</span></span>
<span data-ttu-id="2bfff-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bfff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2bfff-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bfff-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfff-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2bfff-143">INPUTS</span></span>

### <span data-ttu-id="2bfff-144">System.object</span><span class="sxs-lookup"><span data-stu-id="2bfff-144">System.String</span></span>

### <span data-ttu-id="2bfff-145">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="2bfff-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="2bfff-146">輸出</span><span class="sxs-lookup"><span data-stu-id="2bfff-146">OUTPUTS</span></span>

### <span data-ttu-id="2bfff-147">MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2bfff-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="2bfff-148">筆記</span><span class="sxs-lookup"><span data-stu-id="2bfff-148">NOTES</span></span>

## <span data-ttu-id="2bfff-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bfff-149">RELATED LINKS</span></span>
