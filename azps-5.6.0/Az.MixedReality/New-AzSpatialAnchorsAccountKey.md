---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 7c94b9fd1395af8b64425837d1fb08c578b3c2a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916733"
---
# <span data-ttu-id="a57d4-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="a57d4-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="a57d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a57d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a57d4-103">重新產生空間錨點帳戶的金鑰</span><span class="sxs-lookup"><span data-stu-id="a57d4-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="a57d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="a57d4-104">SYNTAX</span></span>

### <span data-ttu-id="a57d4-105">重新產生PrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57d4-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57d4-106">重新產生一個KeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57d4-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57d4-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57d4-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57d4-108">ResourceIdRegenerate2aryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57d4-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57d4-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57d4-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57d4-110">PipelineRegenerate2aryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57d4-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57d4-111">描述</span><span class="sxs-lookup"><span data-stu-id="a57d4-111">DESCRIPTION</span></span>
<span data-ttu-id="a57d4-112">重新產生空間錨點帳戶的主鍵或次要鍵。</span><span class="sxs-lookup"><span data-stu-id="a57d4-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="a57d4-113">例子</span><span class="sxs-lookup"><span data-stu-id="a57d4-113">EXAMPLES</span></span>

### <span data-ttu-id="a57d4-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="a57d4-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="a57d4-115">在資源群組 "rg1" 中重新產生空間錨點帳戶的次要索引鍵「範例」。</span><span class="sxs-lookup"><span data-stu-id="a57d4-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="a57d4-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="a57d4-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a57d4-117">使用管道從目前的訂閱和資源群組 "rg1" 重新產生空間錨點帳戶的次要索引鍵「範例」。</span><span class="sxs-lookup"><span data-stu-id="a57d4-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="a57d4-118">參數</span><span class="sxs-lookup"><span data-stu-id="a57d4-118">PARAMETERS</span></span>

### <span data-ttu-id="a57d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57d4-119">-DefaultProfile</span></span>
<span data-ttu-id="a57d4-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a57d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57d4-121">-強制</span><span class="sxs-lookup"><span data-stu-id="a57d4-121">-Force</span></span>
<span data-ttu-id="a57d4-122">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a57d4-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a57d4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a57d4-123">-InputObject</span></span>
<span data-ttu-id="a57d4-124">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="a57d4-124">The custom domain object.</span></span>

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

### <span data-ttu-id="a57d4-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a57d4-125">-Name</span></span>
<span data-ttu-id="a57d4-126">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a57d4-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="a57d4-127">-主要</span><span class="sxs-lookup"><span data-stu-id="a57d4-127">-Primary</span></span>
<span data-ttu-id="a57d4-128">重新產生空間錨點帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="a57d4-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="a57d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="a57d4-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a57d4-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="a57d4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a57d4-131">-ResourceId</span></span>
<span data-ttu-id="a57d4-132">空間錨點帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a57d4-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="a57d4-133">-次要</span><span class="sxs-lookup"><span data-stu-id="a57d4-133">-Secondary</span></span>
<span data-ttu-id="a57d4-134">重新產生空間錨點帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="a57d4-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="a57d4-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a57d4-135">-Confirm</span></span>
<span data-ttu-id="a57d4-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a57d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57d4-137">-WhatIf</span></span>
<span data-ttu-id="a57d4-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a57d4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a57d4-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a57d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57d4-140">CommonParameters</span></span>
<span data-ttu-id="a57d4-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a57d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a57d4-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a57d4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57d4-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a57d4-143">INPUTS</span></span>

### <span data-ttu-id="a57d4-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a57d4-144">System.String</span></span>

### <span data-ttu-id="a57d4-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a57d4-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a57d4-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a57d4-146">OUTPUTS</span></span>

### <span data-ttu-id="a57d4-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a57d4-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="a57d4-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a57d4-148">NOTES</span></span>

## <span data-ttu-id="a57d4-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a57d4-149">RELATED LINKS</span></span>
