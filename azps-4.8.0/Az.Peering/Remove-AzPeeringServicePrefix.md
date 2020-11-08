---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970241"
---
# <span data-ttu-id="c28eb-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c28eb-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="c28eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c28eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c28eb-103">移除新的對等服務首碼</span><span class="sxs-lookup"><span data-stu-id="c28eb-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="c28eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c28eb-104">SYNTAX</span></span>

### <span data-ttu-id="c28eb-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="c28eb-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c28eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c28eb-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c28eb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c28eb-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c28eb-108">說明</span><span class="sxs-lookup"><span data-stu-id="c28eb-108">DESCRIPTION</span></span>
<span data-ttu-id="c28eb-109">從對等服務移除對等服務的首碼。</span><span class="sxs-lookup"><span data-stu-id="c28eb-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="c28eb-110">示例</span><span class="sxs-lookup"><span data-stu-id="c28eb-110">EXAMPLES</span></span>

### <span data-ttu-id="c28eb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c28eb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="c28eb-112">從對等服務物件移除前置詞</span><span class="sxs-lookup"><span data-stu-id="c28eb-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="c28eb-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c28eb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="c28eb-114">從對等服務資源識別碼移除前置詞。</span><span class="sxs-lookup"><span data-stu-id="c28eb-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="c28eb-115">範例3</span><span class="sxs-lookup"><span data-stu-id="c28eb-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="c28eb-116">從對等服務資源群組名稱和名稱移除前置詞</span><span class="sxs-lookup"><span data-stu-id="c28eb-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="c28eb-117">參數</span><span class="sxs-lookup"><span data-stu-id="c28eb-117">PARAMETERS</span></span>

### <span data-ttu-id="c28eb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c28eb-118">-AsJob</span></span>
<span data-ttu-id="c28eb-119">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="c28eb-119">Run in the background.</span></span>

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

### <span data-ttu-id="c28eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28eb-120">-DefaultProfile</span></span>
<span data-ttu-id="c28eb-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c28eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28eb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c28eb-122">-Force</span></span>
<span data-ttu-id="c28eb-123">強制完成操作</span><span class="sxs-lookup"><span data-stu-id="c28eb-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="c28eb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c28eb-124">-InputObject</span></span>
<span data-ttu-id="c28eb-125">使用 Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c28eb-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="c28eb-126">-Name</span></span>
<span data-ttu-id="c28eb-127">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="c28eb-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c28eb-128">-PassThru</span></span>
<span data-ttu-id="c28eb-129">如果失敗，則傳回 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="c28eb-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="c28eb-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="c28eb-130">-PrefixName</span></span>
<span data-ttu-id="c28eb-131">前置詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="c28eb-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28eb-132">-ResourceGroupName</span></span>
<span data-ttu-id="c28eb-133">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c28eb-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c28eb-134">-ResourceId</span></span>
<span data-ttu-id="c28eb-135">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="c28eb-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c28eb-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c28eb-136">-Confirm</span></span>
<span data-ttu-id="c28eb-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c28eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28eb-138">-WhatIf</span></span>
<span data-ttu-id="c28eb-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c28eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28eb-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c28eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28eb-141">CommonParameters</span></span>
<span data-ttu-id="c28eb-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c28eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28eb-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c28eb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28eb-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c28eb-144">INPUTS</span></span>

### <span data-ttu-id="c28eb-145">PSPeeringServicePrefix 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="c28eb-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="c28eb-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c28eb-146">System.String</span></span>

## <span data-ttu-id="c28eb-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c28eb-147">OUTPUTS</span></span>

### <span data-ttu-id="c28eb-148">System.object</span><span class="sxs-lookup"><span data-stu-id="c28eb-148">System.Boolean</span></span>

## <span data-ttu-id="c28eb-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c28eb-149">NOTES</span></span>

## <span data-ttu-id="c28eb-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c28eb-150">RELATED LINKS</span></span>
